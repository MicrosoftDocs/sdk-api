---
UID: NF:dbghelp.SymSetScopeFromAddr
title: SymSetScopeFromAddr function (dbghelp.h)
description: Sets the local scope to the symbol that matches the specified address.
helpviewer_keywords: ["SymSetScopeFromAddr","SymSetScopeFromAddr function","base.symsetscopefromaddr","dbghelp/SymSetScopeFromAddr"]
old-location: base\symsetscopefromaddr.htm
tech.root: Debug
ms.assetid: 7f7bcf12-8d8d-4dea-8191-4f7b24be1b5a
ms.date: 12/05/2018
ms.keywords: SymSetScopeFromAddr, SymSetScopeFromAddr function, base.symsetscopefromaddr, dbghelp/SymSetScopeFromAddr
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
 - SymSetScopeFromAddr
 - dbghelp/SymSetScopeFromAddr
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
 - SymSetScopeFromAddr
---

# SymSetScopeFromAddr function


## -description

Sets the local scope to the symbol that matches the specified address.

## -parameters

### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param Address [in]

The address.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.
						

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetscope">SymGetScope</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symsetscopefromindex">SymSetScopeFromIndex</a>