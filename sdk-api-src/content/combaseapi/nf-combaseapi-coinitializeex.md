---
UID: NF:combaseapi.CoInitializeEx
title: CoInitializeEx function (combaseapi.h)
description: Initializes the COM library for use by the calling thread, sets the thread's concurrency model, and creates a new apartment for the thread if one is required.
helpviewer_keywords: ["CoInitializeEx","CoInitializeEx function [COM]","_com_CoInitializeEx","com.coinitializeex","combaseapi/CoInitializeEx"]
old-location: com\coinitializeex.htm
tech.root: com
ms.assetid: ffb79c0f-aeda-4ea1-aea8-afb79109837f
ms.date: 12/05/2018
ms.keywords: CoInitializeEx, CoInitializeEx function [COM], _com_CoInitializeEx, com.coinitializeex, combaseapi/CoInitializeEx
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - CoInitializeEx
 - combaseapi/CoInitializeEx
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
 - CoInitializeEx
---

# CoInitializeEx function


## -description

Initializes the COM library for use by the calling thread, sets the thread's concurrency model, and creates a new apartment for the thread if one is required.

You should call Windows::Foundation::Initialize to initialize the thread instead of <b>CoInitializeEx</b> if you want to use the Windows Runtime APIs or if you want to use both COM and Windows Runtime components. Windows::Foundation::Initialize is sufficient to use for COM components.

## -parameters

### -param pvReserved [in, optional]

This parameter is reserved and must be <b>NULL</b>.

### -param dwCoInit [in]

The concurrency model and initialization options for the thread. Values for this parameter are taken from the <a href="/windows/desktop/api/objbase/ne-objbase-coinit">COINIT</a> enumeration. Any combination of values from <b>COINIT</b> can be used, except that the COINIT_APARTMENTTHREADED and COINIT_MULTITHREADED flags cannot both be set. The default is COINIT_MULTITHREADED.

## -returns

This function can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and E_UNEXPECTED, as well as the following values.

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
The COM library was initialized successfully on this thread.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The COM library is already initialized on this thread.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_E_CHANGED_MODE</b></dt>
</dl>
</td>
<td width="60%">
A previous call to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a> specified an incompatible concurrency model for this thread. This could also indicate that a change from neutral-threaded apartment to single-threaded apartment has occurred.

</td>
</tr>
</table>

## -remarks

<b>CoInitializeEx</b> must be called at least once, and is usually called only once, for each thread that uses the COM library. Multiple calls to <b>CoInitializeEx</b> by the same thread are allowed as long as they pass the same concurrency flag, but subsequent valid calls return S_FALSE.
If the concurrency flag does not match, then the call fails and returns RPC_E_CHANGED_MODE.
(For the purpose of this rule, a call to <a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a> is equivalent to calling <b>CoInitializeEx</b> with the COINIT_APARTMENTTHREADED flag.)
To uninitialize the COM library gracefully on a thread, each successful call to <a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a> or <b>CoInitializeEx</b>, including any call that returns S_FALSE, must be balanced by a corresponding call to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize">CoUninitialize</a>.
Once COM has been uninitialized on a thread, you can reinitialize it in any mode, subject to the constraints above.

You need to initialize the COM library on a thread before you call any of the library functions except <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc">CoGetMalloc</a>, to get a pointer to the standard allocator, and the memory allocation functions.
Otherwise, the COM function will return CO_E_NOTINITIALIZED.

Objects created in a single-threaded apartment (STA) receive method calls only from their apartment's thread, so calls are serialized and arrive only at message-queue boundaries (when the <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a> or <a href="/previous-versions/windows/desktop/oe/oe-ihttpmailtransport-sendmessage">SendMessage</a> function is called).

Objects created on a COM thread in a multithread apartment (MTA) must be able to receive method calls from other threads at any time. You would typically implement some form of concurrency control in a multithreaded object's code using synchronization primitives such as critical sections, semaphores, or mutexes to help protect the object's data. 

When an object that is configured to run in the neutral threaded apartment (NTA) is called by a thread that is in either an STA or the MTA, that thread transfers to the NTA. If this thread subsequently calls <b>CoInitializeEx</b>, the call fails and returns RPC_E_CHANGED_MODE.

Because OLE technologies are not thread-safe, the <a href="/windows/desktop/api/ole2/nf-ole2-oleinitialize">OleInitialize</a> function calls <b>CoInitializeEx</b> with the COINIT_APARTMENTTHREADED flag. As a result, an apartment that is initialized for multithreaded object concurrency cannot use the features enabled by <b>OleInitialize</b>.



Because there is no way to control the order in which in-process servers are loaded or unloaded, do not call <a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a>, <b>CoInitializeEx</b>, or <a href="/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize">CoUninitialize</a> from the <a href="/windows/desktop/Dlls/dllmain">DllMain</a> function.

## -see-also

<a href="/windows/desktop/com/processes--threads--and-apartments">Processes, Threads, and Apartments</a>