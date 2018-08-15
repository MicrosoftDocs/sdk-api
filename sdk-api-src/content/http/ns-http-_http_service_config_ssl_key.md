---
UID: NS:http._HTTP_SERVICE_CONFIG_SSL_KEY
title: "_HTTP_SERVICE_CONFIG_SSL_KEY"
author: windows-sdk-content
description: Serves as the key by which a given Secure Sockets Layer (SSL) certificate record is identified.
old-location: http\http_service_config_ssl_key.htm
old-project: http
ms.assetid: 67231fa5-69eb-4353-8c3c-326ec9095554
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PHTTP_SERVICE_CONFIG_SSL_KEY, HTTP_SERVICE_CONFIG_SSL_KEY, HTTP_SERVICE_CONFIG_SSL_KEY structure [HTTP], PHTTP_SERVICE_CONFIG_SSL_KEY, PHTTP_SERVICE_CONFIG_SSL_KEY structure pointer [HTTP], _HTTP_SERVICE_CONFIG_SSL_KEY, _http_http_service_config_ssl_key, http.http_service_config_ssl_key, http/HTTP_SERVICE_CONFIG_SSL_KEY, http/PHTTP_SERVICE_CONFIG_SSL_KEY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: http.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: HTTP_SERVICE_CONFIG_SSL_KEY, *PHTTP_SERVICE_CONFIG_SSL_KEY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_SERVICE_CONFIG_SSL_KEY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _HTTP_SERVICE_CONFIG_SSL_KEY structure


## -description


The 
<b>HTTP_SERVICE_CONFIG_SSL_KEY</b> structure serves as the key by which a given Secure Sockets Layer (SSL) certificate record is identified. It appears in the 
<a href="https://msdn.microsoft.com/23adda0b-907d-4804-9c12-e549af4f18c4">HTTP_SERVICE_CONFIG_SSL_SET</a> and the 
<a href="https://msdn.microsoft.com/733b451a-d35b-4b83-ba49-0529309cd99b">HTTP_SERVICE_CONFIG_SSL_QUERY</a> structures, and is passed as the <i>pConfigInformation</i> parameter to 
<a href="https://msdn.microsoft.com/0ae94936-4c6a-4c9f-adb8-5e3af75cf486">HTTPDeleteServiceConfiguration</a>, 
<a href="https://msdn.microsoft.com/bbd2c3c4-d2d0-4590-9b5c-6916b91600cd">HttpQueryServiceConfiguration</a>, and 
<a href="https://msdn.microsoft.com/b0a6d442-2ff4-4e00-8301-696fb0864d8c">HttpSetServiceConfiguration</a> when the <i>ConfigId</i> parameter is set to <b>HttpServiceConfigSSLCertInfo</b>.


## -struct-fields




### -field pIpPort

Pointer to a <a href="https://msdn.microsoft.com/d1392e1c-2b20-425a-8adf-38e665fb6275">sockaddr</a> structure that contains the Internet Protocol (IP) address with which this SSL certificate is associated.

If the <b>sin_addr</b> field in <b>IpPort</b> is set to 0.0.0.0, the certificate is applicable to all IPv4 and IPv6 addresses.
   If the <b>sin6_addr</b> field in <b>IpPort</b> is set to [::], the certificate is applicable to all IPv6 addresses.



## -see-also




<a href="https://msdn.microsoft.com/0ae94936-4c6a-4c9f-adb8-5e3af75cf486">HTTPDeleteServiceConfiguration</a>



<a href="https://msdn.microsoft.com/733b451a-d35b-4b83-ba49-0529309cd99b">HTTP_SERVICE_CONFIG_SSL_QUERY</a>



<a href="https://msdn.microsoft.com/23adda0b-907d-4804-9c12-e549af4f18c4">HTTP_SERVICE_CONFIG_SSL_SET</a>
 

 

