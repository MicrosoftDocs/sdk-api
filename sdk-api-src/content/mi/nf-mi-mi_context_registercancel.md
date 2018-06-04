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

# MI_Context_RegisterCancel function


## -description


Registers a callback that is invoked when the operation is canceled.


## -parameters




### -param context [in]

Request context.


### -param callback [in]

Function that will be called if the operation is canceled.


### -param callbackData [in, optional]

Data to be passed to the callback.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



If a provider calls this function multiple times on the same context, only the last callback function will be called. Not all operations canceled on the client will reach the provider. If this is an operation that cannot register the cancellation callback, the function will return an error. This would mean the operation will run to completion. If the operation runs through to completion, the callback function will not be called.




## -see-also




<a href="https://msdn.microsoft.com/f2296852-ac09-447c-8088-5639f1e48efd">MI_CancelCallback</a>



<a href="https://msdn.microsoft.com/3c498055-03ef-4163-9de5-cf4e70051cea">MI_CancellationReason</a>



<a href="https://msdn.microsoft.com/51d6c510-f9fd-4ab7-a669-b2a5776b496d">MI_Context</a>
 

 

