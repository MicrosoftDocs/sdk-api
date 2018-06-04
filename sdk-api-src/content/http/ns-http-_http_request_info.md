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

# _HTTP_REQUEST_INFO structure


## -description


The <b>HTTP_REQUEST_INFO</b> structure extends the <a href="https://msdn.microsoft.com/e592cf54-df6d-472b-a736-c44a5ccdd3d2">HTTP_REQUEST</a> structure with additional information about the request.


## -struct-fields




### -field InfoType

A member of the <a href="https://msdn.microsoft.com/178d2608-85c8-4842-bd6a-4c66d7f1b892">HTTP_REQUEST_INFO_TYPE</a> enumeration specifying the type of information contained in this structure.


### -field InfoLength

The length, in bytes,  of the <b>pInfo</b> member.


### -field pInfo

A pointer to the <a href="https://msdn.microsoft.com/07008290-5277-4ef4-ae55-d335fdb2ba90">HTTP_REQUEST_AUTH_INFO</a> structure when the <b>InfoType</b> member is <b>HttpRequestInfoTypeAuth</b>; otherwise <b>NULL</b>.


## -remarks



Starting with the HTTP Server API version 2.0, the HTTP_REQUEST structure is extended to include an array of <b>HTTP_REQUEST_INFO</b> structures in the <b>pRequestInfo</b> member. These structures contain additional information for the  request.




## -see-also




<a href="https://msdn.microsoft.com/5a8e28e9-f85b-4550-929e-53f38eca6a8c">HTTP Server API Version 2.0 Structures</a>



<a href="https://msdn.microsoft.com/07008290-5277-4ef4-ae55-d335fdb2ba90">HTTP_REQUEST_AUTH_INFO</a>



<a href="https://msdn.microsoft.com/02ac6f4f-ca54-42d5-9acb-5a1e81b2cb1c">HTTP_REQUEST_V2</a>
 

 

