---
UID: NF:dbghelp.SymEnumSymbolsForAddrW
title: SymEnumSymbolsForAddrW function (dbghelp.h)
description: The SymEnumSymbolsForAddrW (Unicode) function enumerates the symbols for the specified address.
helpviewer_keywords: ["SymEnumSymbolsForAddr","SymEnumSymbolsForAddr function","SymEnumSymbolsForAddrW","_win32_symenumsymbolsforaddr","base.symenumsymbolsforaddr","dbghelp/SymEnumSymbolsForAddr","dbghelp/SymEnumSymbolsForAddrW"]
old-location: base\symenumsymbolsforaddr.htm
tech.root: Debug
ms.assetid: 1c622d1d-e7be-4b02-8d6d-68b5f07f2e35
ms.date: 08/04/2022
ms.keywords: SymEnumSymbolsForAddr, SymEnumSymbolsForAddr function, SymEnumSymbolsForAddrW, _win32_symenumsymbolsforaddr, base.symenumsymbolsforaddr, dbghelp/SymEnumSymbolsForAddr, dbghelp/SymEnumSymbolsForAddrW
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymEnumSymbolsForAddrW (Unicode) and SymEnumSymbolsForAddr (ANSI)
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
 - SymEnumSymbolsForAddrW
 - dbghelp/SymEnumSymbolsForAddrW
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
 - SymEnumSymbolsForAddr
 - SymEnumSymbolsForAddr
 - SymEnumSymbolsForAddrW
---

# SymEnumSymbolsForAddrW function


## -description

Enumerates the symbols for the specified address.

## -parameters

### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param Address [in]

The address for which symbols are to be located. The address does not have to be on a symbol boundary. If the address comes after the beginning of a symbol and before the end of the symbol (the beginning of the symbol plus the symbol size), the function will find the symbol.

### -param EnumSymbolsCallback [in]

An application-defined callback function. This function is called for every symbol found at <i>Address</i>. For more information, see 
<a href="/windows/desktop/api/dbghelp/nc-dbghelp-psym_enumeratesymbols_callback">SymEnumSymbolsProc</a>.

### -param UserContext [in, optional]

Optional user-defined data. This value is passed to the callback function.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.





> [!NOTE]
> The dbghelp.h header defines SymEnumSymbolsForAddr as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nc-dbghelp-psym_enumeratesymbols_callback">SymEnumSymbolsProc</a>
