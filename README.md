# Moby Dick

All-in-one Docker Image for standard Symfony applications. This Docker Image could be used for any demo or workshop but shouldn't be used in production!
 
## Contents
The Docker Image contains a nginx + PHP 7.3 setup.
 
## Usage
Just place or mount your code under `/code` and you're done.


Docker Compose

    app:
      image: frastel/moby-dick
      ports:
        - "8080:80"
      volumes:
        - ./components/app:/code
      environment:
        - SYMFONY_PHPUNIT_VERSION=7.5
        - FOO=bar
