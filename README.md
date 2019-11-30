# keep-password-secret
> Example site for showing how to prevent accidentally revealing passwords during Cypress tests

Actual login and password: `jack` and `secret`

Originally cloned from [passport/express-4.x-local-example](https://github.com/passport/express-4.x-local-example)

## Tests

### login-spec.js

[cypress/integration/login-spec.js](cypress/integration/login-spec.js) types username and password into the form and submits its. Notice that you can see the entered password in the spec video and screenshots - this is insecure.

![Login spec showing the password](images/login-spec.gif)

### no-password-spec.js

[cypress/integration/no-password-spec.js](cypress/integration/no-password-spec.js) avoids hardcoding the username and the password by reading them from environment variables using [Cypress.env](https://on.cypress.io/env) command.
