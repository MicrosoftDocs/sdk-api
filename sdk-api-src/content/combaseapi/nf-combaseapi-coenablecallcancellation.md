---
UID: NF:combaseapi.CoEnableCallCancellation
title: CoEnableCallCancellation function (combaseapi.h)
author: windows-sdk-content
description: Enables cancellation of synchronous calls on the calling thread.
old-location: com\coenablecallcancellation.htm
tech.root: com
ms.assetid: 59b66f33-486e-49c3-9fb8-0eab93146ed9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CoEnableCallCancellation, CoEnableCallCancellation function [COM], _com_CoEnableCallCancellation, com.coenablecallcancellation, combaseapi/CoEnableCallCancellation
ms.topic: function
f1_keywords: 
 - "combaseapi/CoEnableCallCancellation"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

Unless you want to enable call cancellation on a thread at all times, you should pair calls to <b>CoEnableCallCancellation</b> with calls to <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-codisablecallcancellation">CoDisableCallCancellation</a>. Call cancellation is disabled only if <b>CoDisableCallCancellation</b> has been called once for each time <b>CoEnableCallCancellation</b> was called successfully.

A call will be cancelable or not depending on the state of the thread at the time the call was made. Subsequently enabling or disabling call cancellation has no effect on any calls that are pending on the thread.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-coenablecallcancellation">CoEnableCallCancellation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-icancelmethodcalls">ICancelMethodCalls</a>
 

 

