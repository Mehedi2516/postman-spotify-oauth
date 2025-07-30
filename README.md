🎵 Spotify API with Postman
This project demonstrates how to use OAuth 2.0 Authorization Code Flow in Postman to interact with the Spotify Web API. The goal is to log in, create a playlist, add tracks to it, and explore playlist-related endpoints using your own Spotify developer credentials.

📌 Prerequisites
Before getting started, make sure you’ve completed the following:

✅ Read about OAuth 2.0 Authorization Code Flow.

✅ Create a Spotify account at https://open.spotify.com/.

✅ Create a Developer App and Dashboard at Spotify Developer Portal:
Set Redirect URI as: https://oauth.pstmn.io/v1/callback

✅ Familiarize yourself with the Spotify Web API Documentation.
Set Up OAuth 2.0 in Authorization Tab

Type: Authorization Code

Auth URL: https://accounts.spotify.com/authorize

Access Token URL: https://accounts.spotify.com/api/token

Client ID: {{client_id}}

Client Secret: {{client_secret}}

Scope:
playlist-read-private playlist-read-collaborative playlist-modify-private playlist-modify-public
Redirect URI: https://oauth.pstmn.io/v1/callback
Redirect URI: https://oauth.pstmn.io/v1/callback

Create Environment in Postman with variables:
client_id
client_secret
user_id 
access_token
    
Create a New Playlist
Endpoint: POST https://api.spotify.com/v1/users/{{user_id}}/playlists
Body (raw JSON):

    {
      "name": "My Cool Playlist",
      "description": "TAD is the best",
      "public": false
    }

Add Tracks to Playlist
Choose 3 tracks of your choice.
Endpoint: POST https://api.spotify.com/v1/playlists/{{playlist_id}}/tracks

Body (raw JSON):

    {
        "uris": [
        "spotify:track:TRACK_ID_1",
        "spotify:track:TRACK_ID_2",
        "spotify:track:TRACK_ID_3"
      ]
    }
✅ Done! Enjoy your playlist—dance or sing these songs

💡 Tips
Your Client ID, Client Secret, and User ID should be saved in Postman environment variables.

Use Authorization → Bearer Token with {{access_token}} in all secured requests.

Make sure you click "Get New Access Token" when it expires.






