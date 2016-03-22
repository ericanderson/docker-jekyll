# docker-jekyll
A very simple docker image for building site via drone

Example .drone.yml:

    build:
      image: ericanderson/jekyll
      commands:
      - 'echo "baseurl: /tmp/$$BRANCH" > _config2.yml'
      - jekyll build  --config _config.yml,_config2.yml

Note on the above:

The multiple config files enable us to publish branches under a different location than the root.
