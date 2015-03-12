# steam-on-linode
Running steam dedicated servers on Linode

# Getting a Steam API Key
İt is possible to run dedicated game servers anonymously, which we will do, but if you'd like to get an API key for your TF2 server then you need a steam account and and request API access from the dev portal.

When you have the API key it is a matter of a curl post to get an auth token for the server:

curl --data "appid=440&key=$SteamApiKey" https://api.steampowered.com/IGameServersService/CreateAccount/v0001/

and you will be greeted with a JSON response (this one is made up of course)

~~~

{
	"response": {
		"steamid": "88888888888888888",
		"login_token": "AFAFAFAFAFAFAFAFAFAFAFAFAFAFAFAF"
	}

~~~
