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

# MI_Context_Canceled function


## -description


Determines whether the operation has been canceled. This function is reserved; instead, use the <a href="https://msdn.microsoft.com/7e6b2016-6ce5-4dcd-b5f4-6e6d24c46f0a">MI_Context_RegisterCancel</a> function.


## -parameters




### -param context [in]

A pointer to the request context that was passed to the provider method.


### -param flag [out]

A pointer to a flag that holds the deletion result. Upon return, this flag will be <b>MI_TRUE</b> if the operation has been successfully canceled; 
     otherwise, it will be <b>MI_FALSE</b>.


## -returns



This function returns MI_INLINE MI_Result MI_INLINE_CALL.




## -remarks



A canceled operation on the client does not always signal to the server that the operation should be canceled. It depends on both the type of operation and the support from the underlying protocol handler.



