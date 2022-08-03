---
UID: NC:dbghelp.PENUMLOADED_MODULES_CALLBACK
title: PENUMLOADED_MODULES_CALLBACK (dbghelp.h)
description: PENUMLOADED_MODULES_CALLBACK (dbghelp.h) is an application-defined callback function used with the EnumerateLoadedModules64 function.
helpviewer_keywords: ["EnumerateLoadedModulesProc64","EnumerateLoadedModulesProc64 callback","EnumerateLoadedModulesProc64 callback function","PENUMLOADED_MODULES_CALLBACK","PENUMLOADED_MODULES_CALLBACK64","PENUMLOADED_MODULES_CALLBACKW64","_win32_enumerateloadedmodulesproc64","base.enumerateloadedmodulesproc64","dbghelp/EnumerateLoadedModulesProc64"]
old-location: base\enumerateloadedmodulesproc64.htm
tech.root: Debug
ms.assetid: f6acb9cf-81f7-4b05-95e2-9628855f6b51
ms.date: 08/03/2022
ms.keywords: EnumerateLoadedModulesProc64, EnumerateLoadedModulesProc64 callback, EnumerateLoadedModulesProc64 callback function, PENUMLOADED_MODULES_CALLBACK, PENUMLOADED_MODULES_CALLBACK64, PENUMLOADED_MODULES_CALLBACKW64, _win32_enumerateloadedmodulesproc64, base.enumerateloadedmodulesproc64, dbghelp/EnumerateLoadedModulesProc64
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
 - PENUMLOADED_MODULES_CALLBACK
 - dbghelp/PENUMLOADED_MODULES_CALLBACK
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
 - EnumerateLoadedModulesProc64
---

# PENUMLOADED_MODULES_CALLBACK callback function


## -description

An application-defined callback function used with the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-enumerateloadedmodules">EnumerateLoadedModules64</a> function.

The <b>PENUMLOADED_MODULES_CALLBACK64</b> and <b>PENUMLOADED_MODULES_CALLBACKW64</b> types define a pointer to this callback function. 
<i>EnumerateLoadedModulesProc64</i> is a placeholder for the application-defined function name.

## -parameters

### -param ModuleName [in]

The name of the enumerated module.

### -param ModuleBase [in]

The base address of the module. Note that it is possible for this address to become invalid (for example, the module may be unloaded). Use exception handling when accessing the address or passing the address to another function to prevent an access violation from occurring.

### -param ModuleSize [in]

The size of the module, in bytes.

### -param UserContext [in, optional]

Optional user-defined data. This value is passed from 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-enumerateloadedmodules">EnumerateLoadedModules64</a>.

## -returns

To continue enumeration, the callback function must return <b>TRUE</b>.

To stop enumeration, the callback function must return <b>FALSE</b>.

## -remarks

This callback function supersedes the <i>PENUMLOADED_MODULES_CALLBACK</i> callback function. <i>PENUMLOADED_MODULES_CALLBACK</i> is defined as follows in DbgHelp.h. 


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define PENUMLOADED_MODULES_CALLBACK PENUMLOADED_MODULES_CALLBACK64
#else
typedef BOOL (CALLBACK *PENUMLOADED_MODULES_CALLBACK)(
    __in PCSTR ModuleName,
    __in ULONG ModuleBase,
    __in ULONG ModuleSize,
    __in_opt PVOID UserContext
    );
#endif
```

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-enumerateloadedmodules">EnumerateLoadedModules64</a>
