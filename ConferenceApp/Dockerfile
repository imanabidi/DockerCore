﻿FROM microsoft/aspnetcore-build:2.0 as build
COPY . . 
RUN dotnet restore
RUN dotnet publish -c Release -o output

FROM microsoft/aspnetcore:2.0
COPY --from=build /build/output .
ENTRYPOINT ["dotnet","ConferenceApp.dll"]
