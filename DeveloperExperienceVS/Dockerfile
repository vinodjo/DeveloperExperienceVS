FROM microsoft/aspnetcore:1.1
#RUN apt-get update
#RUN apt-get install curl libunwind8 gettext -y
#Installing DOTNET CORE SDK
#ENV DOTNET_VERSION 1.1.1
#ENV DOTNET_DOWNLOAD_URL 'https://dotnetcli.azureedge.net/dotnet/Sdk/1.0.1/dotnet-dev-debian-x64.1.0.1.tar.gz'
#RUN curl -SL $DOTNET_DOWNLOAD_URL --output dotnet.tar.gz \
#&& mkdir -p /usr/share/dotnet \
#&& tar -zxf dotnet.tar.gz -C /usr/share/dotnet \
#&& rm dotnet.tar.gz \
#&& ln -s /usr/share/dotnet/dotnet /usr/bin/dotnet
ARG source
WORKDIR /app
EXPOSE 80
COPY ${source:-obj/Docker/publish} .
ENTRYPOINT ["dotnet", "DeveloperExperienceVS.dll"]
