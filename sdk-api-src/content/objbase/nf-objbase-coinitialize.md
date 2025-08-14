---
UID: NF:objbase.CoInitialize
title: CoInitialize function (objbase.h)
description: Initializes the COM library on the current thread and identifies the concurrency model as single-thread apartment (STA).
helpviewer_keywords: ["CoInitialize","CoInitialize function [COM]","_com_CoInitialize","com.coinitialize","objbase/CoInitialize"]
old-location: com\coinitialize.htm
tech.root: com
ms.assetid: 0f171cf4-87b9-43a6-97f2-80ed344fe376
ms.date: 12/05/2018
ms.keywords: CoInitialize, CoInitialize function [COM], _com_CoInitialize, com.coinitialize, objbase/CoInitialize
req.header: objbase.h
req.include-header: 
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
 - CoInitialize
 - objbase/CoInitialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-com-ole32-l1-3-0.dll
 - ext-ms-win-com-ole32-l1-2-0.dll
 - ext-ms-win-com-ole32-l1-1-5.dll
 - Ole32.dll
 - API-MS-Win-OLE32-IE-l1-1-0.dll
 - ole32_wp.dll
 - Ext-MS-Win-COM-OLE32-l1-1-1.dll
 - Ext-MS-Win-COM-OLE32-l1-1-2.dll
 - ext-ms-win-com-ole32-l1-1-3.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - CoInitialize
req.apiset: ext-ms-win-com-sta-l1-1-0 (introduced in Windows 10, version 10.0.20166)
---

# CoInitialize function


## -description

Initializes the COM library on the current thread and identifies the concurrency model as single-thread apartment (STA).

New applications should call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a> instead of CoInitialize. 

If you want to use the Windows Runtime, you must call <a href="/windows/win32/api/roapi/nf-roapi-roinitialize">RoInitialize</a> or <a href="/windows/win32/api/roapi/nf-roapi-initialize">Windows::Foundation::Initialize</a> instead.

## -parameters

### -param pvReserved [in, optional]

This parameter is reserved and must be <b>NULL</b>.

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
A previous call to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a> specified the concurrency model for this thread as multithread apartment (MTA). This could also indicate that a change from neutral-threaded apartment to single-threaded apartment has occurred.

</td>
</tr>
</table>

## -remarks

You need to initialize the COM library on a thread before you call any of the library functions except <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc">CoGetMalloc</a>, to get a pointer to the standard allocator, and the memory allocation functions.



After the concurrency model for a thread is set, it cannot be changed. A call to <b>CoInitialize</b> on an apartment that was previously initialized as multithreaded will fail and return RPC_E_CHANGED_MODE. 




<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a> provides the same functionality as <b>CoInitialize</b> and also provides a parameter to explicitly specify the thread's concurrency model. <b>CoInitialize</b> calls <b>CoInitializeEx</b> and specifies the concurrency model as single-thread apartment. Applications developed today should call <b>CoInitializeEx</b> rather than <b>CoInitialize</b>. 



Typically, the COM library is initialized on a thread only once. Subsequent calls to <b>CoInitialize</b> or <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a> on the same thread will succeed, as long as they do not attempt to change the concurrency model, but will return S_FALSE. To close the COM library gracefully, each successful call to <b>CoInitialize</b> or <b>CoInitializeEx</b>, including those that return S_FALSE, must be balanced by a corresponding call to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize">CoUninitialize</a>. However, the first thread in the application that calls <b>CoInitialize</b> with 0 (or <b>CoInitializeEx</b> with COINIT_APARTMENTTHREADED) must be the last thread to call <b>CoUninitialize</b>. Otherwise, subsequent calls to <b>CoInitialize</b> on the STA will fail and the application will not work.

Because there is no way to control the order in which in-process servers are loaded or unloaded, do not call <b>CoInitialize</b>, <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a>, or <a href="/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize">CoUninitialize</a> from the <a href="/windows/desktop/Dlls/dllmain">DllMain</a> function.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex">CoInitializeEx</a>
