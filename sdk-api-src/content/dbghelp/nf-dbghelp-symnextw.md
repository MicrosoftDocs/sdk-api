---
UID: NF:dbghelp.SymNextW
title: SymNextW function (dbghelp.h)
description: The SymNextW (Unicode) function retrieves symbol information for the next symbol.
helpviewer_keywords: ["SymNext","SymNext function","SymNextW","base.symnext","dbghelp/SymNext","dbghelp/SymNextW"]
old-location: base\symnext.htm
tech.root: Debug
ms.assetid: ffd2d416-7149-4a4c-a1d5-7a7f3bdf5dc4
ms.date: 08/04/2022
ms.keywords: SymNext, SymNext function, SymNextW, base.symnext, dbghelp/SymNext, dbghelp/SymNextW
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymNextW (Unicode) and SymNext (ANSI)
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
req.redist: DbgHelp.dll 6.2 or later
ms.custom: 19H1
f1_keywords:
 - SymNextW
 - dbghelp/SymNextW
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
 - SymNext
 - SymNext
 - SymNextW
---

## -description

Retrieves symbol information for the next symbol.

## -parameters

### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param siw [in, out]

A pointer to a 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-symbol_info">SYMBOL_INFO</a> structure that provides information about the current symbol. Upon return, the structure contains information about the next symbol.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.
						

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function requires that the <a href="/windows/desktop/api/dbghelp/ns-dbghelp-symbol_info">SYMBOL_INFO</a> structure have valid data for the current symbol. The next symbol is the symbol with the virtual address that is next in the sequence.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.





> [!NOTE]
> The dbghelp.h header defines SymNext as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-symbol_info">SYMBOL_INFO</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symprev">SymPrev</a>
