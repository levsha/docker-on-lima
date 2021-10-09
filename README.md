# docker-on-lima
Run docker on Mac OS using alpine VM run by [lima](https://github.com/lima-vm/lima).

Guest OS (and docker as result) is always x86_64. Yes, even on M1.


# Install

```sh
brew install lima
cd ~/src
git clone https://github.com/levsha/docker-on-lima.git
ln -s $(pwd)/docker-on-lima/docker-on-lima ~/bin/
```

# Use
```sh
docker-on-lima start
docker ...
```

# Known issues
* It takes about a minute for the provision script to install and start dockerd. Therefore `docker` returns `Cannot connect to the Docker daemon ...` right after start.
* [kind](https://kind.sigs.k8s.io/) does not work on alpine.
