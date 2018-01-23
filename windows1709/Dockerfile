FROM microsoft/iis:windowsservercore-1709

RUN mkdir C:\site

RUN powershell -NoProfile -Command \
    Import-module IISAdministration; \
    New-IISSite -Name "Site" -PhysicalPath C:\site -BindingInformation "*:80:"

EXPOSE 80

ADD ../content/ /site
