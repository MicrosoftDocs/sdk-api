---
UID: NF:combaseapi.CoEnableCallCancellation
title: CoEnableCallCancellation function
author: windows-sdk-content
description: Enables cancellation of synchronous calls on the calling thread.
old-location: com\coenablecallcancellation.htm
tech.root: com
ms.assetid: 59b66f33-486e-49c3-9fb8-0eab93146ed9
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CoEnableCallCancellation, CoEnableCallCancellation function [COM], _com_CoEnableCallCancellation, com.coenablecallcancellation, combaseapi/CoEnableCallCancellation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoEnableCallCancellation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

