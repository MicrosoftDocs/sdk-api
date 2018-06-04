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

# CoEnableCallCancellation function


## -description


Enables cancellation of synchronous calls on the calling thread.


## -parameters




### -param pReserved [in, optional]

This parameter is reserved and must be <b>NULL</b>.


## -returns



This function can return the standard return values S_OK, E_FAIL, E_INVALIDARG, and E_OUTOFMEMORY.




## -remarks



When call cancellation is enabled on a thread, marshaled synchronous calls from that thread to objects on the same computer can suffer serious performance degradation. By default, synchronous calls cannot be canceled, even if a cancel object is available. To enable call cancellation, you must call <b>CoEnableCallCancellation</b> first.

Unless you want to enable call cancellation on a thread at all times, you should pair calls to <b>CoEnableCallCancellation</b> with calls to <a href="https://msdn.microsoft.com/33d99eab-a0bf-4e4d-93a4-5c03c41cebbb">CoDisableCallCancellation</a>. Call cancellation is disabled only if <b>CoDisableCallCancellation</b> has been called once for each time <b>CoEnableCallCancellation</b> was called successfully.

A call will be cancelable or not depending on the state of the thread at the time the call was made. Subsequently enabling or disabling call cancellation has no effect on any calls that are pending on the thread.




## -see-also




<a href="https://msdn.microsoft.com/59b66f33-486e-49c3-9fb8-0eab93146ed9">CoEnableCallCancellation</a>



<a href="https://msdn.microsoft.com/5e31f706-1c9c-4510-845c-4e47093780a1">ICancelMethodCalls</a>
 

 

