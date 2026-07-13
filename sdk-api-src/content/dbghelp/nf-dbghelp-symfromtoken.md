---
UID: NF:dbghelp.SymFromToken
title: SymFromToken function (dbghelp.h)
description: The SymFromToken function (dbghelp.h) retrieves symbol information for the specified managed code token.
helpviewer_keywords: ["SymFromToken","SymFromToken function","SymFromTokenW","base.symfromtoken","dbghelp/SymFromToken","dbghelp/SymFromTokenW"]
old-location: base\symfromtoken.htm
tech.root: Debug
ms.assetid: ecef5213-9301-4ca0-852c-1e6be0d7b2a5
ms.date: 08/04/2022
ms.keywords: SymFromToken, SymFromToken function, SymFromTokenW, base.symfromtoken, dbghelp/SymFromToken, dbghelp/SymFromTokenW
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymFromTokenW (Unicode) and SymFromToken (ANSI)
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
req.redist: DbgHelp.dll 6.1 or later
ms.custom: 19H1
f1_keywords:
 - SymFromToken
 - dbghelp/SymFromToken
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
 - SymFromToken
 - SymFromToken
 - SymFromTokenW
---

# SymFromToken function


## -description

Retrieves symbol information for the specified managed code token.

## -parameters

### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param Base [in]

The base address of the managed code module.

### -param Token [in]

The managed code token.

### -param Symbol [in, out]

A pointer to a 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-symbol_info">SYMBOL_INFO</a> structure that provides information about the symbol.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-symbol_info">SYMBOL_INFO</a>
