---
UID: NF:dbghelp.SymGetScopeW
title: SymGetScopeW function (dbghelp.h)
description: The SymGetScopeW (Unicode) function retrieves the scope for the specified index.
helpviewer_keywords: ["SymGetScope","SymGetScope function","SymGetScopeW","base.symgetscope","dbghelp/SymGetScope","dbghelp/SymGetScopeW"]
old-location: base\symgetscope.htm
tech.root: Debug
ms.assetid: 048a4d07-bf87-4dbc-9169-d8782040b205
ms.date: 08/04/2022
ms.keywords: SymGetScope, SymGetScope function, SymGetScopeW, base.symgetscope, dbghelp/SymGetScope, dbghelp/SymGetScopeW
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymGetScopeW (Unicode) and SymGetScope (ANSI)
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
 - SymGetScopeW
 - dbghelp/SymGetScopeW
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
 - SymGetScope
 - SymGetScope
 - SymGetScopeW
---

# SymGetScopeW function


## -description

Retrieves the scope for the specified index.

## -parameters

### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param BaseOfDll [in]

The base address of the module.

### -param Index [in]

A unique value for the symbol.

### -param Symbol [in, out]

A pointer to a 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-symbol_info">SYMBOL_INFO</a> structure. The <b>Scope</b> member contains the scope.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.
						

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.





> [!NOTE]
> The dbghelp.h header defines SymGetScope as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-symbol_info">SYMBOL_INFO</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symsetscopefromaddr">SymSetScopeFromAddr</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symsetscopefromindex">SymSetScopeFromIndex</a>
