---
UID: NF:libloaderapi.FreeLibraryAndExitThread
title: FreeLibraryAndExitThread function (libloaderapi.h)
description: Decrements the reference count of a loaded dynamic-link library (DLL) by one, then calls ExitThread to terminate the calling thread.
helpviewer_keywords: ["FreeLibraryAndExitThread","FreeLibraryAndExitThread function","_win32_freelibraryandexitthread","base.freelibraryandexitthread","libloaderapi/FreeLibraryAndExitThread","winbase/FreeLibraryAndExitThread"]
old-location: base\freelibraryandexitthread.htm
tech.root: base
ms.assetid: be63fdbf-b3a4-44a8-99b4-b41e159952a7
ms.date: 12/05/2018
ms.keywords: FreeLibraryAndExitThread, FreeLibraryAndExitThread function, _win32_freelibraryandexitthread, base.freelibraryandexitthread, libloaderapi/FreeLibraryAndExitThread, winbase/FreeLibraryAndExitThread
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
 - FreeLibraryAndExitThread
 - libloaderapi/FreeLibraryAndExitThread
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
 - FreeLibraryAndExitThread
---

# FreeLibraryAndExitThread function


## -description

Decrements the reference count of a loaded dynamic-link library (DLL) by one, then calls 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread">ExitThread</a> to terminate the calling thread. The function does not return.

## -parameters

### -param hLibModule [in]

A handle to the DLL module whose reference count the function decrements. The 
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> or 
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandleexa">GetModuleHandleEx</a> function returns this handle.

Do not call this function with a handle returned by either the <b>GetModuleHandleEx</b> function (with the GET_MODULE_HANDLE_EX_FLAG_UNCHANGED_REFCOUNT flag) or the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea">GetModuleHandle</a> function, as they do not maintain a reference count for the module.

### -param dwExitCode [in]

The exit code for the calling thread.

## -remarks

The 
<b>FreeLibraryAndExitThread</b> function allows threads that are executing within a DLL to safely free the DLL in which they are executing and terminate themselves. If they were to call 
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary">FreeLibrary</a> and 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread">ExitThread</a> separately, a race condition would exist. The library could be unloaded before 
<b>ExitThread</b> is called.

## -see-also

<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls">DisableThreadLibraryCalls</a>



<a href="/windows/desktop/Dlls/dynamic-link-library-functions">Dynamic-Link Library Functions</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread">ExitThread</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary">FreeLibrary</a>



<a href="/windows/desktop/Dlls/run-time-dynamic-linking">Run-Time Dynamic Linking</a>