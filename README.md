OANDA client side OAuth javascript demo
=========================

A simple JavaScript application to demonstrate the OANDA client side OAuth flow

To run this, you will need a webserver to host 'clientSide_demo.html' that is included in this package.
'clientSide_demo.html' should be served at where your 'redirect uri' was registered as.

For example, if you registered your application's 'redirect uri' as 'https://xyz.com/clientSide_demo.html', then please ensure 'clientSide_demo.html' is served at that URI.

Within 'clientSide_demo.html', you will need update the <client application id> with your application's client_id, and <redirect uri> with your application's registered 'redirect uri'.  Please see http://developer.oanda.com/docs/v1/auth/#third-party-applications for more details.

*Note your webserver must support TLS/SSL

====================================

Once 'clientSide_demo.html' is loaded in the browser, two bottons will be displayed at the top of the screen.<br>

1.  Begin OANDA Client-Side OAuth Flow
        Once clicked, this button will redirect the user to OANDA's OAuth page to begin the client side OAuth process.
The user will then be asked to sign in to grant/deny the client application access to their account.  Once the grant/deny step is completed, the user will be redirected back to the 'redirect uri' (For this demo's sake, it should be where 'clientSide_demo.html' is being hosted).

2.  Get Account Information
        Once access has been granted (access token returned), clicking this button will return the information about the user's first account.  This button will invoke an authenticated call to OANDA's /v1/accounts endpoint.
