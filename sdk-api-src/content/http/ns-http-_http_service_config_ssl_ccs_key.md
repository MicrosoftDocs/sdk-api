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

# _HTTP_SERVICE_CONFIG_SSL_CCS_KEY structure


## -description


Serves as the key by which identifies the   SSL certificate record that specifies that Http.sys should consult the Centralized Certificate Store (CCS) store to find certificates if the port receives a Transport Layer Security (TLS) handshake.  


## -struct-fields




### -field LocalAddress

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff570825">SOCKADDR_STORAGE</a> structure that contains the Internet Protocol version 4 (IPv4) address with which this SSL certificate record is associated. It must be set to the IPv4 wildcard address of type <a href="https://msdn.microsoft.com/library/windows/hardware/ff570823">SOCKADDR_IN</a> with the <b>sin_family</b> member set to AF_INET and the <b>sin_addr</b> member filled with zeros (0.0.0.0). The <b>sin_port</b> member can be any valid port.


## -remarks



 The <b>HTTP_SERVICE_CONFIG_SSL_CCS_KEY</b> structure appears in the <a href="https://msdn.microsoft.com/BA815FB7-4A9F-4917-89E7-3CD108E1CEE3">HTTP_SERVICE_CONFIG_SSL_CCS_SET</a> and the <a href="https://msdn.microsoft.com/E7578D74-E8BE-472D-A01B-51BBA511F561">HTTP_SERVICE_CONFIG_SSL_CCS_QUERY</a> structures. <b>HTTP_SERVICE_CONFIG_SSL_CCS_KEY</b> is passed as part of these structures in the <i>pConfigInformation</i>, <i>ConfigInfo</i>, <i>pInputConfigInfo</i>, and <i>pOutputConfigInfo</i> parameters to the <a href="https://msdn.microsoft.com/0ae94936-4c6a-4c9f-adb8-5e3af75cf486">HttpDeleteServiceConfiguration</a>, <a href="https://msdn.microsoft.com/bbd2c3c4-d2d0-4590-9b5c-6916b91600cd">HttpQueryServiceConfiguration</a>, <a href="https://msdn.microsoft.com/b0a6d442-2ff4-4e00-8301-696fb0864d8c">HttpSetServiceConfiguration</a>, and <a href="https://msdn.microsoft.com/B2102444-1183-4133-A83F-A58587FB6B89">HttpUpdateServiceConfiguration</a> functions when the <i>ConfigId</i> parameter is set to <b>HttpServiceConfigSslCcsCertInfo</b>.





## -see-also




<a href="https://msdn.microsoft.com/E7578D74-E8BE-472D-A01B-51BBA511F561">HTTP_SERVICE_CONFIG_SSL_CCS_QUERY</a>



<a href="https://msdn.microsoft.com/BA815FB7-4A9F-4917-89E7-3CD108E1CEE3">HTTP_SERVICE_CONFIG_SSL_CCS_SET</a>



<a href="https://msdn.microsoft.com/0ae94936-4c6a-4c9f-adb8-5e3af75cf486">HttpDeleteServiceConfiguration</a>



<a href="https://msdn.microsoft.com/bbd2c3c4-d2d0-4590-9b5c-6916b91600cd">HttpQueryServiceConfiguration</a>



<a href="https://msdn.microsoft.com/b0a6d442-2ff4-4e00-8301-696fb0864d8c">HttpSetServiceConfiguration</a>



<a href="https://msdn.microsoft.com/B2102444-1183-4133-A83F-A58587FB6B89">HttpUpdateServiceConfiguration</a>
 

 

