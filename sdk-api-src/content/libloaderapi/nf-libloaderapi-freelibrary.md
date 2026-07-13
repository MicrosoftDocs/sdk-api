---
UID: NF:libloaderapi.FreeLibrary
title: FreeLibrary function (libloaderapi.h)
description: Frees the loaded dynamic-link library (DLL) module and, if necessary, decrements its reference count.
helpviewer_keywords: ["FreeLibrary","FreeLibrary function","_win32_freelibrary","base.freelibrary","libloaderapi/FreeLibrary","winbase/FreeLibrary"]
old-location: base\freelibrary.htm
tech.root: base
ms.assetid: 823d3147-4ba8-4fe5-ade4-e5604f47eb0a
ms.date: 12/05/2018
ms.keywords: FreeLibrary, FreeLibrary function, _win32_freelibrary, base.freelibrary, libloaderapi/FreeLibrary, winbase/FreeLibrary
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FreeLibrary
 - libloaderapi/FreeLibrary
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-libraryloader-l1-2-3.dll
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
---

# FreeLibrary function


## -description

Frees the loaded dynamic-link library (DLL) module and, if necessary, decrements its reference count. When the reference count reaches zero, the module is unloaded from the address space of the calling process and the handle is no longer valid.

## -parameters

### -param hLibModule [in]

A handle to the loaded library module. The 
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>, <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a>,  
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea">GetModuleHandle</a>, or <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandleexa">GetModuleHandleEx</a> function returns this handle.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

The system maintains a per-process reference count for each loaded module. A  module that was loaded at process initialization due to load-time dynamic linking has a reference count of one. The reference count for a module is incremented each time the  module is loaded by a call to 
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>. The reference count is also incremented by a call to <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a> unless the  module  is being loaded for the first time and is being loaded as   a data or image file. 

The reference count is decremented each time 
the <b>FreeLibrary</b> or <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread">FreeLibraryAndExitThread</a> function is called for the module. When a  module's reference count reaches zero or the process terminates, the system unloads the module from the address space of the  process. Before unloading a library module, the system enables the module to detach from the process by calling the module's 
<a href="/windows/desktop/Dlls/dllmain">DllMain</a> function, if it has one, with the DLL_PROCESS_DETACH value. Doing so gives the library module an opportunity to clean up resources allocated on behalf of the current process. After the entry-point function returns, the library module is removed from the address space of the current process.

It is not safe to call 
<b>FreeLibrary</b> from 
<a href="/windows/desktop/Dlls/dllmain">DllMain</a>. For more information, see the Remarks section in 
<a href="/windows/desktop/Dlls/dllmain">DllMain</a>.

Calling 
<b>FreeLibrary</b> does not affect other processes that are using the same module.

Use caution when calling <b>FreeLibrary</b> with a handle returned by <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea">GetModuleHandle</a>. The <b>GetModuleHandle</b> function does not increment a module's reference count, so passing this handle to <b>FreeLibrary</b> can cause a module to be unloaded prematurely.

A thread that must unload the DLL in which it is executing and then terminate itself should call <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread">FreeLibraryAndExitThread</a> instead of calling <b>FreeLibrary</b> and <b>ExitThread</b> separately. Otherwise, a race condition can occur. For details, see the Remarks section of <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread">FreeLibraryAndExitThread</a>. 


#### Examples

For an example, see 
<a href="/windows/desktop/Dlls/using-run-time-dynamic-linking">Using Run-Time Dynamic Linking</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/Dlls/dllmain">DllMain</a>



<a href="/windows/desktop/Dlls/dynamic-link-library-functions">Dynamic-Link Library Functions</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread">FreeLibraryAndExitThread</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea">GetModuleHandle</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandleexa">GetModuleHandleEx</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a>



<a href="/windows/desktop/Dlls/run-time-dynamic-linking">Run-Time Dynamic Linking</a>