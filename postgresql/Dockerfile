FROM postgres:16-bullseye

# https://www.postgresql.org/download/linux/ubuntu/
# https://wiki.postgresql.org/wiki/Apt
# https://www.ubuntuupdates.org/ppa/postgresql?dist=focal-pgdg
# https://www.ubuntuupdates.org/package/postgresql/focal-pgdg/main/base/pg-partman
# https://www.ubuntuupdates.org/package/postgresql/focal-pgdg/main/base/postgresql-16-partman?id=2575230&page=1

ARG PG_EXTENSION="postgresql-16-partman"

ARG BUILDPKG="build-essential \
				curl \
				git"

RUN apt-get update \
	&& apt-get upgrade -y \
	&& apt-get install -y --no-install-recommends $BUILDPKG \
	&& apt-get install -y postgresql-server-dev-16

RUN apt-get update \
	&& apt-get upgrade -y $PG_EXTENSION

