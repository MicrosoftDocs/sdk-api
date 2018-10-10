---
UID: NF:processthreadsapi.TlsAlloc
title: TlsAlloc function
author: windows-sdk-content
description: Allocates a thread local storage (TLS) index. Any thread of the process can subsequently use this index to store and retrieve values that are local to the thread, because each thread receives its own slot for the index.
old-location: base\tlsalloc.htm
tech.root: ProcThread
ms.assetid: cbb3d832-cd92-4875-8366-6b69be7a536f
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: TlsAlloc, TlsAlloc function, _win32_tlsalloc, base.tlsalloc, processthreadsapi/TlsAlloc, winbase/TlsAlloc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib; WindowsPhoneCore.lib on Windows Phone 8.1
req.dll: KernelBase.dll on Windows Phone 8.1; Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - KernelBase.dll
 - Kernel32.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - TlsAlloc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TlsAlloc function


## -description


Allocates a thread local storage (TLS) index. Any thread of the process can subsequently use this index to store and retrieve values that are local to the thread, because each thread receives its own slot for the index.


## -parameters






## -returns



If the function succeeds, the return value is a TLS index. The slots for the index are initialized to zero.

If the function fails, the return value is <b>TLS_OUT_OF_INDEXES</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<b>Windows Phone 8.1:</b> This function is supported for Windows Phone Store apps on Windows Phone 8.1 and later. When a Windows Phone Store app calls this function, it is replaced with an inline call to <b>FlsAlloc</b>. Refer to <a href="https://msdn.microsoft.com/dc348ef3-37e5-40f2-bd5c-5f8aebc7cc59">FlsAlloc</a> for function documentation.

<b>Windows 8.1</b>,  <b>Windows Server 2012 R2</b>, and <b>Windows 10, version 1507</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and Windows 10, version 1507. When a Windows Store app calls this function, it is replaced with an inline call to <b>FlsAlloc</b>. Refer to <a href="https://msdn.microsoft.com/dc348ef3-37e5-40f2-bd5c-5f8aebc7cc59">FlsAlloc</a> for function documentation.

<b>Windows 10, version 1511</b> and <b>Windows 10, version 1607</b>: This function is fully supported for Universal Windows Platform (UWP) apps, and is no longer replaced with an inline call to <b>FlsAlloc</b>.

The threads of the process can use the TLS index in subsequent calls to the 
<a href="https://msdn.microsoft.com/f5b1e8fc-02eb-4a06-b606-2b647944029b">TlsFree</a>, 
<a href="https://msdn.microsoft.com/531b4a4a-a251-4ab4-b00a-754783a51283">TlsSetValue</a>, or 
<a href="https://msdn.microsoft.com/82bd5ff6-ff0b-42b7-9ece-e9e8531eb5fb">TlsGetValue</a> functions. The value of the TLS index should be treated as an opaque value; do not assume that it is an index into a zero-based array. 

TLS indexes are typically allocated during process or dynamic-link library (DLL) initialization. When a TLS index is allocated, its storage slots are initialized to <b>NULL</b>. After a TLS index has been allocated, each thread of the process can use it to access its own TLS storage slot. To store a value in its TLS slot, a thread specifies the index in a call to 
<a href="https://msdn.microsoft.com/531b4a4a-a251-4ab4-b00a-754783a51283">TlsSetValue</a>. The thread specifies the same index in a subsequent call to 
<a href="https://msdn.microsoft.com/82bd5ff6-ff0b-42b7-9ece-e9e8531eb5fb">TlsGetValue</a>, to retrieve the stored value.

TLS indexes are not valid across process boundaries. A DLL cannot assume that an index assigned in one process is valid in another process.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/b7f5a206-a827-4b6b-86f6-5e3aea1246b7">Using Thread Local Storage</a> or 
<a href="https://msdn.microsoft.com/a300f223-b513-4a22-a7a4-5d98cf74d77d">Using Thread Local Storage in a Dynamic-Link Library</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/40df7410-64d6-4edd-8009-d9c3d2aca920">Thread Local Storage</a>



<a href="https://msdn.microsoft.com/f5b1e8fc-02eb-4a06-b606-2b647944029b">TlsFree</a>



<a href="https://msdn.microsoft.com/82bd5ff6-ff0b-42b7-9ece-e9e8531eb5fb">TlsGetValue</a>



<a href="https://msdn.microsoft.com/531b4a4a-a251-4ab4-b00a-754783a51283">TlsSetValue</a>
 

 

