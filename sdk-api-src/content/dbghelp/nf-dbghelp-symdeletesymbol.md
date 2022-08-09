---
UID: NF:dbghelp.SymDeleteSymbol
title: SymDeleteSymbol function (dbghelp.h)
description: The SymDeleteSymbol function (dbghelp.h) deletes a virtual symbol from the specified module.
helpviewer_keywords: ["SymDeleteSymbol","SymDeleteSymbol function","SymDeleteSymbolW","_win32_symdeletesymbol","base.symdeletesymbol","dbghelp/SymDeleteSymbol","dbghelp/SymDeleteSymbolW"]
old-location: base\symdeletesymbol.htm
tech.root: Debug
ms.assetid: 9fc5a19d-5984-4d0a-a3d6-3da474055f5e
ms.date: 08/04/2022
ms.keywords: SymDeleteSymbol, SymDeleteSymbol function, SymDeleteSymbolW, _win32_symdeletesymbol, base.symdeletesymbol, dbghelp/SymDeleteSymbol, dbghelp/SymDeleteSymbolW
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymDeleteSymbolW (Unicode) and SymDeleteSymbol (ANSI)
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
req.redist: DbgHelp.dll 6.0 or later
ms.custom: 19H1
f1_keywords:
 - SymDeleteSymbol
 - dbghelp/SymDeleteSymbol
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
 - SymDeleteSymbol
 - SymDeleteSymbol
 - SymDeleteSymbolW
---

# SymDeleteSymbol function


## -description

Deletes a virtual symbol from the specified module.

## -parameters

### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param BaseOfDll [in]

The base address of the module.

### -param Name [in, optional]

The name of the symbol.

### -param Address [in]

The address of the symbol. This address must be within the address range of the specified module.

### -param Flags [in]

This parameter is unused.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symaddsymbol">SymAddSymbol</a>
