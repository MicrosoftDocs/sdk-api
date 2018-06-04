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

# CoInitialize function


## -description


Initializes the COM library on the current thread and identifies the concurrency model as single-thread apartment (STA).

New applications should call <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a> instead of CoInitialize. 

If you want to use the Windows Runtime, you must call Windows::Foundation::Initialize instead.


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
A previous call to <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a> specified the concurrency model for this thread as multithread apartment (MTA). This could also indicate that a change from neutral-threaded apartment to single-threaded apartment has occurred.

</td>
</tr>
</table>
 




## -remarks



You need to initialize the COM library on a thread before you call any of the library functions except <a href="https://msdn.microsoft.com/d1d09fbe-ca5c-4480-b807-3afcc043ccb9">CoGetMalloc</a>, to get a pointer to the standard allocator, and the memory allocation functions.



After the concurrency model for a thread is set, it cannot be changed. A call to <b>CoInitialize</b> on an apartment that was previously initialized as multithreaded will fail and return RPC_E_CHANGED_MODE. 




<a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a> provides the same functionality as <b>CoInitialize</b> and also provides a parameter to explicitly specify the thread's concurrency model. <b>CoInitialize</b> calls <b>CoInitializeEx</b> and specifies the concurrency model as single-thread apartment. Applications developed today should call <b>CoInitializeEx</b> rather than <b>CoInitialize</b>. 



Typically, the COM library is initialized on a thread only once. Subsequent calls to <b>CoInitialize</b> or <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a> on the same thread will succeed, as long as they do not attempt to change the concurrency model, but will return S_FALSE. To close the COM library gracefully, each successful call to <b>CoInitialize</b> or <b>CoInitializeEx</b>, including those that return S_FALSE, must be balanced by a corresponding call to <a href="https://msdn.microsoft.com/9411cbed-fa3b-46f7-b677-6ada53324edc">CoUninitialize</a>. However, the first thread in the application that calls <b>CoInitialize</b> with 0 (or <b>CoInitializeEx</b> with COINIT_APARTMENTTHREADED) must be the last thread to call <b>CoUninitialize</b>. Otherwise, subsequent calls to <b>CoInitialize</b> on the STA will fail and the application will not work.

Because there is no way to control the order in which in-process servers are loaded or unloaded, do not call <b>CoInitialize</b>, <a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a>, or <a href="https://msdn.microsoft.com/9411cbed-fa3b-46f7-b677-6ada53324edc">CoUninitialize</a> from the <a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a> function.




## -see-also




<a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a>
 

 

