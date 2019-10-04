---
UID: NF:dbghelp.SymFunctionTableAccess64AccessRoutines
title: SymFunctionTableAccess64AccessRoutines function (dbghelp.h)
author: windows-sdk-content
description: Finds a function table entry or frame pointer omission (FPO) record for an address.
old-location: base\symfunctiontableaccess64accessroutines.htm
tech.root: Debug
ms.assetid: 7AE8779A-F3F8-45FF-B11C-4D48CF76FDCA
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SymFunctionTableAccess64AccessRoutines, SymFunctionTableAccess64AccessRoutines function, base.symfunctiontableaccess64accessroutines, dbghelp/SymFunctionTableAccess64AccessRoutines
ms.topic: function
f1_keywords: 
 - "dbghelp/SymFunctionTableAccess64AccessRoutines"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - DbgHelp.dll
api_name:
 - SymFunctionTableAccess64AccessRoutines
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.2 or later
ms.custom: 19H1
---

# SymFunctionTableAccess64AccessRoutines function


## -description


 Finds a function table entry or  frame pointer omission (FPO) record for an address.

Use <a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-symfunctiontableaccess">SymFunctionTableAccess64</a> instead.


## -parameters




### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.


### -param AddrBase [in]

The base address for which function table information is required.


### -param ReadMemoryRoutine [in, optional]

Pointer to a read memory callback function.


### -param GetModuleBaseRoutine [in, optional]

Pointer to a get module base callback function.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a>
 

 

