---
UID: NF:processthreadsapi.TlsFree
title: TlsFree function (processthreadsapi.h)
author: windows-sdk-content
description: Releases a thread local storage (TLS) index, making it available for reuse.
old-location: base\tlsfree.htm
tech.root: ProcThread
ms.assetid: f5b1e8fc-02eb-4a06-b606-2b647944029b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TlsFree, TlsFree function, _win32_tlsfree, base.tlsfree, processthreadsapi/TlsFree, winbase/TlsFree
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
 - TlsFree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TlsFree function


## -description


Releases a thread local storage (TLS) index, making it available for reuse.


## -parameters




### -param dwTlsIndex [in]

The TLS index that was allocated by the 
<a href="https://msdn.microsoft.com/cbb3d832-cd92-4875-8366-6b69be7a536f">TlsAlloc</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<b>Windows Phone 8.1:</b> This function is supported for Windows Phone Store apps on Windows Phone 8.1 and later. When a Windows Phone Store app calls this function, it is replaced with an inline call to <b>FlsFree</b>. Refer to <a href="https://msdn.microsoft.com/ef996c6b-77d0-4b06-97a4-14773cb67146">FlsFree</a> for function documentation.

<b>Windows 8.1</b>, <b>Windows Server 2012 R2</b>, and <b>Windows 10, version 1507</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and Windows 10, version 1507. When a Windows Store app calls this function, it is replaced with an inline call to <b>FlsFree</b>. Refer to <a href="https://msdn.microsoft.com/ef996c6b-77d0-4b06-97a4-14773cb67146">FlsFree</a> for function documentation.

<b>Windows 10, version 1511</b> and <b>Windows 10, version 1607</b>: This function is fully supported for Universal Windows Platform (UWP) apps, and is no longer replaced with an inline call to <b>FlsFree</b>.

If the threads of the process have allocated memory and stored a pointer to the memory in a TLS slot, they should free the memory before calling 
<b>TlsFree</b>. The 
<b>TlsFree</b> function does not free memory blocks whose addresses have been stored in the TLS slots associated with the TLS index. It is expected that DLLs call this function (if at all) only during <b>DLL_PROCESS_DETACH</b>.

For more information, see 
<a href="https://msdn.microsoft.com/40df7410-64d6-4edd-8009-d9c3d2aca920">Thread Local Storage</a>.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/b7f5a206-a827-4b6b-86f6-5e3aea1246b7">Using Thread Local Storage</a> or 
<a href="https://msdn.microsoft.com/a300f223-b513-4a22-a7a4-5d98cf74d77d">Using Thread Local Storage in a Dynamic-Link Library</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/6bff848c-0c55-41e7-aff1-84c6b21a1b8d">Processes and Threads Overview</a>



<a href="https://msdn.microsoft.com/40df7410-64d6-4edd-8009-d9c3d2aca920">Thread Local Storage</a>



<a href="https://msdn.microsoft.com/cbb3d832-cd92-4875-8366-6b69be7a536f">TlsAlloc</a>



<a href="https://msdn.microsoft.com/82bd5ff6-ff0b-42b7-9ece-e9e8531eb5fb">TlsGetValue</a>



<a href="https://msdn.microsoft.com/531b4a4a-a251-4ab4-b00a-754783a51283">TlsSetValue</a>
 

 

