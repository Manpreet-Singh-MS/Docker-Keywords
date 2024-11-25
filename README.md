## Dockerfile Keywords ##


Dockerfile Keywords
FROM
Specifies the base image. This is mandatory and must be the first line in the Dockerfile.
Example:
FROM ubuntu:20.04
RUN
Executes commands in the shell during the build phase.
Example:
RUN apt-get update && apt-get install -y curl
CMD
Specifies the default command for the container. This command can be overridden at runtime.
Example:
CMD ["nginx", "-g", "daemon off;"]
ENTRYPOINT
Specifies the executable for the container. Unlike CMD, this is not easily overridden.
Example:
ENTRYPOINT ["python", "app.py"]
COPY
Copies files or directories from the build context to the image.
Example:
COPY ./app /usr/src/app
ADD
Similar to COPY, but also handles archives and URLs.
Example:
ADD https://example.com/file.tar.gz /app/
WORKDIR
Sets the working directory for subsequent instructions.
Example:
WORKDIR /usr/src/app
ENV
Sets environment variables for the container.
Example:
ENV NODE_ENV=production
EXPOSE
Documents the ports the container will listen on.
Example:
EXPOSE 8080
ARG
Defines build-time variables.
Example:
ARG VERSION=1.0
LABEL
Adds metadata to the image.
Example:
LABEL maintainer="your_email@example.com"
USER
Specifies the user for running the container.
Example:
USER nonroot
VOLUME
Defines mount points for external volumes.
Example:
VOLUME /data
ONBUILD
Adds triggers for child images, which execute when the child image is built.
Example:
ONBUILD RUN apt-get update
STOPSIGNAL
Sets the system call signal to stop the container.
Example:
STOPSIGNAL SIGTERM
SHELL
Changes the default shell used for RUN commands.
Example:
SHELL ["powershell", "-Command"]

