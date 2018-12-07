---
UID: NF:libloaderapi.FreeLibrary
title: FreeLibrary function
author: windows-sdk-content
description: Frees the loaded dynamic-link library (DLL) module and, if necessary, decrements its reference count.
old-location: base\freelibrary.htm
tech.root: Dlls
ms.assetid: 823d3147-4ba8-4fe5-ade4-e5604f47eb0a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FreeLibrary, FreeLibrary function, _win32_freelibrary, base.freelibrary, libloaderapi/FreeLibrary, winbase/FreeLibrary
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
 - FreeLibrary
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FreeLibrary function


## -description


Frees the loaded dynamic-link library (DLL) module and, if necessary, decrements its reference count. When the reference count reaches zero, the module is unloaded from the address space of the calling process and the handle is no longer valid.


## -parameters




### -param hLibModule [in]

A handle to the loaded library module. The 
<a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a>, <a href="https://msdn.microsoft.com/4fc699ca-6ffb-4954-9b72-1b827d558563">LoadLibraryEx</a>,  
<a href="https://msdn.microsoft.com/29514410-89fe-4888-8b34-0c30d5af237f">GetModuleHandle</a>, or <a href="https://msdn.microsoft.com/951c7e6e-1d6d-4393-a675-d2b353c53b87">GetModuleHandleEx</a> function returns this handle.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



The system maintains a per-process reference count for each loaded module. A  module that was loaded at process initialization due to load-time dynamic linking has a reference count of one. The reference count for a module is incremented each time the  module is loaded by a call to 
<a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a>. The reference count is also incremented by a call to <a href="https://msdn.microsoft.com/4fc699ca-6ffb-4954-9b72-1b827d558563">LoadLibraryEx</a> unless the  module  is being loaded for the first time and is being loaded as   a data or image file. 

The reference count is decremented each time 
the <b>FreeLibrary</b> or <a href="https://msdn.microsoft.com/be63fdbf-b3a4-44a8-99b4-b41e159952a7">FreeLibraryAndExitThread</a> function is called for the module. When a  module's reference count reaches zero or the process terminates, the system unloads the module from the address space of the  process. Before unloading a library module, the system enables the module to detach from the process by calling the module's 
<a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a> function, if it has one, with the DLL_PROCESS_DETACH value. Doing so gives the library module an opportunity to clean up resources allocated on behalf of the current process. After the entry-point function returns, the library module is removed from the address space of the current process.

It is not safe to call 
<b>FreeLibrary</b> from 
<a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a>. For more information, see the Remarks section in 
<a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a>.

Calling 
<b>FreeLibrary</b> does not affect other processes that are using the same module.

Use caution when calling <b>FreeLibrary</b> with a handle returned by <a href="https://msdn.microsoft.com/29514410-89fe-4888-8b34-0c30d5af237f">GetModuleHandle</a>. The <b>GetModuleHandle</b> function does not increment a module's reference count, so passing this handle to <b>FreeLibrary</b> can cause a module to be unloaded prematurely.

A thread that must unload the DLL in which it is executing and then terminate itself should call <a href="https://msdn.microsoft.com/be63fdbf-b3a4-44a8-99b4-b41e159952a7">FreeLibraryAndExitThread</a> instead of calling <b>FreeLibrary</b> and <b>ExitThread</b> separately. Otherwise, a race condition can occur. For details, see the Remarks section of <a href="https://msdn.microsoft.com/be63fdbf-b3a4-44a8-99b4-b41e159952a7">FreeLibraryAndExitThread</a>. 


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/0ffce2b1-ce50-4550-aa68-6628fdcac01a">Using Run-Time Dynamic Linking</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a>



<a href="https://msdn.microsoft.com/29e50bd5-1712-407f-bcb3-50a0a22ab8b5">Dynamic-Link Library Functions</a>



<a href="https://msdn.microsoft.com/be63fdbf-b3a4-44a8-99b4-b41e159952a7">FreeLibraryAndExitThread</a>



<a href="https://msdn.microsoft.com/29514410-89fe-4888-8b34-0c30d5af237f">GetModuleHandle</a>



<a href="https://msdn.microsoft.com/951c7e6e-1d6d-4393-a675-d2b353c53b87">GetModuleHandleEx</a>



<a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a>



<a href="https://msdn.microsoft.com/81e237a9-3c32-46a5-88d3-c978f43dad54">Run-Time Dynamic Linking</a>
 

 

