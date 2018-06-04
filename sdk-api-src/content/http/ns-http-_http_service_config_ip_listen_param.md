---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _HTTP_SERVICE_CONFIG_IP_LISTEN_PARAM structure


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




<a href="https://msdn.microsoft.com/0ae94936-4c6a-4c9f-adb8-5e3af75cf486">HttpDeleteServiceConfiguration</a>



<a href="https://msdn.microsoft.com/b0a6d442-2ff4-4e00-8301-696fb0864d8c">HttpSetServiceConfiguration</a>
 

 

