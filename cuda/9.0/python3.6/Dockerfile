FROM nvidia/cuda::9.0-runtime-ubuntu16.04
RUN apt-get install -y git
RUN apt-get install -y build-essential libbz2-dev libssl-dev libreadline-dev \
                        libffi-dev libsqlite3-dev tk-dev
RUN apt-get install -y libpng-dev libfreetype6-dev
RUN curl -L https://github.com/pyenv/pyenv-installer/raw/master/bin/pyenv-installer | bash
RUN export PATH="$HOME/.pyenv/bin:$PATH"
RUN eval "$(pyenv init -)"
RUN eval "$(pyenv virtualenv-init -)"
RUN pyenv install 3.6.0
pyenv virtualenv 3.6.0 general
pyenv global general