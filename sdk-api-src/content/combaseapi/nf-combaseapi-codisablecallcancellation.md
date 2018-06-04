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

# CoDisableCallCancellation function


## -description


Undoes the action of a call to <a href="https://msdn.microsoft.com/59b66f33-486e-49c3-9fb8-0eab93146ed9">CoEnableCallCancellation</a>. Disables cancellation of synchronous calls on the calling thread when all calls to <b>CoEnableCallCancellation</b> are balanced by calls to <b>CoDisableCallCancellation</b>.


## -parameters




### -param pReserved [in, optional]

This parameter is reserved and must be <b>NULL</b>.


## -returns



This function can return the standard return values E_FAIL, E_INVALIDARG, E_OUTOFMEMORY, and E_UNEXPECTED, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Call cancellation was successfully disabled on the thread.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_CANCEL_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
There have been more successful calls to <a href="https://msdn.microsoft.com/59b66f33-486e-49c3-9fb8-0eab93146ed9">CoEnableCallCancellation</a> on the thread than there have been calls to <a href="https://msdn.microsoft.com/33d99eab-a0bf-4e4d-93a4-5c03c41cebbb">CoDisableCallCancellation</a>. Cancellation is still enabled on the thread.

</td>
</tr>
</table>
 




## -remarks



When call cancellation is enabled on a thread, marshaled synchronous calls from that thread to objects on the same computer can suffer serious performance degradation. By default, then, synchronous calls cannot be canceled, even if a cancel object is available. To enable call cancellation, you must call <a href="https://msdn.microsoft.com/59b66f33-486e-49c3-9fb8-0eab93146ed9">CoEnableCallCancellation</a> first. 



When call cancellation is disabled, attempts to gain a pointer to a call object will fail. If the calling thread already has a pointer to a call object, calls on that object will fail.

Unless you want to enable call cancellation on a thread at all times, you should pair calls to <a href="https://msdn.microsoft.com/59b66f33-486e-49c3-9fb8-0eab93146ed9">CoEnableCallCancellation</a> with calls to <b>CoDisableCallCancellation</b>. Call cancellation is disabled only if each successful call to <b>CoEnableCallCancellation</b> is balanced by a successful call to <b>CoDisableCallCancellation</b>. 



A call will be cancelable or not depending on the state of the thread at the time the call was made. Subsequently enabling or disabling call cancellation has no effect on any calls that are pending on the thread.

If a thread is uninitialized and then reinitialized by calls to <a href="https://msdn.microsoft.com/9411cbed-fa3b-46f7-b677-6ada53324edc">CoUninitialize</a> and <a href="https://msdn.microsoft.com/0f171cf4-87b9-43a6-97f2-80ed344fe376">CoInitialize</a>, call cancellation is disabled on the thread, even if it was enabled when the thread was uninitialized.




## -see-also




<a href="https://msdn.microsoft.com/59b66f33-486e-49c3-9fb8-0eab93146ed9">CoEnableCallCancellation</a>



<a href="https://msdn.microsoft.com/5e31f706-1c9c-4510-845c-4e47093780a1">ICancelMethodCalls</a>
 

 

