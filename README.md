## GBPHub Wrapper

Assuming you already have docker configured and running on your machine, follow the steps below to run GBPHUB.

1. clone this repo
2. switch to branch `docker` in each submodule
3. copy .env.shared.sample to .env.shared and add your GITHUB_TOKEN
4. build your local image for each specific node version
   `docker build -t gbphub-wrapper-18.17.0 ./docker`
   `docker build -t gbphub-wrapper-18.9.0 ./docker`
5. copy `compose.yaml.sample` to `compose.yaml`
6. install dependencies in each submodule
   docker-compose run --rm opsui npm install
   docker-compose run --rm gbpseui npm install
   docker-compose run --rm gbpcui npm install
7. start all the projects with `docker-compose up`
