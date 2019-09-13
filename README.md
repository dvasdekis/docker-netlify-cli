# docker-netlify-cli

A Docker image for [netlify/cli](https://github.com/netlify/cli).

## Available tags

*   `latest` &rarr; `2.15.0`
*   `2.14.0`
*   `2.13.1`

## Usage

In your [Netlify user settings][a], create a personal access token. Set the environment variable `NETLIFY_AUTH_TOKEN`
inside the container.

The default working directory in the container is `/project`, so mount your project directory into the container at that
location.

Specify the Netlify CLI command after the image name.

```bash
docker container run -it \
    -e NETLIFY_AUTH_TOKEN=<personal_access_token> \
    -v /path/to/project:/project \
    williamjackson/netlify-cli \
    deploy
```

[a]: https://app.netlify.com/user/applications
