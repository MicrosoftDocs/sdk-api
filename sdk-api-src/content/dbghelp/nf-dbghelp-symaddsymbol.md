---
UID: NF:dbghelp.SymAddSymbol
title: SymAddSymbol function (dbghelp.h)
description: The SymAddSymbol function (dbghelp.h) adds a virtual symbol to the specified module.
helpviewer_keywords: ["SymAddSymbol","SymAddSymbol function","SymAddSymbolW","_win32_symaddsymbol","base.symaddsymbol","dbghelp/SymAddSymbol","dbghelp/SymAddSymbolW"]
old-location: base\symaddsymbol.htm
tech.root: Debug
ms.assetid: 28405993-035f-4946-91c3-0e3e34fd8824
ms.date: 08/04/2022
ms.keywords: SymAddSymbol, SymAddSymbol function, SymAddSymbolW, _win32_symaddsymbol, base.symaddsymbol, dbghelp/SymAddSymbol, dbghelp/SymAddSymbolW
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymAddSymbolW (Unicode) and SymAddSymbol (ANSI)
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
 - SymAddSymbol
 - dbghelp/SymAddSymbol
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
 - SymAddSymbol
 - SymAddSymbol
 - SymAddSymbolW
---

# SymAddSymbol function


## -description

Adds a virtual symbol
				to the specified module.

## -parameters

### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param BaseOfDll [in]

The base address of the module.

### -param Name [in]

The name of the symbol. The maximum size of a symbol name is MAX_SYM_NAME characters.

### -param Address [in]

The address of the symbol. This address must be within the address range of the specified module.

### -param Size [in]

The size of the symbol, in bytes. This parameter is optional.

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



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symdeletesymbol">SymDeleteSymbol</a>
