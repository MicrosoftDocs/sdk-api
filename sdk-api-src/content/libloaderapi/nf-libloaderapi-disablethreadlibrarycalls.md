---
UID: NF:libloaderapi.DisableThreadLibraryCalls
title: DisableThreadLibraryCalls function (libloaderapi.h)
author: windows-sdk-content
description: Disables the DLL_THREAD_ATTACH and DLL_THREAD_DETACH notifications for the specified dynamic-link library (DLL).
old-location: base\disablethreadlibrarycalls.htm
tech.root: Dlls
ms.assetid: 25e0e533-35e3-48c6-80a5-f063d38d87ca
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DisableThreadLibraryCalls, DisableThreadLibraryCalls function, _win32_disablethreadlibrarycalls, base.disablethreadlibrarycalls, libloaderapi/DisableThreadLibraryCalls, winbase/DisableThreadLibraryCalls
ms.topic: function
req.header: libloaderapi.h
req.include-header: Windows.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-LibraryLoader-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-LibraryLoader-l1-1-1.dll
 - API-MS-Win-Core-LibraryLoader-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Libraryloader-l1-2-1.dll
 - API-MS-Win-Core-LibraryLoader-L1-2-2.dll
api_name:
 - DisableThreadLibraryCalls
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DisableThreadLibraryCalls function


## -description


Disables the DLL_THREAD_ATTACH and DLL_THREAD_DETACH notifications for the specified dynamic-link library (DLL). This can reduce the size of the working set for some applications.


## -parameters




### -param hLibModule [in]

A handle to the DLL module for which the DLL_THREAD_ATTACH and DLL_THREAD_DETACH notifications are to be disabled. The 
<a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a>, <a href="https://msdn.microsoft.com/4fc699ca-6ffb-4954-9b72-1b827d558563">LoadLibraryEx</a>,  or 
<a href="https://msdn.microsoft.com/29514410-89fe-4888-8b34-0c30d5af237f">GetModuleHandle</a> function returns this handle. Note that you cannot call <b>GetModuleHandle</b> with NULL because this returns the base address of the executable image, not the DLL image.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. The 
<b>DisableThreadLibraryCalls</b> function fails if the DLL specified by <i>hModule</i> has active static thread local storage, or if <i>hModule</i> is an invalid module handle. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>DisableThreadLibraryCalls</b> function lets a DLL disable the DLL_THREAD_ATTACH and DLL_THREAD_DETACH notification calls. This can be a useful optimization for multithreaded applications that have many DLLs, frequently create and delete threads, and whose DLLs do not need these thread-level notifications of attachment/detachment. A remote procedure call (RPC) server application is an example of such an application. In these sorts of applications, DLL initialization routines often remain in memory to service DLL_THREAD_ATTACH and DLL_THREAD_DETACH notifications. By disabling the notifications, the DLL initialization code is not paged in because a thread is created or deleted, thus reducing the size of the application's working code set. To implement the optimization, modify a DLL's DLL_PROCESS_ATTACH code to call 
<b>DisableThreadLibraryCalls</b>.

Do not call this function from a DLL that is linked to the static C run-time library (CRT). The static CRT requires DLL_THREAD_ATTACH and DLL_THREAD_DETATCH notifications to function properly.




## -see-also




<a href="https://msdn.microsoft.com/ec035fc6-0a6f-4e52-a4cc-8d7a25a94366">Dynamic-Link Library Entry-Point Function</a>



<a href="https://msdn.microsoft.com/29e50bd5-1712-407f-bcb3-50a0a22ab8b5">Dynamic-Link Library Functions</a>



<a href="https://msdn.microsoft.com/be63fdbf-b3a4-44a8-99b4-b41e159952a7">FreeLibraryAndExitThread</a>
 

 

