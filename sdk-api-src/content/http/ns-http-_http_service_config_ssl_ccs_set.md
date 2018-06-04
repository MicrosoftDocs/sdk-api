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

# _HTTP_SERVICE_CONFIG_SSL_CCS_SET structure


## -description


Represents the   SSL certificate record that specifies that Http.sys should consult the Centralized Certificate Store (CCS) store to find certificates if the port receives a Transport Layer Security (TLS) handshake.   Use this structure to add, delete, retrieve, or update that SSL certificate.


## -struct-fields




### -field KeyDesc

An <a href="https://msdn.microsoft.com/C40070D6-AE19-4E42-A7C6-38F8AF5C1F53">HTTP_SERVICE_CONFIG_SSL_CCS_KEY</a> structure that identifies the SSL CCS certificate record.


### -field ParamDesc

An <a href="https://msdn.microsoft.com/2bb3bfe0-9bac-4eb5-80b1-c883503a30b3">HTTP_SERVICE_CONFIG_SSL_PARAM</a> structure that holds the contents of the specified SSL CCS certificate record.


## -remarks



Pass this structure to the <a href="https://msdn.microsoft.com/b0a6d442-2ff4-4e00-8301-696fb0864d8c">HttpSetServiceConfiguration</a> or <a href="https://msdn.microsoft.com/0ae94936-4c6a-4c9f-adb8-5e3af75cf486">HttpDeleteServiceConfiguration</a> function through the <i>pConfigInformation</i> parameter to add or remove an SSL certificate record. Pass this structure to the <a href="https://msdn.microsoft.com/B2102444-1183-4133-A83F-A58587FB6B89">HttpUpdateServiceConfiguration</a> function through the <i>ConfigInfo</i> parameter to update an SSL certificate record.  Use  the <i>pOutputConfigInfo</i> parameter of the <a href="https://msdn.microsoft.com/bbd2c3c4-d2d0-4590-9b5c-6916b91600cd">HttpQueryServiceConfiguration</a> function to retrieve SSL certificate record data in this structure. For all of these operations, set the <i>ConfigId</i> parameter of these functions to <b>HttpServiceConfigSslCcsCertInfo</b>.




## -see-also




<a href="https://msdn.microsoft.com/C40070D6-AE19-4E42-A7C6-38F8AF5C1F53">HTTP_SERVICE_CONFIG_SSL_CCS_KEY</a>



<a href="https://msdn.microsoft.com/2bb3bfe0-9bac-4eb5-80b1-c883503a30b3">HTTP_SERVICE_CONFIG_SSL_PARAM</a>



<a href="https://msdn.microsoft.com/0ae94936-4c6a-4c9f-adb8-5e3af75cf486">HttpDeleteServiceConfiguration</a>



<a href="https://msdn.microsoft.com/bbd2c3c4-d2d0-4590-9b5c-6916b91600cd">HttpQueryServiceConfiguration</a>



<a href="https://msdn.microsoft.com/b0a6d442-2ff4-4e00-8301-696fb0864d8c">HttpSetServiceConfiguration</a>



<a href="https://msdn.microsoft.com/B2102444-1183-4133-A83F-A58587FB6B89">HttpUpdateServiceConfiguration</a>
 

 

