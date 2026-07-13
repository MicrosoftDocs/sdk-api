---
UID: NF:dbghelp.SymGetModuleBase64
title: SymGetModuleBase64 function (dbghelp.h)
description: Retrieves the base address of the module that contains the specified address. (SymGetModuleBase64)
helpviewer_keywords: ["SymGetModuleBase","SymGetModuleBase function","SymGetModuleBase64","SymGetModuleBase64 function","_win32_symgetmodulebase64","base.symgetmodulebase64","dbghelp/SymGetModuleBase","dbghelp/SymGetModuleBase64"]
old-location: base\symgetmodulebase64.htm
tech.root: Debug
ms.assetid: 964d0fdb-d982-4509-8c49-0ad0a3491226
ms.date: 12/05/2018
ms.keywords: SymGetModuleBase, SymGetModuleBase function, SymGetModuleBase64, SymGetModuleBase64 function, _win32_symgetmodulebase64, base.symgetmodulebase64, dbghelp/SymGetModuleBase, dbghelp/SymGetModuleBase64
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
 - SymGetModuleBase64
 - dbghelp/SymGetModuleBase64
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
 - SymGetModuleBase64
 - SymGetModuleBase
---

# SymGetModuleBase64 function

## -description

Retrieves the base address of the module that contains the specified address.

## -parameters

### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param qwAddr [in]

The virtual address that is contained in one of the modules loaded by the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symloadmodule">SymLoadModule64</a> function.

## -returns

If the function succeeds, the return value is a nonzero virtual address. The value is the base address of the module containing the address specified by the <i>dwAddr</i> parameter.

If the function fails, the return value is zero. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The module table is searched for a module that contains <i>dwAddr</i>. The module is located based on the load address and size of each module.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

This function supersedes the <b>SymGetModuleBase</b> function. For more information, see 
<a href="/windows/desktop/Debug/updated-platform-support">Updated Platform Support</a>. <b>SymGetModuleBase</b> is defined as follows in DbgHelp.h. 


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define SymGetModuleBase SymGetModuleBase64
#else
DWORD
IMAGEAPI
SymGetModuleBase(
    __in HANDLE hProcess,
    __in DWORD dwAddr
    );
#endif
```

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symloadmodule">SymLoadModule64</a>
