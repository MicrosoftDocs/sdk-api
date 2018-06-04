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

# MI_Context_NewDynamicInstance function


## -description


Creates a new dynamic instance (weakly typed instance without a class declaration) of a class.


## -parameters




### -param context [in]

A pointer to the request context.


### -param className [in]

The name of the new class.


### -param flags

The create flags (include class meta type).


### -param instance

A pointer to a new instance upon successful return.


## -returns



This function returns MI_INLINE MI_Result MI_INLINE_CALL.




## -remarks



To add elements, call the <a href="https://msdn.microsoft.com/51a26894-f391-4281-9e06-2e70fb662aa2">MI_Instance_AddElement</a> function. When you have finished using the instance, delete it with the <a href="https://msdn.microsoft.com/6370e464-b262-4c91-a3c8-889911df7965">MI_Instance_Delete</a> function.




## -see-also




<a href="https://msdn.microsoft.com/51a26894-f391-4281-9e06-2e70fb662aa2">MI_Instance_AddElement</a>



<a href="https://msdn.microsoft.com/6370e464-b262-4c91-a3c8-889911df7965">MI_Instance_Delete</a>
 

 

