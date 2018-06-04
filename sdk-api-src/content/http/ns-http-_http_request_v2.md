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

# _HTTP_REQUEST_V2 structure


## -description


The <b>HTTP_REQUEST_V2</b> structure extends the <a href="https://msdn.microsoft.com/5550c49c-36ef-42e6-8134-5d9d0d9d53b5">HTTP_REQUEST_V1</a> request structure with more information about the request.

Do not use <b>HTTP_REQUEST_V2</b> directly in your code;  use <a href="https://msdn.microsoft.com/e592cf54-df6d-472b-a736-c44a5ccdd3d2">HTTP_REQUEST</a> instead to ensure that the proper version, based on the operating system the code is compiled under, is used.


## -struct-fields




### -field RequestInfoCount

The number of <a href="https://msdn.microsoft.com/83c2a922-4ddb-4dc0-9ed6-d75d47b97d6a">HTTP_REQUEST_INFO</a> structures in the array pointed to by <b>pRequestInfo</b>.


### -field pRequestInfo

A pointer to an array of <a href="https://msdn.microsoft.com/83c2a922-4ddb-4dc0-9ed6-d75d47b97d6a">HTTP_REQUEST_INFO</a> structures that contains additional information about the request.


### -field _HTTP_REQUEST_V1

 




## -see-also




<a href="https://msdn.microsoft.com/5a8e28e9-f85b-4550-929e-53f38eca6a8c">HTTP Server API Version 2.0 Structures</a>



<a href="https://msdn.microsoft.com/beb31444-4a4b-4d8d-b88b-7d74467c9ca1">HTTP_COOKED_URL</a>



<a href="https://msdn.microsoft.com/ae67c066-c8bd-483f-829f-30192f49593d">HTTP_DATA_CHUNK</a>



<a href="https://msdn.microsoft.com/e592cf54-df6d-472b-a736-c44a5ccdd3d2">HTTP_REQUEST</a>



<a href="https://msdn.microsoft.com/5550c49c-36ef-42e6-8134-5d9d0d9d53b5">HTTP_REQUEST_V1</a>



<a href="https://msdn.microsoft.com/F94646C0-7293-4543-842B-F08D8C7E2247">HTTP_RESPONSE</a>



<a href="https://msdn.microsoft.com/35aac36d-87a1-45b2-acb1-6969c992d0cf">HTTP_SSL_INFO</a>



<a href="https://msdn.microsoft.com/2dac2817-c911-4ca1-afb1-32147a16ad4c">HTTP_TRANSPORT_ADDRESS</a>



<a href="https://msdn.microsoft.com/4aa36eab-eff2-4caa-9bad-15c534c5a5a0">HTTP_VERB</a>



<a href="https://msdn.microsoft.com/ad9e80f7-04c4-4108-a7ab-40eb57d00e3b">HttpReceiveHttpRequest</a>



<a href="https://msdn.microsoft.com/b4ba765f-537b-4021-9ecc-d400d9b94723">HttpReceiveRequestEntityBody</a>



<a href="https://msdn.microsoft.com/0183584f-105e-4fa3-8991-d3f2dfca1d62">HttpSendHttpResponse</a>



<a href="https://msdn.microsoft.com/f2ff2e40-ef1f-4c35-a615-f31ac63ab738">HttpSendResponseEntityBody</a>
 

 

