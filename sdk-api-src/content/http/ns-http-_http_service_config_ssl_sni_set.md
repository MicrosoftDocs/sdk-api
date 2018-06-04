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

# _HTTP_SERVICE_CONFIG_SSL_SNI_SET structure


## -description


The 
<b>HTTP_SERVICE_CONFIG_SSL_SNI_SET</b> structure is used to add a new Secure Sockets Layer (SSL) Server Name Indication (SNI) certificate record to the SSL SNI store or retrieve an existing record from it. It is passed to the 
<a href="https://msdn.microsoft.com/b0a6d442-2ff4-4e00-8301-696fb0864d8c">HttpSetServiceConfiguration</a> function through the <i>pConfigInformation</i> parameter or to retrieve data from the 
<a href="https://msdn.microsoft.com/bbd2c3c4-d2d0-4590-9b5c-6916b91600cd">HttpQueryServiceConfiguration</a> function through the <i>pOutputConfigInformation</i> parameter when the <i>ConfigId</i> parameter of either function is set to <b>HttpServiceConfigSslSniCertInfo</b>.


## -struct-fields




### -field KeyDesc

An <a href="https://msdn.microsoft.com/0EABB454-B4B9-4912-8E81-7930164B12F2">HTTP_SERVICE_CONFIG_SSL_SNI_KEY</a> structure that identifies the SSL SNI certificate record.


### -field ParamDesc

An <a href="https://msdn.microsoft.com/2bb3bfe0-9bac-4eb5-80b1-c883503a30b3">HTTP_SERVICE_CONFIG_SSL_PARAM</a> structure that holds the contents of the specified SSL SNI certificate record.


## -see-also




<a href="https://msdn.microsoft.com/0EABB454-B4B9-4912-8E81-7930164B12F2">HTTP_SERVICE_CONFIG_SSL_SNI_KEY</a>



<a href="https://msdn.microsoft.com/9C45B1B1-5572-4153-BBA4-0E8A52F650CA">HTTP_SERVICE_CONFIG_SSL_SNI_QUERY</a>



<a href="https://msdn.microsoft.com/0ae94936-4c6a-4c9f-adb8-5e3af75cf486">HttpDeleteServiceConfiguration</a>



<a href="https://msdn.microsoft.com/bbd2c3c4-d2d0-4590-9b5c-6916b91600cd">HttpQueryServiceConfiguration</a>



<a href="https://msdn.microsoft.com/b0a6d442-2ff4-4e00-8301-696fb0864d8c">HttpSetServiceConfiguration</a>
 

 

