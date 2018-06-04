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

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff570825">SOCKADDR_STORAGE</a> structure that contains the Internet Protocol version 4 (IPv4) address with which this SSL SNI certificate is associated. It must be set to the IPv4 wildcard address of type <b>SOCKADDR_IN</b> with <b>ss_family</b> set to <b>AF_INET</b> and <b>sin_addr</b> filled with zeros. <b>Port</b> can be any valid port.


### -field Host

A pointer to a null-terminated Unicode UTF-16 string that represents the hostname. 


## -see-also




<a href="https://msdn.microsoft.com/9C45B1B1-5572-4153-BBA4-0E8A52F650CA">HTTP_SERVICE_CONFIG_SSL_SNI_QUERY</a>



<a href="https://msdn.microsoft.com/382838B9-C15E-459F-AC40-ECA15EFC18B8">HTTP_SERVICE_CONFIG_SSL_SNI_SET</a>



<a href="https://msdn.microsoft.com/0ae94936-4c6a-4c9f-adb8-5e3af75cf486">HttpDeleteServiceConfiguration</a>



<a href="https://msdn.microsoft.com/bbd2c3c4-d2d0-4590-9b5c-6916b91600cd">HttpQueryServiceConfiguration</a>



<a href="https://msdn.microsoft.com/b0a6d442-2ff4-4e00-8301-696fb0864d8c">HttpSetServiceConfiguration</a>
 

 

