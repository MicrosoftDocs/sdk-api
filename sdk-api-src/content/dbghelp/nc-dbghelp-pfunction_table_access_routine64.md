---
UID: NC:dbghelp.PFUNCTION_TABLE_ACCESS_ROUTINE64
title: PFUNCTION_TABLE_ACCESS_ROUTINE64 (dbghelp.h)
description: PFUNCTION_TABLE_ACCESS_ROUTINE64 (dbghelp.h) is an application-defined callback function used with the StackWalk64 function.
helpviewer_keywords: ["FunctionTableAccessProc64","FunctionTableAccessProc64 callback","FunctionTableAccessProc64 callback function","PFUNCTION_TABLE_ACCESS_ROUTINE","PFUNCTION_TABLE_ACCESS_ROUTINE64","_win32_functiontableaccessproc64","base.functiontableaccessproc64","dbghelp/FunctionTableAccessProc64"]
old-location: base\functiontableaccessproc64.htm
tech.root: Debug
ms.assetid: 387c20b0-ed16-463c-8b11-3ac9a43548a1
ms.date: 08/03/2022
ms.keywords: FunctionTableAccessProc64, FunctionTableAccessProc64 callback, FunctionTableAccessProc64 callback function, PFUNCTION_TABLE_ACCESS_ROUTINE, PFUNCTION_TABLE_ACCESS_ROUTINE64, _win32_functiontableaccessproc64, base.functiontableaccessproc64, dbghelp/FunctionTableAccessProc64
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
 - PFUNCTION_TABLE_ACCESS_ROUTINE64
 - dbghelp/PFUNCTION_TABLE_ACCESS_ROUTINE64
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
 - FunctionTableAccessProc64
---

# PFUNCTION_TABLE_ACCESS_ROUTINE64 callback function

## -description

An application-defined callback function used with the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-stackwalk">StackWalk64</a> function. It provides access to the run-time function table for the process.

The <b>PFUNCTION_TABLE_ACCESS_ROUTINE64</b> type defines a pointer to this callback function. 
<b>FunctionTableAccessProc64</b> is a placeholder for the application-defined function name.

## -parameters

### -param ahProcess [in]

A handle to the process for which the stack trace is generated.

### -param AddrBase [in]

The address of the instruction to be located.

## -returns

The function returns a pointer to the run-time function table. On an x86 computer, this is a pointer to an 
<a href="/windows/desktop/api/winnt/ns-winnt-fpo_data">FPO_DATA</a> structure. On an Alpha computer, this is a pointer to an 
<a href="/windows/desktop/api/winnt/ns-winnt-image_function_entry">IMAGE_FUNCTION_ENTRY</a> structure.

## -remarks

This callback function supersedes the <i>PFUNCTION_TABLE_ACCESS_ROUTINE</i> callback function.  <i>PFUNCTION_TABLE_ACCESS_ROUTINE</i> is defined as follows in DbgHelp.h. 


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define PFUNCTION_TABLE_ACCESS_ROUTINE PFUNCTION_TABLE_ACCESS_ROUTINE64
#else
typedef
PVOID
(__stdcall *PFUNCTION_TABLE_ACCESS_ROUTINE)(
    __in HANDLE hProcess,
    __in DWORD AddrBase
    );
#endif
```

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/winnt/ns-winnt-fpo_data">FPO_DATA</a>



<a href="/windows/desktop/api/winnt/ns-winnt-image_function_entry">IMAGE_FUNCTION_ENTRY</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-stackwalk">StackWalk64</a>
