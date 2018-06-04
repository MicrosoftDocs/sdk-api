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

# MI_Context_PostCimError function


## -description


Posts a return code and an error message (in the form of a <a href="https://msdn.microsoft.com/a7dc450d-7dbd-4097-a186-0e42f100fbfe">CIM_Error</a> object) to the server in response to a request.


## -parameters




### -param context [in]

A pointer to the request context.


### -param error [in]

A pointer to a <a href="https://msdn.microsoft.com/a7dc450d-7dbd-4097-a186-0e42f100fbfe">CIM_Error</a> object to be posted to the server.


## -returns



This function returns MI_INLINE MI_Result MI_INLINE_CALL.




## -remarks



The <a href="https://msdn.microsoft.com/a7dc450d-7dbd-4097-a186-0e42f100fbfe">CIM_Error</a> instance that is returned in the <i>error</i> parameter can be compiled into your provider so you can initialize and then post it. Once an error has been posted, the context must not be used, as it becomes invalid at this point.




## -see-also




<a href="https://msdn.microsoft.com/a7dc450d-7dbd-4097-a186-0e42f100fbfe">CIM_Error</a>



<a href="https://msdn.microsoft.com/51d6c510-f9fd-4ab7-a669-b2a5776b496d">MI_Context</a>



<a href="https://msdn.microsoft.com/6df0841b-3e13-4f9a-9e54-5c3c0c0d79fe">MI_Context_WriteCimError</a>



<a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a>
 

 

