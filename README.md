# A sample that runs NGINX with a self-signed certificate

This is a sample Docker Compose configuration to run an NGINX server with a self-signed certificate.

## Requirements

- Docker
- Docker Compose `>=1.29.0`

## Usage

```zsh
docker compose build
docker compose up -d
```

```zsh
curl --insecure \
    --resolve 'example.local:443:127.0.0.1' \
    https://example.local
```

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <title>Hello</title>
    <style type="text/css">
        body {
            margin: 0;
            padding: 0;
            font-family: sans-serif;
        }
        .bodywrapper {
            width: 100vw;
            height: 100vh;
            display: flex;
            flex-direction: row;
            justify-content: center;
            align-items: center;
            background-color: #f4f8f8;
        }
    </style>
</head>
<body>
    <div class="bodywrapper">
        <h1>Hello.</h1>
    </div>
</body>
</html>
```

## References

- [Depends_on condition service_completed_successfully · Issue #8154 · docker/compose · GitHub](https://github.com/docker/compose/issues/8154)
- [Release 1.29.0 · docker/compose · GitHub](https://github.com/docker/compose/releases/tag/1.29.0)
