---
UID: NF:libloaderapi.FreeLibraryAndExitThread
title: FreeLibraryAndExitThread function
author: windows-sdk-content
description: Decrements the reference count of a loaded dynamic-link library (DLL) by one, then calls ExitThread to terminate the calling thread.
old-location: base\freelibraryandexitthread.htm
tech.root: dlls
ms.assetid: be63fdbf-b3a4-44a8-99b4-b41e159952a7
ms.author: windowssdkdev
ms.date: 09/04/2018
ms.keywords: FreeLibraryAndExitThread, FreeLibraryAndExitThread function, _win32_freelibraryandexitthread, base.freelibraryandexitthread, libloaderapi/FreeLibraryAndExitThread, winbase/FreeLibraryAndExitThread
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - FreeLibraryAndExitThread
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FreeLibraryAndExitThread function


## -description


Decrements the reference count of a loaded dynamic-link library (DLL) by one, then calls 
<a href="https://msdn.microsoft.com/e7f6d054-c535-4521-a3b4-800a9174732f">ExitThread</a> to terminate the calling thread. The function does not return.


## -parameters




### -param hLibModule [in]

A handle to the DLL module whose reference count the function decrements. The 
<a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> or 
<a href="https://msdn.microsoft.com/951c7e6e-1d6d-4393-a675-d2b353c53b87">GetModuleHandleEx</a> function returns this handle.

Do not call this function with a handle returned by the <a href="https://msdn.microsoft.com/29514410-89fe-4888-8b34-0c30d5af237f">GetModuleHandle</a> function, since this function does not maintain a reference count for the module.


### -param dwExitCode [in]

The exit code for the calling thread.


## -returns



This function does not return a value. Invalid module handles are ignored.




## -remarks



The 
<b>FreeLibraryAndExitThread</b> function allows threads that are executing within a DLL to safely free the DLL in which they are executing and terminate themselves. If they were to call 
<a href="https://msdn.microsoft.com/823d3147-4ba8-4fe5-ade4-e5604f47eb0a">FreeLibrary</a> and 
<a href="https://msdn.microsoft.com/e7f6d054-c535-4521-a3b4-800a9174732f">ExitThread</a> separately, a race condition would exist. The library could be unloaded before 
<b>ExitThread</b> is called.




## -see-also




<a href="https://msdn.microsoft.com/25e0e533-35e3-48c6-80a5-f063d38d87ca">DisableThreadLibraryCalls</a>



<a href="https://msdn.microsoft.com/29e50bd5-1712-407f-bcb3-50a0a22ab8b5">Dynamic-Link Library Functions</a>



<a href="https://msdn.microsoft.com/e7f6d054-c535-4521-a3b4-800a9174732f">ExitThread</a>



<a href="https://msdn.microsoft.com/823d3147-4ba8-4fe5-ade4-e5604f47eb0a">FreeLibrary</a>



<a href="https://msdn.microsoft.com/81e237a9-3c32-46a5-88d3-c978f43dad54">Run-Time Dynamic Linking</a>
 

 

