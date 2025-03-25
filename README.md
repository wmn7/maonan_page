# Maonan's Academic Pages

## Local Development

### Docker Build & Docker Run

To get started with local development, first clone the repository. Navigate into the cloned directory and build the Docker image with the following command:

```bash
docker build -t jekyll-site .
```

You can verify the image creation by running `docker images`. Once the image is ready, start the local server with:

```bash
docker run --rm -p 127.0.0.1:5000:4000 -v <path-to-your-project>:/usr/src/app jekyll-site
```

This command will allow you to edit your website content locally. After making your changes, compile the site using:

```bash
jekyll build
```

Once the build is complete, you can view the updated site by opening [http://127.0.0.1:5000](http://127.0.0.1:5000) in your web browser.

### Docker Compose

Alternatively, you can use Docker Compose to start the server:

```bash
docker compose up
```

After finishing your debugging session, you can stop the server with:

```bash
docker compose down
```

## Acknowledgments

Special thanks to [Academicpages](https://github.com/academicpages/academicpages.github.io) for providing the template.
