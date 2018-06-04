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

# RpcRaiseException function


## -description


Use the 
<b>RpcRaiseException</b> function to raise an exception. The function does not return to the caller.


## -parameters




### -param exception

TBD




#### - Exception

Exception code for the exception.


## -returns



This function does not return a value.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



<b>RpcRaiseException</b> raises an exception. The exception handler can then handle the exception. For more information about handling exceptions, see 
<a href="https://msdn.microsoft.com/4882d29b-08f3-41ec-84c3-35df6c56fd31">Making RPC Function Calls</a>.




## -see-also




<a href="https://msdn.microsoft.com/6025da80-d334-4abd-9d7c-6cce139cd4d7">RpcAbnormalTermination</a>



<a href="https://msdn.microsoft.com/5bd57250-1fd7-4aeb-aa53-4fd2c8d84836">RpcExcept</a>



<a href="https://msdn.microsoft.com/332641ea-748f-47e5-bb0e-33d2bf4e04c9">RpcFinally</a>
 

 

