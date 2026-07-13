---
UID: NF:libloaderapi.DisableThreadLibraryCalls
title: DisableThreadLibraryCalls function (libloaderapi.h)
description: Disables the DLL_THREAD_ATTACH and DLL_THREAD_DETACH notifications for the specified dynamic-link library (DLL).
helpviewer_keywords: ["DisableThreadLibraryCalls","DisableThreadLibraryCalls function","_win32_disablethreadlibrarycalls","base.disablethreadlibrarycalls","libloaderapi/DisableThreadLibraryCalls","winbase/DisableThreadLibraryCalls"]
old-location: base\disablethreadlibrarycalls.htm
tech.root: base
ms.assetid: 25e0e533-35e3-48c6-80a5-f063d38d87ca
ms.date: 02/05/2024
ms.keywords: DisableThreadLibraryCalls, DisableThreadLibraryCalls function, _win32_disablethreadlibrarycalls, base.disablethreadlibrarycalls, libloaderapi/DisableThreadLibraryCalls, winbase/DisableThreadLibraryCalls
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
 - DisableThreadLibraryCalls
 - libloaderapi/DisableThreadLibraryCalls
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
 - vertdll.dll
api_name:
 - DisableThreadLibraryCalls
---

# DisableThreadLibraryCalls function

## -description

Disables the DLL_THREAD_ATTACH and DLL_THREAD_DETACH notifications for the specified dynamic-link library (DLL). This can reduce the size of the working set for some applications.

## -parameters

### -param hLibModule [in]

A handle to the DLL module for which the DLL_THREAD_ATTACH and DLL_THREAD_DETACH notifications are to be disabled. The [LoadLibrary](nf-libloaderapi-loadlibrarya.md), [LoadLibraryEx](nf-libloaderapi-loadlibraryexa.md), or [GetModuleHandle](nf-libloaderapi-getmodulehandlea.md) function returns this handle. Note that you cannot call **GetModuleHandle** with `NULL` because this returns the base address of the executable image, not the DLL image.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. The **DisableThreadLibraryCalls** function fails if the DLL specified by *hModule* has active static thread local storage, or if *hModule* is an invalid module handle. To get extended error information, call [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md).

## -remarks

The **DisableThreadLibraryCalls** function lets a DLL disable the DLL_THREAD_ATTACH and DLL_THREAD_DETACH notification calls. This can be a useful optimization for multithreaded applications that have many DLLs, frequently create and delete threads, and whose DLLs do not need these thread-level notifications of attachment/detachment. A remote procedure call (RPC) server application is an example of such an application. In these sorts of applications, DLL initialization routines often remain in memory to service DLL_THREAD_ATTACH and DLL_THREAD_DETACH notifications. By disabling the notifications, the DLL initialization code is not paged in because a thread is created or deleted, thus reducing the size of the application's working code set. To implement the optimization, modify a DLL's DLL_PROCESS_ATTACH code to call **DisableThreadLibraryCalls**.

Do not call this function from a DLL that is linked to the static C run-time library (CRT). The static CRT requires DLL_THREAD_ATTACH and DLL_THREAD_DETATCH notifications to function properly.

This function does not perform any optimizations if static [Thread Local Storage (TLS)](/windows/win32/procthread/thread-local-storage) is enabled. Static TLS is enabled when using **thread_local** variables, **__declspec( thread )** variables, or function-local **static**.

## -see-also

[Dynamic-Link Library Entry-Point Function](/windows/win32/Dlls/dynamic-link-library-entry-point-function)

[Dynamic-Link Library Functions](/windows/win32/Dlls/dynamic-link-library-functions)

[FreeLibraryAndExitThread](nf-libloaderapi-freelibraryandexitthread.md)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
