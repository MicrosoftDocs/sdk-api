---
UID: NF:dbghelp.SymRegisterCallback64
title: SymRegisterCallback64 function (dbghelp.h)
description: Registers a callback function for use by the symbol handler. (SymRegisterCallback64)
helpviewer_keywords: ["SymRegisterCallback","SymRegisterCallback function","SymRegisterCallback64","SymRegisterCallback64 function","SymRegisterCallbackW64","_win32_symregistercallback64","base.symregistercallback64","dbghelp/SymRegisterCallback","dbghelp/SymRegisterCallback64","dbghelp/SymRegisterCallbackW64"]
old-location: base\symregistercallback64.htm
tech.root: Debug
ms.assetid: 91d123cd-f68f-4120-b98d-7e3f94b7b1ec
ms.date: 12/05/2018
ms.keywords: SymRegisterCallback, SymRegisterCallback function, SymRegisterCallback64, SymRegisterCallback64 function, SymRegisterCallbackW64, _win32_symregistercallback64, base.symregistercallback64, dbghelp/SymRegisterCallback, dbghelp/SymRegisterCallback64, dbghelp/SymRegisterCallbackW64
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymRegisterCallbackW64 (Unicode) and SymRegisterCallback64 (ANSI)
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
 - SymRegisterCallback64
 - dbghelp/SymRegisterCallback64
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
 - SymRegisterCallback64
 - SymRegisterCallback64
 - SymRegisterCallbackW64
 - SymRegisterCallback
---

# SymRegisterCallback64 function


## -description

Registers a callback function for use by the symbol handler.

## -parameters

### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param CallbackFunction [in]

A <a href="/windows/desktop/api/dbghelp/nc-dbghelp-psymbol_registered_callback">SymRegisterCallbackProc64</a> callback function.

### -param UserContext [in]

A user-defined value or <b>NULL</b>. This value is simply passed to the callback function. Normally, this parameter is used by an application to pass a pointer to a data structure that lets the callback function establish some context.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>SymRegisterCallback64</b> function lets an application register a callback function for use by the symbol handler. The symbol handler calls the registered callback function when there is status or progress information for the application.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR. <b>SymRegisterCallbackW64</b> is defined as follows in Dbghelp.h. 


```cpp
BOOL
IMAGEAPI
SymRegisterCallbackW64(
    __in HANDLE hProcess,
    __in PSYMBOL_REGISTERED_CALLBACK64 CallbackFunction,
    __in ULONG64 UserContext
    );

#ifdef DBGHELP_TRANSLATE_TCHAR
#define SymRegisterCallback64   SymRegisterCallbackW64
#endif
```


This function supersedes the <b>SymRegisterCallback</b> function. For more information, see 
<a href="/windows/desktop/Debug/updated-platform-support">Updated Platform Support</a>. <b>SymRegisterCallback</b> is defined as follows in Dbghelp.h. 


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define SymRegisterCallback SymRegisterCallback64
#else
BOOL
IMAGEAPI
SymRegisterCallback(
    __in HANDLE hProcess,
    __in PSYMBOL_REGISTERED_CALLBACK CallbackFunction,
    __in_opt PVOID UserContext
    );
#endif
```


For a more extensive example, read <a href="/windows/desktop/Debug/getting-notifications">Getting Notifications</a>.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/Debug/getting-notifications">Getting Notifications</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a>



<a href="/windows/desktop/api/dbghelp/nc-dbghelp-psymbol_registered_callback">SymRegisterCallbackProc64</a>
