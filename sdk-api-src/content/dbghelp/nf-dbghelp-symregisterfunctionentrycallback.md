---
UID: NF:dbghelp.SymRegisterFunctionEntryCallback
title: SymRegisterFunctionEntryCallback function (dbghelp.h)
description: Registers a callback function for use by the stack walking procedure on Alpha computers. (SymRegisterFunctionEntryCallback)
helpviewer_keywords: ["SymRegisterFunctionEntryCallback","SymRegisterFunctionEntryCallback function","SymRegisterFunctionEntryCallback64","SymRegisterFunctionEntryCallback64 function","_win32_symregisterfunctionentrycallback64","base.symregisterfunctionentrycallback64","dbghelp/SymRegisterFunctionEntryCallback","dbghelp/SymRegisterFunctionEntryCallback64"]
old-location: base\symregisterfunctionentrycallback64.htm
tech.root: Debug
ms.assetid: 5915055f-2c6c-4a0e-ad0f-c5bd74558802
ms.date: 12/05/2018
ms.keywords: SymRegisterFunctionEntryCallback, SymRegisterFunctionEntryCallback function, SymRegisterFunctionEntryCallback64, SymRegisterFunctionEntryCallback64 function, _win32_symregisterfunctionentrycallback64, base.symregisterfunctionentrycallback64, dbghelp/SymRegisterFunctionEntryCallback, dbghelp/SymRegisterFunctionEntryCallback64
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
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - SymRegisterFunctionEntryCallback
 - dbghelp/SymRegisterFunctionEntryCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dbghelp.dll
 - imagehlp.dll
api_name:
 - SymRegisterFunctionEntryCallback64
 - SymRegisterFunctionEntryCallback
---

# SymRegisterFunctionEntryCallback function


## -description

Registers a callback function for use by the stack walking procedure on Alpha computers.

## -parameters

### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-stackwalk">StackWalk64</a> function.

### -param CallbackFunction [in]

A <a href="/windows/desktop/api/dbghelp/nc-dbghelp-psymbol_funcentry_callback">SymRegisterFunctionEntryCallbackProc64</a> callback function.

### -param UserContext [in]

A user-defined value or <b>NULL</b>. This value is simply passed to the callback function. Normally, this parameter is used by an application to pass a pointer to a data structure that lets the callback function establish some context.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>SymRegisterFunctionEntryCallback64</b> function lets an application register a callback function for use by the stack walking procedure. The stack walking procedure calls the registered callback function when it is unable to locate a function table entry for an address. In most cases, the stack walking procedure locates the function table entries in the function table of the image containing the address. However, in situations where the function table entries are not in the image, this callback allows the debugger to provide the function table entry from another source. For example, run-time generated code on Alpha computers can define dynamic function tables to support exception handling and stack tracing.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

This function supersedes the <b>SymRegisterFunctionEntryCallback</b> function. For more information, see 
<a href="/windows/desktop/Debug/updated-platform-support">Updated Platform Support</a>. <b>SymRegisterFunctionEntryCallback</b> is defined as follows in Dbghelp.h. 


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define SymRegisterFunctionEntryCallback SymRegisterFunctionEntryCallback64
#else
BOOL
IMAGEAPI
SymRegisterFunctionEntryCallback(
    __in HANDLE hProcess,
    __in PSYMBOL_FUNCENTRY_CALLBACK CallbackFunction,
    __in_opt PVOID UserContext
    );
#endif
```

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-stackwalk">StackWalk64</a>



<a href="/windows/desktop/api/dbghelp/nc-dbghelp-psymbol_funcentry_callback">SymRegisterFunctionEntryCallbackProc64</a>
