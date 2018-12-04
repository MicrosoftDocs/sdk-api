---
UID: NF:processthreadsapi.TlsGetValue
title: TlsGetValue function
author: windows-sdk-content
description: Retrieves the value in the calling thread's thread local storage (TLS) slot for the specified TLS index. Each thread of a process has its own slot for each TLS index.
old-location: base\tlsgetvalue.htm
tech.root: procthread
ms.assetid: 82bd5ff6-ff0b-42b7-9ece-e9e8531eb5fb
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: TlsGetValue, TlsGetValue function, _win32_tlsgetvalue, base.tlsgetvalue, processthreadsapi/TlsGetValue, winbase/TlsGetValue
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
 - TlsGetValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TlsGetValue function


## -description


Retrieves the value in the calling thread's thread local storage (TLS) slot for the specified TLS index. Each thread of a process has its own slot for each TLS index.


## -parameters




### -param dwTlsIndex [in]

The TLS index that was allocated by the 
<a href="https://msdn.microsoft.com/cbb3d832-cd92-4875-8366-6b69be7a536f">TlsAlloc</a> function.


## -returns



If the function succeeds, the return value is the value stored in the calling thread's TLS slot associated with the specified index. If <i>dwTlsIndex</i> is a valid index allocated by a successful call to <a href="https://msdn.microsoft.com/cbb3d832-cd92-4875-8366-6b69be7a536f">TlsAlloc</a>, this function always succeeds.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The data stored in a TLS slot can have a value of 0 because it still has its initial value or because the thread called the <a href="https://msdn.microsoft.com/531b4a4a-a251-4ab4-b00a-754783a51283">TlsSetValue</a> function with 0. Therefore, if the return value is 0, you must check whether <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_SUCCESS</b> before determining that the function has failed. If <b>GetLastError</b> returns <b>ERROR_SUCCESS</b>, then the function has succeeded and the data stored in the TLS slot is 0. Otherwise, the function has failed.

Functions that return indications of failure call <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a>when they fail. They generally do not call <b>SetLastError</b>when they succeed. The 
<b>TlsGetValue</b> function is an exception to this general rule. The 
<b>TlsGetValue</b> function calls <b>SetLastError</b>to clear a thread's last error when it succeeds. That allows checking for the error-free retrieval of zero values.




## -remarks



<b>Windows Phone 8.1:</b> This function is supported for Windows Phone Store apps on Windows Phone 8.1 and later. When a Windows Phone Store app calls this function, it is replaced with an inline call to <b>FlsGetValue</b>. Refer to <a href="https://msdn.microsoft.com/5d5a1fe6-10ed-42c5-87db-b24eef6f174c">FlsGetValue</a> for function documentation.

<b>Windows 8.1</b>, <b>Windows Server 2012 R2</b>, and <b>Windows 10, version 1507</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and Windows 10, version 1507. When a Windows Store app calls this function, it is replaced with an inline call to <b>FlsGetValue</b>. Refer to <a href="https://msdn.microsoft.com/5d5a1fe6-10ed-42c5-87db-b24eef6f174c">FlsGetValue</a> for function documentation.

<b>Windows 10, version 1511</b> and <b>Windows 10, version 1607</b>: This function is fully supported for Universal Windows Platform (UWP) apps, and is no longer replaced with an inline call to <b>FlsGetValue</b>.

TLS indexes are typically allocated by the 
<a href="https://msdn.microsoft.com/cbb3d832-cd92-4875-8366-6b69be7a536f">TlsAlloc</a> function during process or DLL initialization. After a TLS index is allocated, each thread of the process can use it to access its own TLS slot for that index. A thread specifies a TLS index in a call to 
<a href="https://msdn.microsoft.com/531b4a4a-a251-4ab4-b00a-754783a51283">TlsSetValue</a> to store a value in its slot. The thread specifies the same index in a subsequent call to 
<b>TlsGetValue</b> to retrieve the stored value.

<b>TlsGetValue</b> was implemented with speed as the primary goal. The function performs minimal parameter validation and error checking. In particular, it succeeds if <i>dwTlsIndex</i> is in the range 0 through (<b>TLS_MINIMUM_AVAILABLE</b>– 1). It is up to the programmer to ensure that the index is valid and that the thread calls <a href="https://msdn.microsoft.com/531b4a4a-a251-4ab4-b00a-754783a51283">TlsSetValue</a> before calling <b>TlsGetValue</b>.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/b7f5a206-a827-4b6b-86f6-5e3aea1246b7">Using Thread Local Storage</a> or 
<a href="https://msdn.microsoft.com/a300f223-b513-4a22-a7a4-5d98cf74d77d">Using Thread Local Storage in a Dynamic-Link Library</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/40df7410-64d6-4edd-8009-d9c3d2aca920">Thread Local Storage</a>



<a href="https://msdn.microsoft.com/cbb3d832-cd92-4875-8366-6b69be7a536f">TlsAlloc</a>



<a href="https://msdn.microsoft.com/f5b1e8fc-02eb-4a06-b606-2b647944029b">TlsFree</a>



<a href="https://msdn.microsoft.com/531b4a4a-a251-4ab4-b00a-754783a51283">TlsSetValue</a>
 

 

