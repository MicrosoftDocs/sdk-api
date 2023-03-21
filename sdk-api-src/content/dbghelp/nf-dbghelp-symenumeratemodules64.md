---
UID: NF:dbghelp.SymEnumerateModules64
title: SymEnumerateModules64 function (dbghelp.h)
description: Enumerates all modules that have been loaded for the process by the SymLoadModule64 or SymLoadModuleEx function. (SymEnumerateModules64)
helpviewer_keywords: ["SymEnumerateModules","SymEnumerateModules function","SymEnumerateModules64","SymEnumerateModules64 function","SymEnumerateModulesW64","_win32_symenumeratemodules64","base.symenumeratemodules64","dbghelp/SymEnumerateModules","dbghelp/SymEnumerateModules64","dbghelp/SymEnumerateModulesW64"]
old-location: base\symenumeratemodules64.htm
tech.root: Debug
ms.assetid: d2372521-eff7-4ac4-a0f3-1267ef50db6e
ms.date: 12/05/2018
ms.keywords: SymEnumerateModules, SymEnumerateModules function, SymEnumerateModules64, SymEnumerateModules64 function, SymEnumerateModulesW64, _win32_symenumeratemodules64, base.symenumeratemodules64, dbghelp/SymEnumerateModules, dbghelp/SymEnumerateModules64, dbghelp/SymEnumerateModulesW64
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymEnumerateModulesW64 (Unicode) and SymEnumerateModules64 (ANSI)
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
 - SymEnumerateModules64
 - dbghelp/SymEnumerateModules64
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
 - SymEnumerateModules64
 - SymEnumerateModules64
 - SymEnumerateModulesW64
 - SymEnumerateModules
---

# SymEnumerateModules64 function


## -description

Enumerates all modules that have been loaded for the process by the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symloadmodule">SymLoadModule64</a> or <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symloadmoduleex">SymLoadModuleEx</a> function.

## -parameters

### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param EnumModulesCallback [in]

The enumeration callback function. This function is called once per module. For more information, see 
<a href="/windows/desktop/api/dbghelp/nc-dbghelp-psym_enummodules_callback">SymEnumerateModulesProc64</a>.

### -param UserContext [in, optional]

A user-defined value or <b>NULL</b>. This value is simply passed to the callback function. Normally, this parameter is used by an application to pass a pointer to a data structure that lets the callback function establish some type of context.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>SymEnumerateModules64</b> function enumerates all modules that have been loaded for the process by 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symloadmodule">SymLoadModule64</a>, even if the symbol loading is deferred. The enumeration callback function is called once for each module and is passed the module information.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR. <b>SymEnumerateModulesW64</b> is defined as follows in Dbghelp.h. 


```cpp

BOOL
IMAGEAPI
SymEnumerateModulesW64(
    __in HANDLE hProcess,
    __in PSYM_ENUMMODULES_CALLBACKW64 EnumModulesCallback,
    __in_opt PVOID UserContext
    );

#ifdef DBGHELP_TRANSLATE_TCHAR
#define SymEnumerateModules64  SymEnumerateModulesW64
#endif
```


This function supersedes the <b>SymEnumerateModules</b> function. For more information, see 
<a href="/windows/desktop/Debug/updated-platform-support">Updated Platform Support</a>. <b>SymEnumerateModules</b> is defined as follows in Dbghelp.h. 


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define SymEnumerateModules SymEnumerateModules64
#else
BOOL
IMAGEAPI
SymEnumerateModules(
    __in HANDLE hProcess,
    __in PSYM_ENUMMODULES_CALLBACK EnumModulesCallback,
    __in_opt PVOID UserContext
    );
#endif
```



#### Examples

For an example, see 
<a href="/windows/desktop/Debug/enumerating-symbol-modules">Enumerating Symbol Modules</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nc-dbghelp-psym_enummodules_callback">SymEnumerateModulesProc64</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symloadmodule">SymLoadModule64</a>
