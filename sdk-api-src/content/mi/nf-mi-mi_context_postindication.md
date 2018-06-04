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

# MI_Context_PostIndication function


## -description


Posts an indication result to the server in response to a subscribe operation request.


## -parameters




### -param context [in]

Request context.


### -param indication [in]

Indication instance to be posted.


### -param subscriptionIDCount

Number of subscription identifiers.


### -param bookmark

An optional, null-terminated string that represents the bookmark for this subscription. In general, if a bookmark was supplied to the subscribe operation, and bookmarks are supported, a resume bookmark should be returned with every indication.


## -returns



This function returns MI_INLINE MI_Result MI_INLINE_CALL.




## -remarks



There will be posting functions automatically generated for the indication class (for example, className_Post).

The server is responsible for copying the instance so the provider is free to dispose of the instance afterwards using the <a href="https://msdn.microsoft.com/6370e464-b262-4c91-a3c8-889911df7965">MI_Instance_Delete</a> function.




## -see-also




<a href="https://msdn.microsoft.com/51d6c510-f9fd-4ab7-a669-b2a5776b496d">MI_Context</a>



<a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a>



<a href="https://msdn.microsoft.com/6370e464-b262-4c91-a3c8-889911df7965">MI_Instance_Delete</a>
 

 

