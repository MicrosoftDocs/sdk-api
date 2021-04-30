---
UID: NF:dbghelp.SymSetScopeFromIndex
title: SymSetScopeFromIndex function (dbghelp.h)
description: Sets the local scope to the symbol that matches the specified index.
helpviewer_keywords: ["SymSetScopeFromIndex","SymSetScopeFromIndex function","base.symsetscopefromindex","dbghelp/SymSetScopeFromIndex"]
old-location: base\symsetscopefromindex.htm
tech.root: Debug
ms.assetid: 06792478-35e2-4f05-85c9-910909fe65cd
ms.date: 12/05/2018
ms.keywords: SymSetScopeFromIndex, SymSetScopeFromIndex function, base.symsetscopefromindex, dbghelp/SymSetScopeFromIndex
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
req.redist: DbgHelp.dll 6.8 or later
ms.custom: 19H1
f1_keywords:
 - SymSetScopeFromIndex
 - dbghelp/SymSetScopeFromIndex
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
 - SymSetScopeFromIndex
---

# SymSetScopeFromIndex function


## -description

Sets the local scope to the symbol that matches the specified index.

## -parameters

### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param BaseOfDll [in]

The base address of the module.

### -param Index [in]

The unique value for the symbol.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error 
       information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetscope">SymGetScope</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symsetscopefromaddr">SymSetScopeFromAddr</a>