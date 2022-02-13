oauthSignIn = function(clientId, redirectUrl) {
  // Google's OAuth 2.0 endpoint for requesting an access token
  var oauth2Endpoint = 'https://accounts.google.com/o/oauth2/v2/auth';

  // Create <form> element to submit parameters to OAuth 2.0 endpoint.
  var form = document.createElement('form');
  form.setAttribute('method', 'GET'); // Send as a GET request.
  form.setAttribute('action', oauth2Endpoint);

  // Parameters to pass to OAuth 2.0 endpoint.
  var params = {
    'client_id': clientId,
    'redirect_uri': redirectUrl,
    'response_type': 'code',
    'scope': 'https://www.googleapis.com/auth/something',
    'access_type': 'offline',
    'include_granted_scopes': 'true',
    'state': 'pass-through value'
  };

  // Add form parameters as hidden input values.
  for (var p in params) {
    var input = document.createElement('input');
    input.setAttribute('type', 'hidden');
    input.setAttribute('name', p);
    input.setAttribute('value', params[p]);
    form.appendChild(input);
  }

  // Add form to page and submit it to open the OAuth 2.0 endpoint.
  document.body.appendChild(form);
  form.submit();
}

// oauthSignIn('', "http://localhost")

oauthWithCode = function(clientId, clientSecret, code, redirectUrl) {
  // Google's OAuth 2.0 endpoint for requesting an access token
  var oauth2Endpoint = 'https://oauth2.googleapis.com/token';

  // Create <form> element to submit parameters to OAuth 2.0 endpoint.
  var form = document.createElement('form');
  form.setAttribute('method', 'POST'); // Send as a GET request.
  form.setAttribute('action', oauth2Endpoint);

  // Parameters to pass to OAuth 2.0 endpoint.
  var params = {
    'client_id': clientId,
    'client_secret': clientSecret,
    'redirect_uri': redirectUrl,
    'code': code,
    'grant_type': 'authorization_code',
  };

  // Add form parameters as hidden input values.
  for (var p in params) {
    var input = document.createElement('input');
    input.setAttribute('type', 'hidden');
    input.setAttribute('name', p);
    input.setAttribute('value', params[p]);
    form.appendChild(input);
  }

  // Add form to page and submit it to open the OAuth 2.0 endpoint.
  document.body.appendChild(form);
  form.submit();
}

oauthWithCode('',
              '',
              'insert from result of prev',
              "http://localhost")


