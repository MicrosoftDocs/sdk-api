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

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">sockaddr</a> structure that contains the Internet Protocol (IP) address with which this SSL certificate is associated.

If the <b>sin_addr</b> field in <b>IpPort</b> is set to 0.0.0.0, the certificate is applicable to all IPv4 and IPv6 addresses.
   If the <b>sin6_addr</b> field in <b>IpPort</b> is set to [::], the certificate is applicable to all IPv6 addresses.



## -see-also




<a href="https://msdn.microsoft.com/0ae94936-4c6a-4c9f-adb8-5e3af75cf486">HTTPDeleteServiceConfiguration</a>



<a href="https://msdn.microsoft.com/733b451a-d35b-4b83-ba49-0529309cd99b">HTTP_SERVICE_CONFIG_SSL_QUERY</a>



<a href="https://msdn.microsoft.com/23adda0b-907d-4804-9c12-e549af4f18c4">HTTP_SERVICE_CONFIG_SSL_SET</a>
 

 

