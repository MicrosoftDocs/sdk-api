---
UID: NF:libloaderapi2.QueryOptionalDelayLoadedAPI
title: QueryOptionalDelayLoadedAPI function (libloaderapi2.h)
description: Determines whether the specified function in a delay-loaded DLL is available on the system.
helpviewer_keywords: ["QueryOptionalDelayLoadedAPI","QueryOptionalDelayLoadedAPI function","base.queryoptionaldelayloadedapi","libloaderapi2/QueryOptionalDelayLoadedAPI"]
old-location: base\queryoptionaldelayloadedapi.htm
tech.root: base
ms.assetid: 43690689-4372-48ae-ac6d-230250f05f7c
ms.date: 12/05/2018
ms.keywords: QueryOptionalDelayLoadedAPI, QueryOptionalDelayLoadedAPI function, base.queryoptionaldelayloadedapi, libloaderapi2/QueryOptionalDelayLoadedAPI
req.header: libloaderapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WindowsApp.lib
req.dll: Api-ms-win-core-libraryloader-l1-1-1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - QueryOptionalDelayLoadedAPI
 - libloaderapi2/QueryOptionalDelayLoadedAPI
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-libraryloader-l1-1-1.dll
 - kernelbase.dll
 - api-ms-win-core-libraryloader-l2-1-0.dll
 - API-MS-Win-Core-LibraryLoader-Private-L1-1-0.dll
api_name:
 - QueryOptionalDelayLoadedAPI
---

# QueryOptionalDelayLoadedAPI function


## -description

Determines whether the specified function in a delay-loaded DLL is available on the system.

## -parameters

### -param hParentModule [in]

A handle to the calling module. Desktop applications can use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea">GetModuleHandle</a> or <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandleexa">GetModuleHandleEx</a> function to get this handle. Windows Store apps should set this parameter to <code>static_cast&lt;HMODULE&gt;(&amp;__ImageBase)</code>.

### -param lpDllName [in]

The file name of the delay-loaded DLL that exports the specified function. This parameter is case-insensitive.

Windows Store apps should specify API sets, rather than monolithic DLLs. For example,   api-ms-win-core-memory-l1-1-1.dll, rather than kernel32.dll.

### -param lpProcName [in]

The name of the function to query. This parameter is case-sensitive.

### -param Reserved

This parameter is reserved and must be zero (0).

## -returns

TRUE if the specified function is available on the system. If the specified function is not available on the system, this function returns FALSE. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

A delay-loaded DLL is statically linked but not actually loaded into memory until the running application references a symbol exported by that DLL. Applications often delay load DLLs that contain functions the application might call only rarely or not at all, because the DLL is only loaded when it is needed instead of being loaded at application startup like other statically linked DLLs. This helps improve application performance, especially during initialization. A delay-load DLL is specified at link time with the <a href="/cpp/build/reference/delayload-delay-load-import">/DELAYLOAD (Delay Load Import)</a> linker option. 

Applications that target multiple versions of Windows or multiple Windows device families also rely on delay-loaded DLLs to make visible extra features when they are available.

A desktop application can use delayed loading as an alternative to runtime dynamic linking that uses  <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> or <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a> to load a DLL and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> to get a pointer to a function. A Windows Store app cannot use <b>LoadLibrary</b> or <b>LoadLibraryEx</b>, so to get the benefits to runtime dynamic linking, a Windows Store app must use the delayed loading mechanism.

To check whether a function in a delay-loaded DLL is available on the system, the application calls <b>QueryOptionalDelayLoadedAPI</b> with the specified function. If <b>QueryOptionalDelayLoadedAPI</b> succeeds, the application can safely call the specified function. 


#### Examples

The following example shows how to use <b>QueryOptionalDelayLoadedAPI</b> to determine whether the <a href="/windows/win32/api/objbase/nf-objbase-mkparsedisplayname">MkParseDisplayName</a> function is available on the system.


```cpp
#include <windows.h>
#include <libloaderapi2.h>

// For this example, you need to pass
// /delayload: ext-ms-win-com-ole32-l1-1-1.dll to link.exe.

EXTERN_C IMAGE_DOS_HEADER __ImageBase;

BOOL
AreMonikersSupported ()
{

    BOOL isApiAvailable;

    // Check if MkParseDisplayName is available on the system. It is only
    // available on desktop computers, and not on mobile devices or Xbox.

    isApiAvailable = 
        QueryOptionalDelayLoadedAPI(static_cast<HMODULE>(&__ImageBase),
                                    "ext-ms-win-com-ole32-l1-1-1.dll",
                                    "MkParseDisplayName",
                                    0);

    return isApiAvailable;
}

```

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-loadpackagedlibrary">LoadPackagedLibrary</a>



<a href="/windows/desktop/Dlls/run-time-dynamic-linking">Run-Time Dynamic Linking</a>
