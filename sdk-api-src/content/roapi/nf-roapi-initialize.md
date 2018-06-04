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

# Initialize function


## -description


Initializes a thread to use Windows Runtime APIs.


## -parameters




### -param initType

Specifies the apartment type of the thread to be initialized.


## -returns



<ul>
<li><b>S_OK</b> - Successfully initialized for the first time on the current thread</li>
<li><b>S_FALSE</b> - Successful nested initialization (current thread was already 
        initialized for the specified apartment type)</li>
<li><b>E_INVALIDARG</b> - Invalid <i>initType</i> value</li>
<li><b>CO_E_INIT_TLS</b> - Failed to allocate COM's internal TLS structure</li>
<li><b>E_OUTOFMEMORY</b> - Failed to allocate per-thread/per-apartment structures other 
        than the TLS</li>
<li><b>RPC_E_CHANGED_MODE</b> - The current thread is already initialized for a different 
        apartment type from what is specified.</li>
</ul>



## -remarks



<b>Windows::Foundation::Initialize</b> is changed to create 
    ASTAs instead of classic STAs for the <a href="https://msdn.microsoft.com/961ABFEB-E11F-4405-A021-F3756A79AF18">RO_INIT_TYPE</a> 
    value <b>RO_INIT_SINGLETHREADED</b>. 
    <b>Windows::Foundation::Initialize</b>(<b>RO_INIT_SINGLETHREADED</b>) 
    is not supported for desktop applications and will return <b>CO_E_NOTSUPPORTED</b> if called 
    from a process other than a Windows Store app.

For Microsoft DirectX applications, you must initialize the initial thread by using 
    <b>Windows::Foundation::Initialize</b>(<b>RO_INIT_MULTITHREADED</b>).

For an out-of-process EXE server,  you must initialize the initial thread of the server by using 
    <b>Windows::Foundation::Initialize</b>(<b>RO_INIT_MULTITHREADED</b>).




## -see-also




<a href="https://msdn.microsoft.com/961ABFEB-E11F-4405-A021-F3756A79AF18">RO_INIT_TYPE</a>
 

 

