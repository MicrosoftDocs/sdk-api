---
UID: NF:dbghelp.EnumerateLoadedModules64
title: EnumerateLoadedModules64 function (dbghelp.h)
description: Enumerates the loaded modules for the specified process. (EnumerateLoadedModules64)
helpviewer_keywords: ["EnumerateLoadedModules","EnumerateLoadedModules function","EnumerateLoadedModules64","EnumerateLoadedModules64 function","EnumerateLoadedModulesW64","_win32_enumerateloadedmodules64","base.enumerateloadedmodules64","dbghelp/EnumerateLoadedModules","dbghelp/EnumerateLoadedModules64","dbghelp/EnumerateLoadedModulesW64"]
old-location: base\enumerateloadedmodules64.htm
tech.root: Debug
ms.assetid: 9bfa683f-2a0f-418f-8ac4-5c4224265f2e
ms.date: 12/05/2018
ms.keywords: EnumerateLoadedModules, EnumerateLoadedModules function, EnumerateLoadedModules64, EnumerateLoadedModules64 function, EnumerateLoadedModulesW64, _win32_enumerateloadedmodules64, base.enumerateloadedmodules64, dbghelp/EnumerateLoadedModules, dbghelp/EnumerateLoadedModules64, dbghelp/EnumerateLoadedModulesW64
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumerateLoadedModulesW64 (Unicode) and EnumerateLoadedModules64 (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - EnumerateLoadedModules64
 - dbghelp/EnumerateLoadedModules64
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dbghelp.dll
api_name:
 - EnumerateLoadedModules64
 - EnumerateLoadedModules64
 - EnumerateLoadedModulesW64
 - EnumerateLoadedModules
---

# EnumerateLoadedModules64 function


## -description

Enumerates the loaded modules for the specified process.

## -parameters

### -param hProcess [in]

A handle to the process whose modules will be enumerated.

### -param EnumLoadedModulesCallback [in]

An application-defined callback function. For more information, see 
<a href="/windows/desktop/api/dbghelp/nc-dbghelp-penumloaded_modules_callback">EnumerateLoadedModulesProc64</a>.

### -param UserContext [in, optional]

Optional user-defined data. This value is passed to the callback function.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, <i>EnumerateLoadedModulesW64</i>, define <b>DBGHELP_TRANSLATE_TCHAR</b>. <i>EnumerateLoadedModulesW64</i> is defined as follows in DbgHelp.h. 


```cpp
BOOL
IMAGEAPI
EnumerateLoadedModulesW64(
    __in HANDLE hProcess,
    __in PENUMLOADED_MODULES_CALLBACKW64 EnumLoadedModulesCallback,
    __in PVOID UserContext
    );

#ifdef DBGHELP_TRANSLATE_TCHAR
    #define EnumerateLoadedModules64      EnumerateLoadedModulesW64
#endif
```


This function supersedes the <i>EnumerateLoadedModules</i> function. For more information, see 
<a href="/windows/desktop/Debug/updated-platform-support">Updated Platform Support</a>. <i>EnumerateLoadedModules</i> is defined as follows in DbgHelp.h. 


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define EnumerateLoadedModules EnumerateLoadedModules64
#else
BOOL
IMAGEAPI
EnumerateLoadedModules(
    __in HANDLE hProcess,
    __in PENUMLOADED_MODULES_CALLBACK EnumLoadedModulesCallback,
    __in_opt PVOID UserContext
    );
#endif
```

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nc-dbghelp-penumloaded_modules_callback">EnumerateLoadedModulesProc64</a>
