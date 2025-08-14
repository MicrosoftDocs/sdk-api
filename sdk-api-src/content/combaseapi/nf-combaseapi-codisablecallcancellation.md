---
UID: NF:combaseapi.CoDisableCallCancellation
title: CoDisableCallCancellation function (combaseapi.h)
description: Undoes the action of a call to CoEnableCallCancellation. Disables cancellation of synchronous calls on the calling thread when all calls to CoEnableCallCancellation are balanced by calls to CoDisableCallCancellation.
helpviewer_keywords: ["CoDisableCallCancellation","CoDisableCallCancellation function [COM]","_com_CoDisableCallCancellation","com.codisablecallcancellation","combaseapi/CoDisableCallCancellation"]
old-location: com\codisablecallcancellation.htm
tech.root: com
ms.assetid: 33d99eab-a0bf-4e4d-93a4-5c03c41cebbb
ms.date: 12/05/2018
ms.keywords: CoDisableCallCancellation, CoDisableCallCancellation function [COM], _com_CoDisableCallCancellation, com.codisablecallcancellation, combaseapi/CoDisableCallCancellation
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoDisableCallCancellation
 - combaseapi/CoDisableCallCancellation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-ole32-l1-1-0.dll
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoDisableCallCancellation
---

# CoDisableCallCancellation function


## -description

Undoes the action of a call to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coenablecallcancellation">CoEnableCallCancellation</a>. Disables cancellation of synchronous calls on the calling thread when all calls to <b>CoEnableCallCancellation</b> are balanced by calls to <b>CoDisableCallCancellation</b>.

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
There have been more successful calls to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coenablecallcancellation">CoEnableCallCancellation</a> on the thread than there have been calls to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-codisablecallcancellation">CoDisableCallCancellation</a>. Cancellation is still enabled on the thread.

</td>
</tr>
</table>

## -remarks

When call cancellation is enabled on a thread, marshaled synchronous calls from that thread to objects on the same computer can suffer serious performance degradation. By default, then, synchronous calls cannot be canceled, even if a cancel object is available. To enable call cancellation, you must call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coenablecallcancellation">CoEnableCallCancellation</a> first. 



When call cancellation is disabled, attempts to gain a pointer to a call object will fail. If the calling thread already has a pointer to a call object, calls on that object will fail.

Unless you want to enable call cancellation on a thread at all times, you should pair calls to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coenablecallcancellation">CoEnableCallCancellation</a> with calls to <b>CoDisableCallCancellation</b>. Call cancellation is disabled only if each successful call to <b>CoEnableCallCancellation</b> is balanced by a successful call to <b>CoDisableCallCancellation</b>. 



A call will be cancelable or not depending on the state of the thread at the time the call was made. Subsequently enabling or disabling call cancellation has no effect on any calls that are pending on the thread.

If a thread is uninitialized and then reinitialized by calls to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize">CoUninitialize</a> and <a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a>, call cancellation is disabled on the thread, even if it was enabled when the thread was uninitialized.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coenablecallcancellation">CoEnableCallCancellation</a>



<a href="/windows/desktop/api/objidl/nn-objidl-icancelmethodcalls">ICancelMethodCalls</a>