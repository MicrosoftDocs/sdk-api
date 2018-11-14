---
UID: NS:http._HTTP_SERVICE_CONFIG_SSL_SNI_KEY
title: "_HTTP_SERVICE_CONFIG_SSL_SNI_KEY"
author: windows-sdk-content
description: Serves as the key by which a given Secure Sockets Layer (SSL) Server Name Indication (SNI) certificate record is identified in the SSL SNI store.
old-location: http\http_service_config_ssl_sni_key.htm
tech.root: Http
ms.assetid: 0EABB454-B4B9-4912-8E81-7930164B12F2
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PHTTP_SERVICE_CONFIG_SSL_SNI_KEY, HTTP_SERVICE_CONFIG_SSL_SNI_KEY, HTTP_SERVICE_CONFIG_SSL_SNI_KEY structure [HTTP], PHTTP_SERVICE_CONFIG_SSL_SNI_KEY, PHTTP_SERVICE_CONFIG_SSL_SNI_KEY structure pointer [HTTP], _HTTP_SERVICE_CONFIG_SSL_SNI_KEY, http.http_service_config_ssl_sni_key, http/HTTP_SERVICE_CONFIG_SSL_SNI_KEY, http/PHTTP_SERVICE_CONFIG_SSL_SNI_KEY"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_SERVICE_CONFIG_SSL_SNI_KEY
product: Windows
targetos: Windows
req.typenames: HTTP_SERVICE_CONFIG_SSL_SNI_KEY, *PHTTP_SERVICE_CONFIG_SSL_SNI_KEY
req.redist: 
---

# _HTTP_SERVICE_CONFIG_SSL_SNI_KEY structure


## -description


The 
<b>HTTP_SERVICE_CONFIG_SSL_SNI_KEY</b> structure serves as the key by which a given Secure Sockets Layer (SSL) Server Name Indication (SNI) certificate record is identified in the SSL SNI store.  It appears in the 
<a href="https://msdn.microsoft.com/382838B9-C15E-459F-AC40-ECA15EFC18B8">HTTP_SERVICE_CONFIG_SSL_SNI_SET</a> and the 
<a href="https://msdn.microsoft.com/9C45B1B1-5572-4153-BBA4-0E8A52F650CA">HTTP_SERVICE_CONFIG_SSL_SNI_QUERY</a> structures, and is passed as the <i>pConfigInformation</i> parameter to 
<a href="https://msdn.microsoft.com/0ae94936-4c6a-4c9f-adb8-5e3af75cf486">HttpDeleteServiceConfiguration</a>, 
<a href="https://msdn.microsoft.com/bbd2c3c4-d2d0-4590-9b5c-6916b91600cd">HttpQueryServiceConfiguration</a>, and 
<a href="https://msdn.microsoft.com/b0a6d442-2ff4-4e00-8301-696fb0864d8c">HttpSetServiceConfiguration</a> when the <i>ConfigId</i> parameter is set to <b>HttpServiceConfigSslSniCertInfo</b>.


## -struct-fields




### -field IpPort

A <a href="https://msdn.microsoft.com/dfd84b91-0a94-4fe6-b8d2-18562afb9c24">SOCKADDR_STORAGE</a> structure that contains the Internet Protocol version 4 (IPv4) address with which this SSL SNI certificate is associated. It must be set to the IPv4 wildcard address of type <b>SOCKADDR_IN</b> with <b>ss_family</b> set to <b>AF_INET</b> and <b>sin_addr</b> filled with zeros. <b>Port</b> can be any valid port.


### -field Host

A pointer to a null-terminated Unicode UTF-16 string that represents the hostname. 


## -see-also




<a href="https://msdn.microsoft.com/9C45B1B1-5572-4153-BBA4-0E8A52F650CA">HTTP_SERVICE_CONFIG_SSL_SNI_QUERY</a>



<a href="https://msdn.microsoft.com/382838B9-C15E-459F-AC40-ECA15EFC18B8">HTTP_SERVICE_CONFIG_SSL_SNI_SET</a>



<a href="https://msdn.microsoft.com/0ae94936-4c6a-4c9f-adb8-5e3af75cf486">HttpDeleteServiceConfiguration</a>



<a href="https://msdn.microsoft.com/bbd2c3c4-d2d0-4590-9b5c-6916b91600cd">HttpQueryServiceConfiguration</a>



<a href="https://msdn.microsoft.com/b0a6d442-2ff4-4e00-8301-696fb0864d8c">HttpSetServiceConfiguration</a>
 

 

