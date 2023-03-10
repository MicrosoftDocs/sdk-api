---
UID: NF:dbghelp.SymFunctionTableAccess
title: SymFunctionTableAccess function (dbghelp.h)
description: Retrieves the function table entry for the specified address. (SymFunctionTableAccess)
helpviewer_keywords: ["SymFunctionTableAccess","SymFunctionTableAccess function","SymFunctionTableAccess64","SymFunctionTableAccess64 function","_win32_symfunctiontableaccess64","base.symfunctiontableaccess64","dbghelp/SymFunctionTableAccess","dbghelp/SymFunctionTableAccess64"]
old-location: base\symfunctiontableaccess64.htm
tech.root: Debug
ms.assetid: f79e6af9-9931-4bd7-ae12-29d890267a89
ms.date: 12/05/2018
ms.keywords: SymFunctionTableAccess, SymFunctionTableAccess function, SymFunctionTableAccess64, SymFunctionTableAccess64 function, _win32_symfunctiontableaccess64, base.symfunctiontableaccess64, dbghelp/SymFunctionTableAccess, dbghelp/SymFunctionTableAccess64
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
 - SymFunctionTableAccess
 - dbghelp/SymFunctionTableAccess
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
 - SymFunctionTableAccess64
 - SymFunctionTableAccess
---

# SymFunctionTableAccess function


## -description

Retrieves the function table entry for the specified address.

## -parameters

### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param AddrBase [in]

The base address for which function table information is required.

## -returns

If the function succeeds, the return value is a pointer to the function table entry.

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The type of pointer returned is specific to the image from which symbols are loaded. 

<b>x86:  </b>If the image is for an x86 system, this is a pointer to an 
<a href="/windows/desktop/api/winnt/ns-winnt-fpo_data">FPO_DATA</a> structure.

<b>x64:  </b>If the image is for an x64 system, this is a pointer to an <a href="/windows/win32/api/winnt/ns-winnt-runtime_function">_IMAGE_RUNTIME_FUNCTION_ENTRY</a> structure.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

This function supersedes the <b>SymFunctionTableAccess</b> function. For more information, see 
<a href="/windows/desktop/Debug/updated-platform-support">Updated Platform Support</a>. <b>SymFunctionTableAccess</b> is defined as follows in Dbghelp.h. 


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define SymFunctionTableAccess SymFunctionTableAccess64
#else
PVOID
IMAGEAPI
SymFunctionTableAccess(
    __in HANDLE hProcess,
    __in DWORD AddrBase
    );
#endif
```

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/winnt/ns-winnt-fpo_data">FPO_DATA</a>



<a href="/windows/desktop/api/winnt/ns-winnt-image_function_entry">IMAGE_FUNCTION_ENTRY</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a>



<a href="/windows/win32/api/winnt/ns-winnt-runtime_function">_IMAGE_RUNTIME_FUNCTION_ENTRY</a>
