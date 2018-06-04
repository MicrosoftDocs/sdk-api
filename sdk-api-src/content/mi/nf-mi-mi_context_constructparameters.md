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

# MI_Context_ConstructParameters function


## -description


A provider calls this function to initialize a parameter's instance.


## -parameters




### -param context [in]

A pointer to the request context.


### -param methodDecl [in]

A pointer to the method declaration used to initialize the instance.


### -param instance [out]

A pointer to the returned instance.


## -returns



This function returns MI_INLINE MI_Result MI_INLINE_CALL.




## -remarks



You are responsible for reserving the memory for the instance (either on the stack or the heap). When you have finished using the instance, delete it by calling the <a href="https://msdn.microsoft.com/2ecbf165-0918-489c-8e70-b48c31263aed">MI_Instance_Destruct</a> function.



