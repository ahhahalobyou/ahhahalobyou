<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Facebook Login</title>
</head>
<body>
    <h1>Login with Facebook</h1>
    <div id="fb-root"></div>
    <script async defer crossorigin="anonymous" src="https://connect.facebook.net/en_US/sdk.js"></script>
    <script>
        window.fbAsyncInit = function() {
            FB.init({
                appId      : 'YOUR_APP_ID',
                cookie     : true,
                xfbml      : true,
                version    : 'v12.0'
            });
        };

        function checkLoginState() {
            FB.getLoginStatus(function(response) {
                console.log(response);
            });
        }
    </script>
    <fb:login-button 
        scope="public_profile,email"
        onlogin="checkLoginState();">
    </fb:login-button>
</body>
</html>
