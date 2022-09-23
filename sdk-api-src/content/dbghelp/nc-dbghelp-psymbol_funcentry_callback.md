---
UID: NC:dbghelp.PSYMBOL_FUNCENTRY_CALLBACK
title: PSYMBOL_FUNCENTRY_CALLBACK (dbghelp.h)
description: PSYMBOL_FUNCENTRY_CALLBACK (dbghelp.h) is an application-defined callback function used with the SymRegisterFunctionEntryCallback64 function.
helpviewer_keywords: ["PSYMBOL_FUNCENTRY_CALLBACK","PSYMBOL_FUNCENTRY_CALLBACK64","SymRegisterFunctionEntryCallbackProc64","SymRegisterFunctionEntryCallbackProc64 callback","SymRegisterFunctionEntryCallbackProc64 callback function","_win32_symregisterfunctionentrycallbackproc64","base.symregisterfunctionentrycallbackproc64","dbghelp/SymRegisterFunctionEntryCallbackProc64"]
old-location: base\symregisterfunctionentrycallbackproc64.htm
tech.root: Debug
ms.assetid: cd10dfeb-451f-4d6d-ae1c-ecca75f86f3d
ms.date: 08/03/2022
ms.keywords: PSYMBOL_FUNCENTRY_CALLBACK, PSYMBOL_FUNCENTRY_CALLBACK64, SymRegisterFunctionEntryCallbackProc64, SymRegisterFunctionEntryCallbackProc64 callback, SymRegisterFunctionEntryCallbackProc64 callback function, _win32_symregisterfunctionentrycallbackproc64, base.symregisterfunctionentrycallbackproc64, dbghelp/SymRegisterFunctionEntryCallbackProc64
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
 - PSYMBOL_FUNCENTRY_CALLBACK
 - dbghelp/PSYMBOL_FUNCENTRY_CALLBACK
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
 - SymRegisterFunctionEntryCallbackProc64
---

# PSYMBOL_FUNCENTRY_CALLBACK callback function


## -description

An application-defined callback function used with the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symregisterfunctionentrycallback">SymRegisterFunctionEntryCallback64</a> function. It is called by the stack walking procedure.

The <b>PSYMBOL_FUNCENTRY_CALLBACK64</b> type defines a pointer to this callback function. 
<b>SymRegisterFunctionEntryCallbackProc64</b> is a placeholder for the application-defined function name.

## -parameters

### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-stackwalk">StackWalk64</a> function.

### -param AddrBase [in]

The address of an instruction for which the callback function should return a function table entry.

### -param UserContext [in, optional]

The user-defined value specified in 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symregisterfunctionentrycallback">SymRegisterFunctionEntryCallback64</a>, or <b>NULL</b>. Typically, this parameter is used by an application to pass a pointer to a data structure that lets the callback function establish some context.

## -returns

Return the value <b>NULL</b> if no function table entry is available.

On success, return a pointer to an <b>IMAGE_RUNTIME_FUNCTION_ENTRY</b> structure. Refer to the header file WinNT.h for the definition of this function.

## -remarks

The structure must be returned in exactly the form it exists in the process being debugged. Some members may be pointers to other locations in the process address space. The 
<a href="/windows/desktop/api/dbghelp/nc-dbghelp-pread_process_memory_routine">ReadProcessMemoryProc64</a> callback function may be called to retrieve the information at these locations.

The calling application gets called through the registered callback function as a result of a call to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-stackwalk">StackWalk64</a> function. The calling application must be prepared for the possible side effects that this can cause. If the application has only one callback function that is being used by multiple threads, then it may be necessary to synchronize some types of data access while in the context of the callback function.

This function is similar to the 
<a href="/windows/desktop/api/dbghelp/nc-dbghelp-pfunction_table_access_routine">FunctionTableAccessProc64</a> callback function. The difference is that 
<b>FunctionTableAccessProc64</b> returns an 
<a href="/windows/desktop/api/winnt/ns-winnt-image_function_entry">IMAGE_FUNCTION_ENTRY</a> structure, while this function returns an <b>IMAGE_RUNTIME_FUNCTION_ENTRY</b> structure.

This callback function supersedes the <i>PSYMBOL_FUNCENTRY_CALLBACK</i> callback function.  <i>PSYMBOL_FUNCENTRY_CALLBACK</i> is defined as follows in Dbghelp.h.


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define PSYMBOL_FUNCENTRY_CALLBACK PSYMBOL_FUNCENTRY_CALLBACK64
#endif

typedef
PVOID
(CALLBACK *PSYMBOL_FUNCENTRY_CALLBACK)(
    __in HANDLE hProcess,
    __in DWORD AddrBase,
    __in_opt PVOID UserContext
    );
```

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symregisterfunctionentrycallback">SymRegisterFunctionEntryCallback64</a>
