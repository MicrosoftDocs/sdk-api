---
UID: NC:dbghelp.PSYM_ENUMMODULES_CALLBACK
title: PSYM_ENUMMODULES_CALLBACK (dbghelp.h)
description: PSYM_ENUMMODULES_CALLBACK (dbghelp.h) is an application-defined callback function used with the SymEnumerateModules64 function.
helpviewer_keywords: ["PSYM_ENUMMODULES_CALLBACK","PSYM_ENUMMODULES_CALLBACK64","PSYM_ENUMMODULES_CALLBACKW64","SymEnumerateModulesProc64","SymEnumerateModulesProc64 callback","SymEnumerateModulesProc64 callback function","_win32_symenumeratemodulesproc64","base.symenumeratemodulesproc64","dbghelp/SymEnumerateModulesProc64"]
old-location: base\symenumeratemodulesproc64.htm
tech.root: Debug
ms.assetid: 97a82134-7e1b-4c7e-aa55-8347fea4e739
ms.date: 08/03/2022
ms.keywords: PSYM_ENUMMODULES_CALLBACK, PSYM_ENUMMODULES_CALLBACK64, PSYM_ENUMMODULES_CALLBACKW64, SymEnumerateModulesProc64, SymEnumerateModulesProc64 callback, SymEnumerateModulesProc64 callback function, _win32_symenumeratemodulesproc64, base.symenumeratemodulesproc64, dbghelp/SymEnumerateModulesProc64
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - PSYM_ENUMMODULES_CALLBACK
 - dbghelp/PSYM_ENUMMODULES_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - DbgHelp.h
api_name:
 - SymEnumerateModulesProc64
---

# PSYM_ENUMMODULES_CALLBACK callback function


## -description

An application-defined callback function used with the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symenumeratemodules">SymEnumerateModules64</a> function. It is called once for each enumerated module, and receives the module information.

The <b>PSYM_ENUMMODULES_CALLBACK64</b> and <b>PSYM_ENUMMODULES_CALLBACKW64</b> types define a pointer to this callback function. 
<b>SymEnumerateModulesProc64</b> is a placeholder for the application-defined function name.

## -parameters

### -param ModuleName [in]

The name of the module.

### -param BaseOfDll [in]

The base address where the module is loaded into memory.

### -param UserContext [in, optional]

The user-defined value specified in 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symenumeratemodules">SymEnumerateModules64</a>, or <b>NULL</b>. Typically, this parameter is used by an application to pass a pointer to a data structure that lets the callback function establish some type of context.

## -returns

If the return value is <b>TRUE</b>, the enumeration will continue.

If the return value is <b>FALSE</b>, the enumeration will stop.

## -remarks

The calling application is called once per module until all modules are enumerated, or until the enumeration callback function returns <b>FALSE</b>.

This callback function supersedes the <i>PSYM_ENUMMODULES_CALLBACK</i> callback function.  <i>PSYM_ENUMMODULES_CALLBACK</i> is defined as follows in DbgHelp.h. 


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define PSYM_ENUMMODULES_CALLBACK PSYM_ENUMMODULES_CALLBACK64
#else
typedef BOOL
(CALLBACK *PSYM_ENUMMODULES_CALLBACK)(
    __in PCSTR ModuleName,
    __in ULONG BaseOfDll,
    __in_opt PVOID UserContext
    );
#endif
```

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symenumeratemodules">SymEnumerateModules64</a>
