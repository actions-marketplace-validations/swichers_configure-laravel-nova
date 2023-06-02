# Configure Laravel Nova

A GitHub action for configuring composer to use Laravel Nova

## Usage

```yml
      - uses: actions/checkout@v3

      - uses: swichers/configure-laravel-nova@v1
        with:
          user: ${{ secrets.NOVA_USER }}
          token: ${{ secrets.NOVA_TOKEN }}

      - uses: "ramsey/composer-install@v2"

      # Composer should be able to access Repman based packages.
```

## Action inputs

All inputs are required.

| Name           | Description                                                       |
|----------------|-------------------------------------------------------------------|
| `user`         | The user you use to authenticate on nova.laravel.com              |
| `token`        | A Nova access token.                                              |

It is recommended to use a secret configured in GitHub instead of hard coding the access token.
