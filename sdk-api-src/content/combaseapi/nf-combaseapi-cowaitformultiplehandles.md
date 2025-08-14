---
UID: NF:combaseapi.CoWaitForMultipleHandles
title: CoWaitForMultipleHandles function (combaseapi.h)
description: Waits for specified handles to be signaled or for a specified timeout period to elapse.
helpviewer_keywords: ["CoWaitForMultipleHandles","CoWaitForMultipleHandles function [COM]","_com_CoWaitForMultipleHandles","com.cowaitformultiplehandles","combaseapi/CoWaitForMultipleHandles"]
old-location: com\cowaitformultiplehandles.htm
tech.root: com
ms.assetid: 3eeecd34-aa94-4a48-8b41-167a71b52860
ms.date: 12/05/2018
ms.keywords: CoWaitForMultipleHandles, CoWaitForMultipleHandles function [COM], _com_CoWaitForMultipleHandles, com.cowaitformultiplehandles, combaseapi/CoWaitForMultipleHandles
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
 - CoWaitForMultipleHandles
 - combaseapi/CoWaitForMultipleHandles
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoWaitForMultipleHandles
---

# CoWaitForMultipleHandles function


## -description

Waits for specified handles to be signaled or for a specified timeout period to elapse.

## -parameters

### -param dwFlags [in]

The wait options. Possible values are taken from the <a href="/windows/desktop/api/combaseapi/ne-combaseapi-cowait_flags">COWAIT_FLAGS</a> enumeration.

### -param dwTimeout [in]

The timeout period, in milliseconds.

### -param cHandles [in]

The number of elements in the <i>pHandles</i> array.

### -param pHandles [in]

An array of handles.

### -param lpdwindex [out]

A pointer to a variable that, when the returned status is S_OK, receives a value indicating the event that caused the function to return. This value is usually the index into <i>pHandles</i> for the handle that was signaled.

If <i>pHandles</i> includes one or more handles to mutex objects, a value between WAIT_ABANDONED_0 and (WAIT_ABANDONED_0 + nCount - 1) indicates the index into <i>pHandles</i> for the mutex that was abandoned.

If the <a href="/windows/desktop/api/combaseapi/ne-combaseapi-cowait_flags">COWAIT_ALERTABLE</a> flag is set in <i>dwFlags</i>, a value of WAIT_IO_COMPLETION indicates the wait was ended by one or more user-mode asynchronous procedure calls (APC) queued to the thread.

See <a href="/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex">WaitForMultipleObjectsEx</a> for more information.

## -returns

This function can return the following values.

<div class="alert"><b>Note</b>  The return value of <b>CoWaitForMultipleHandles</b> can be nondeterministic if the <a href="/windows/desktop/api/combaseapi/ne-combaseapi-cowait_flags">COWAIT_ALERTABLE</a> flag is set in <i>dwFlags</i>, or if <i>pHandles</i> includes one or more handles to mutex objects. The recommended workaround is to call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError(ERROR_SUCCESS)</a> before <b>CoWaitForMultipleHandles</b>.</div>
<div> </div>
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
The required handle or handles were signaled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pHandles</i> was <b>NULL</b>, <i>lpdwindex</i> was <b>NULL</b>, or <i>dwFlags</i> was not a value from the <a href="/windows/desktop/api/combaseapi/ne-combaseapi-cowait_flags">COWAIT_FLAGS</a> enumeration.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_E_NO_SYNC</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>pHandles</i> was 0.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_CALLPENDING</b></dt>
</dl>
</td>
<td width="60%">
The timeout period elapsed before the required handle or handles were signaled.

</td>
</tr>
</table>

## -remarks

Depending on which flags are set in the dwFlags parameter, <b>CoWaitForMultipleHandles</b> blocks the calling thread until one of the following events occurs: 



<ul>
<li>One or all of the handles is signaled. In the case of mutex objects, this condition is also satisfied by a mutex being abandoned.</li>
<li>An asynchronous procedure call (APC) has been queued to the calling thread with a call to the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc">QueueUserAPC</a> function.</li>
<li>The timeout period expires.</li>
</ul>
If the caller resides in a single-thread apartment, <b>CoWaitForMultipleHandles</b> enters the COM modal loop, and the thread's message loop will continue to dispatch messages using the thread's message filter. If no message filter is registered for the thread, the default COM message processing is used.

If the calling thread resides in a multithread apartment (MTA), <b>CoWaitForMultipleHandles</b> calls the  <a href="/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex">WaitForMultipleObjectsEx</a> function.

## -see-also

<a href="/windows/desktop/api/combaseapi/ne-combaseapi-cowait_flags">COWAIT_FLAGS</a>