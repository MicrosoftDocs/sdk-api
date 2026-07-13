---
UID: NF:dbghelp.SymFromNameW
title: SymFromNameW function (dbghelp.h)
description: The SymFromNameW (Unicode) function retrieves symbol information for the specified name.
helpviewer_keywords: ["SymFromName","SymFromName function","SymFromNameW","_win32_symfromname","base.symfromname","dbghelp/SymFromName","dbghelp/SymFromNameW"]
old-location: base\symfromname.htm
tech.root: Debug
ms.assetid: 26b9eba7-2038-4640-aeb2-3052889b14ea
ms.date: 08/04/2022
ms.keywords: SymFromName, SymFromName function, SymFromNameW, _win32_symfromname, base.symfromname, dbghelp/SymFromName, dbghelp/SymFromNameW
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymFromNameW (Unicode) and SymFromName (ANSI)
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
 - SymFromNameW
 - dbghelp/SymFromNameW
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
 - SymFromName
 - SymFromName
 - SymFromNameW
---

# SymFromNameW function


## -description

Retrieves symbol information for the specified name.

## -parameters

### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param Name [in]

The name of the symbol to be located.

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


#### Examples

For an example, see 
<a href="/windows/desktop/Debug/retrieving-symbol-information-by-name">Retrieving Symbol Information by Name</a>.

<div class="code"></div>




> [!NOTE]
> The dbghelp.h header defines SymFromName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-symbol_info">SYMBOL_INFO</a>
