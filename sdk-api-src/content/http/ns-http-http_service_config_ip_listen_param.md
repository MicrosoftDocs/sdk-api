---
UID: NS:http._HTTP_SERVICE_CONFIG_IP_LISTEN_PARAM
title: HTTP_SERVICE_CONFIG_IP_LISTEN_PARAM (http.h)
author: windows-sdk-content
description: Used to specify an IP address to be added to or deleted from the list of IP addresses to which the HTTP service binds.
old-location: http\http_service_config_ip_listen_param.htm
tech.root: http
ms.assetid: a45fd5e4-0ae4-47fc-bb50-931e0947a6bc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PHTTP_SERVICE_CONFIG_IP_LISTEN_PARAM, HTTP_SERVICE_CONFIG_IP_LISTEN_PARAM, HTTP_SERVICE_CONFIG_IP_LISTEN_PARAM structure [HTTP], PHTTP_SERVICE_CONFIG_IP_LISTEN_PARAM, PHTTP_SERVICE_CONFIG_IP_LISTEN_PARAM structure pointer [HTTP], _http_http_service_config_ip_listen_param, http.http_service_config_ip_listen_param, http/HTTP_SERVICE_CONFIG_IP_LISTEN_PARAM, http/PHTTP_SERVICE_CONFIG_IP_LISTEN_PARAM"
ms.topic: struct
f1_keywords: 
 - "http/HTTP_SERVICE_CONFIG_IP_LISTEN_PARAM"
req.header: http.h
req.include-header: 
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
 - HTTP_SERVICE_CONFIG_IP_LISTEN_PARAM
product: Windows
targetos: Windows
req.typenames: HTTP_SERVICE_CONFIG_IP_LISTEN_PARAM, *PHTTP_SERVICE_CONFIG_IP_LISTEN_PARAM
req.redist: 
ms.custom: 19H1
---

# HTTP_SERVICE_CONFIG_IP_LISTEN_PARAM structure


## -description


The 
<b>HTTP_SERVICE_CONFIG_IP_LISTEN_PARAM</b> structure is used to specify an IP address to be added to or deleted from the list of IP addresses to which the HTTP service binds.


## -struct-fields




### -field AddrLength

The size, in bytes, of the address pointed to by <b>pAddress</b>.


### -field pAddress

A pointer to an Internet Protocol (IP) address to be added to or deleted from the listen list. 




To specify an IPv6 address, use a <a href="http://go.microsoft.com/fwlink/p/?linkid=154492">SOCKADDR_IN6</a> structure, declared in the Ws2tcpip.h header file, and cast its address to a PSOCKADDR when you use it to set the <b>pAddress</b> member. The <b>sin_family</b> member of the SOCKADDR_IN6 should be set to AF_INET6.

  If the <b>sin_addr</b> field in <a href="http://go.microsoft.com/fwlink/p/?linkid=154492">SOCKADDR_IN6</a> structure is set to 0.0.0.0, it means to bind to all IPv4 addresses.
   If the <b>sin6_addr</b> field in <a href="http://go.microsoft.com/fwlink/p/?linkid=154492">SOCKADDR_IN6</a> is set to [::], it means to bind to all IPv6 addresses.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/http/nf-http-httpdeleteserviceconfiguration">HttpDeleteServiceConfiguration</a>



<a href="https://docs.microsoft.com/windows/desktop/api/http/nf-http-httpsetserviceconfiguration">HttpSetServiceConfiguration</a>
 

 

