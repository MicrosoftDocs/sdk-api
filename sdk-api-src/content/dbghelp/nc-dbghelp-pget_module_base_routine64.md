---
UID: NC:dbghelp.PGET_MODULE_BASE_ROUTINE64
title: PGET_MODULE_BASE_ROUTINE64 (dbghelp.h)
description: PGET_MODULE_BASE_ROUTINE64 (dbghelp.h) is an application-defined callback function used with the StackWalk64 function.
helpviewer_keywords: ["GetModuleBaseProc64","GetModuleBaseProc64 callback","GetModuleBaseProc64 callback function","PGET_MODULE_BASE_ROUTINE","PGET_MODULE_BASE_ROUTINE64","_win32_getmodulebaseproc64","base.getmodulebaseproc64","dbghelp/GetModuleBaseProc64"]
old-location: base\getmodulebaseproc64.htm
tech.root: Debug
ms.assetid: a1060d41-183f-4cb1-8214-afef2996ca66
ms.date: 08/03/2022
ms.keywords: GetModuleBaseProc64, GetModuleBaseProc64 callback, GetModuleBaseProc64 callback function, PGET_MODULE_BASE_ROUTINE, PGET_MODULE_BASE_ROUTINE64, _win32_getmodulebaseproc64, base.getmodulebaseproc64, dbghelp/GetModuleBaseProc64
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
 - PGET_MODULE_BASE_ROUTINE64
 - dbghelp/PGET_MODULE_BASE_ROUTINE64
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
 - GetModuleBaseProc64
---

# PGET_MODULE_BASE_ROUTINE64 callback function


## -description

An application-defined callback function used with the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-stackwalk">StackWalk64</a> function. It is called when 
<b>StackWalk64</b> needs a module base address for a given virtual address.

The <b>PGET_MODULE_BASE_ROUTINE64</b> type defines a pointer to this callback function. 
<b>GetModuleBaseProc64</b> is a placeholder for the application-defined function name.

## -parameters

### -param hProcess [in]

A handle to the process for which the stack trace is generated.

### -param Address [in]

An address within the module image to be located.

## -returns

The function returns the base address of the module.

## -remarks

This callback function supersedes the <i>PGET_MODULE_BASE_ROUTINE</i> callback function.  <i>PGET_MODULE_BASE_ROUTINE</i> is defined as follows in DbgHelp.h. 


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define PGET_MODULE_BASE_ROUTINE PGET_MODULE_BASE_ROUTINE64
#else
typedef
DWORD
(__stdcall *PGET_MODULE_BASE_ROUTINE)(
    __in HANDLE hProcess,
    __in DWORD Address
    );
#endif
```

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-stackwalk">StackWalk64</a>
