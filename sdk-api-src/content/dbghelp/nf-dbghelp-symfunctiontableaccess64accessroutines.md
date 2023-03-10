---
UID: NF:dbghelp.SymFunctionTableAccess64AccessRoutines
title: SymFunctionTableAccess64AccessRoutines function (dbghelp.h)
description: Finds a function table entry or frame pointer omission (FPO) record for an address.
helpviewer_keywords: ["SymFunctionTableAccess64AccessRoutines","SymFunctionTableAccess64AccessRoutines function","base.symfunctiontableaccess64accessroutines","dbghelp/SymFunctionTableAccess64AccessRoutines"]
old-location: base\symfunctiontableaccess64accessroutines.htm
tech.root: Debug
ms.assetid: 7AE8779A-F3F8-45FF-B11C-4D48CF76FDCA
ms.date: 12/05/2018
ms.keywords: SymFunctionTableAccess64AccessRoutines, SymFunctionTableAccess64AccessRoutines function, base.symfunctiontableaccess64accessroutines, dbghelp/SymFunctionTableAccess64AccessRoutines
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
req.lib: DbgHelp.lib
req.dll: DbgHelp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.2 or later
ms.custom: 19H1
f1_keywords:
 - SymFunctionTableAccess64AccessRoutines
 - dbghelp/SymFunctionTableAccess64AccessRoutines
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - DbgHelp.dll
api_name:
 - SymFunctionTableAccess64AccessRoutines
---

# SymFunctionTableAccess64AccessRoutines function


## -description

 Finds a function table entry or  frame pointer omission (FPO) record for an address.

Use <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symfunctiontableaccess">SymFunctionTableAccess64</a> instead.

## -parameters

### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param AddrBase [in]

The base address for which function table information is required.

### -param ReadMemoryRoutine [in, optional]

Pointer to a read memory callback function.

### -param GetModuleBaseRoutine [in, optional]

Pointer to a get module base callback function.

## -see-also

<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a>