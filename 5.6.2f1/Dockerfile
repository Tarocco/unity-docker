FROM ubuntu

# http://forum.unity3d.com/threads/unity-on-linux-release-notes-and-known-issues.350256/

ENV UNITY_DOWNLOAD_ID ddd95e743b51
ENV UNITY_PACKAGE_NAME unity-editor_amd64-5.6.2xf1Linux.deb

ENV UNITY_PACKAGE_URL https://beta.unity3d.com/download/$UNITY_DOWNLOAD_ID/$UNITY_PACKAGE_NAME
ENV UNITY_PACKAGE_PATH /data/$UNITY_PACKAGE_NAME

RUN apt-get update && apt-get install -y \
      gconf-service \
      lib32gcc1 \
      lib32stdc++6 \
      libasound2 \
      libc6 \
      libc6-i386 \
      libcairo2 \
      libcap2 \
      libcups2 \
      libdbus-1-3 \
      libexpat1 \
      libfontconfig1 \
      libfreetype6 \
      libgcc1 \
      libgconf-2-4 \
      libgdk-pixbuf2.0-0 \
      libgl1-mesa-glx \
      libglib2.0-0 \
      libglu1-mesa \
      libgtk2.0-0 \
      libnspr4 \
      libnss3 \
      libpango1.0-0 \
      libstdc++6 \
      libx11-6 \
      libxcomposite1 \
      libxcursor1 \
      libxdamage1 \
      libxext6 \
      libxfixes3 \
      libxi6 \
      libxrandr2 \
      libxrender1 \
      libxtst6 \
      zlib1g \
      debconf \
      psmisc \
      npm \
      xdg-utils \
      lsb-release \
      libpq5 \
      wget \
      xvfb

RUN wget -nc -O $UNITY_PACKAGE_PATH $UNITY_PACKAGE_URL && \
    dpkg -i $UNITY_PACKAGE_PATH
