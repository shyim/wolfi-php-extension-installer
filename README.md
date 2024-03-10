# Wofli PHP Extension Installer

This script should covers all PHP proprietary extensions for PHP. All open source PHP extensions should be directly submitted to [WolfiOS itself](https://github.com/wolfi-dev/os).

Inspired by https://github.com/mlocati/docker-php-extension-installer

## Supported Extensions

- Blackfire
- Tideways

## Installation

### Copy into Image

```dockerfile
ADD https://raw.githubusercontent.com/shyim/wolfi-php-extension-installer/main/install-wolfi-php-extensions /usr/bin/install-wolfi-php-extensions

RUN sh /usr/bin/install-wolfi-php-extensions blackfire
```

### Execute directly

```dockerfile
RUN apk add --no-cache curl

RUN curl -sSL https://raw.githubusercontent.com/shyim/wolfi-php-extension-installer/main/install-wolfi-php-extensions | sh -s blackfire
```


## Usage

```bash
install-wolfi-php-extensions blackfire
```

You can pass also multiple ones.


