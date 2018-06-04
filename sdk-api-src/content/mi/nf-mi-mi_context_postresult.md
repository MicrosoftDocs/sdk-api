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

# MI_Context_PostResult function


## -description


Posts the final terminating result code back to the client (through the server) in response to a request.


## -parameters




### -param context [in]

Request context.


### -param result

Result code to post to the server.


## -returns



This function returns MI_INLINE MI_Result MI_INLINE_CALL.




## -remarks



All calls to the <a href="https://msdn.microsoft.com/1e7fb986-0896-44cb-9b19-e3576911058c">MI_Context_PostIndication</a> and <a href="https://msdn.microsoft.com/b7c5e677-5b49-48b8-8273-4fd04c2f4a90">MI_Context_PostInstance</a> functions must be complete before calling this function. When this function is called, the lifetime of the request context is terminated; the context becomes invalid, and no additional calls can be made on the context.




## -see-also




<a href="https://msdn.microsoft.com/51d6c510-f9fd-4ab7-a669-b2a5776b496d">MI_Context</a>



<a href="https://msdn.microsoft.com/1e7fb986-0896-44cb-9b19-e3576911058c">MI_Context_PostIndication</a>



<a href="https://msdn.microsoft.com/b7c5e677-5b49-48b8-8273-4fd04c2f4a90">MI_Context_PostInstance</a>
 

 

