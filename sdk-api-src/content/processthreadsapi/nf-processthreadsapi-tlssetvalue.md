---
UID: NF:processthreadsapi.TlsSetValue
title: TlsSetValue function
author: windows-sdk-content
description: Stores a value in the calling thread's thread local storage (TLS) slot for the specified TLS index. Each thread of a process has its own slot for each TLS index.
old-location: base\tlssetvalue.htm
tech.root: ProcThread
ms.assetid: 531b4a4a-a251-4ab4-b00a-754783a51283
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: TlsSetValue, TlsSetValue function, _win32_tlssetvalue, base.tlssetvalue, processthreadsapi/TlsSetValue, winbase/TlsSetValue
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
 - TlsSetValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- TlsSetValue
: 
---

# TlsSetValue function


## -description


Stores a value in the calling thread's thread local storage (TLS) slot for the specified TLS index. Each thread of a process has its own slot for each TLS index.


## -parameters




### -param dwTlsIndex [in]

The TLS index that was allocated by the <a href="https://msdn.microsoft.com/cbb3d832-cd92-4875-8366-6b69be7a536f">TlsAlloc</a> 
      function.


### -param lpTlsValue [in, optional]

The value to be stored in the calling thread's TLS slot for the index.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<b>Windows Phone 8.1:</b> This function is supported for Windows Phone Store apps on Windows Phone 8.1 and later. When a Windows Phone Store app calls this function, it is replaced with an inline call to <b>FlsSetValue</b>. Refer to <a href="https://msdn.microsoft.com/f2abea00-8c1b-47e8-a4e9-9e3e7242d0ad">FlsSetValue</a> for function documentation.

<b>Windows 8.1</b>, <b>Windows Server 2012 R2</b>, and <b>Windows 10, version 1507</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and Windows 10, version 1507. When a Windows Store app calls this function, it is replaced with an inline call to <b>FlsSetValue</b>. Refer to <a href="https://msdn.microsoft.com/f2abea00-8c1b-47e8-a4e9-9e3e7242d0ad">FlsSetValue</a> for function documentation.

<b>Windows 10, version 1511</b> and <b>Windows 10, version 1607</b>: This function is fully supported for Universal Windows Platform (UWP) apps, and is no longer replaced with an inline call to <b>FlsSetValue</b>.

TLS indexes are typically allocated by the 
<a href="https://msdn.microsoft.com/cbb3d832-cd92-4875-8366-6b69be7a536f">TlsAlloc</a> function during process or DLL initialization. When a TLS index is allocated, its storage slots are initialized to NULL. After a TLS index is allocated, each thread of the process can use it to access its own TLS slot for that index. A thread specifies a TLS index in a call to 
<b>TlsSetValue</b>, to store a value in its slot. The thread specifies the same index in a subsequent call to 
<a href="https://msdn.microsoft.com/82bd5ff6-ff0b-42b7-9ece-e9e8531eb5fb">TlsGetValue</a>, to retrieve the stored value.

<b>TlsSetValue</b> was implemented with speed as the primary goal. The function performs minimal parameter validation and error checking. In particular, it succeeds if <i>dwTlsIndex</i> is in the range 0 through (<b>TLS_MINIMUM_AVAILABLE </b>– 1). It is up to the programmer to ensure that the index is valid before calling <a href="https://msdn.microsoft.com/82bd5ff6-ff0b-42b7-9ece-e9e8531eb5fb">TlsGetValue</a>.


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



<a href="https://msdn.microsoft.com/82bd5ff6-ff0b-42b7-9ece-e9e8531eb5fb">TlsGetValue</a>
 

 

