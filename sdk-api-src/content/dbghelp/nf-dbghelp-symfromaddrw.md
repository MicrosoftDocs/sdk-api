---
UID: NF:dbghelp.SymFromAddrW
title: SymFromAddrW function (dbghelp.h)
description: The SymFromAddrW (Unicode) function retrieves symbol information for the specified address.
helpviewer_keywords: ["SymFromAddr","SymFromAddr function","SymFromAddrW","_win32_symfromaddr","base.symfromaddr","dbghelp/SymFromAddr","dbghelp/SymFromAddrW"]
old-location: base\symfromaddr.htm
tech.root: Debug
ms.assetid: 20338631-19ab-4ad8-9ba2-56fa4812b33e
ms.date: 08/04/2022
ms.keywords: SymFromAddr, SymFromAddr function, SymFromAddrW, _win32_symfromaddr, base.symfromaddr, dbghelp/SymFromAddr, dbghelp/SymFromAddrW
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymFromAddrW (Unicode) and SymFromAddr (ANSI)
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
 - SymFromAddrW
 - dbghelp/SymFromAddrW
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
 - SymFromAddr
 - SymFromAddr
 - SymFromAddrW
---

# SymFromAddrW function


## -description

Retrieves symbol information for the specified address.

## -parameters

### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param Address [in]

The address for which a symbol should be located. The address does not have to be on a symbol boundary. If the address comes after the beginning of a symbol and before the end of the symbol, the symbol is found.

### -param Displacement [out, optional]

The displacement from the beginning of the symbol, or zero.

### -param Symbol [in, out]

A pointer to a 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-symbol_info">SYMBOL_INFO</a> structure that provides information about the symbol. The symbol name is variable in length; therefore this buffer must be large enough to hold the name stored at the end of the 
<b>SYMBOL_INFO</b> structure. Be sure to set the <b>MaxNameLen</b> member to the number of bytes reserved for the name.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.


#### Examples

For an example, see 
<a href="/windows/desktop/Debug/retrieving-symbol-information-by-address">Retrieving Symbol Information by Address</a>.

<div class="code"></div>




> [!NOTE]
> The dbghelp.h header defines SymFromAddr as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-symbol_info">SYMBOL_INFO</a>
