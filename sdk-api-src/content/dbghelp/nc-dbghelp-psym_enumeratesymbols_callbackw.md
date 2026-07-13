---
UID: NC:dbghelp.PSYM_ENUMERATESYMBOLS_CALLBACKW
title: PSYM_ENUMERATESYMBOLS_CALLBACKW (dbghelp.h)
description: PSYM_ENUMERATESYMBOLS_CALLBACKW (Unicode) is a callback function used with the SymEnumSymbols, SymEnumTypes, and SymEnumTypesByName functions.
helpviewer_keywords: ["PSYM_ENUMERATESYMBOLS_CALLBACK","PSYM_ENUMERATESYMBOLS_CALLBACKW","PSYM_ENUMERATESYMBOLS_CALLBACKW callback function","SymEnumSymbolsProc","SymEnumSymbolsProc callback","SymEnumSymbolsProc callback function","_win32_symenumsymbolsproc","base.symenumsymbolsproc","dbghelp/PSYM_ENUMERATESYMBOLS_CALLBACK","dbghelp/PSYM_ENUMERATESYMBOLS_CALLBACKW","dbghelp/SymEnumSymbolsProc"]
old-location: base\symenumsymbolsproc.htm
tech.root: Debug
ms.assetid: c9f9aad8-754d-4ec8-92a3-8cf1929b9d8a
ms.date: 08/03/2022
ms.keywords: PSYM_ENUMERATESYMBOLS_CALLBACK, PSYM_ENUMERATESYMBOLS_CALLBACKW, PSYM_ENUMERATESYMBOLS_CALLBACKW callback function, SymEnumSymbolsProc, SymEnumSymbolsProc callback, SymEnumSymbolsProc callback function, _win32_symenumsymbolsproc, base.symenumsymbolsproc, dbghelp/PSYM_ENUMERATESYMBOLS_CALLBACK, dbghelp/PSYM_ENUMERATESYMBOLS_CALLBACKW, dbghelp/SymEnumSymbolsProc
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PSYM_ENUMERATESYMBOLS_CALLBACKW (Unicode) and PSYM_ENUMERATESYMBOLS_CALLBACK (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - PSYM_ENUMERATESYMBOLS_CALLBACKW
 - dbghelp/PSYM_ENUMERATESYMBOLS_CALLBACKW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - DbgHelp.h
api_name:
 - SymEnumSymbolsProc
 - PSYM_ENUMERATESYMBOLS_CALLBACK
 - PSYM_ENUMERATESYMBOLS_CALLBACKW
---

# PSYM_ENUMERATESYMBOLS_CALLBACKW callback function


## -description

An application-defined callback function used with the 
    <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symenumsymbols">SymEnumSymbols</a>, 
    <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symenumtypes">SymEnumTypes</a>, and 
    <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symenumtypesbyname">SymEnumTypesByName</a> functions.

The <b>PSYM_ENUMERATESYMBOLS_CALLBACK</b> and 
    <b>PSYM_ENUMERATESYMBOLS_CALLBACKW</b> types define a pointer to this callback function. 
    <b>SymEnumSymbolsProc</b> is a placeholder for the 
    application-defined function name.

## -parameters

### -param pSymInfo [in]

A pointer to a <a href="/windows/desktop/api/dbghelp/ns-dbghelp-symbol_info">SYMBOL_INFO</a> structure that 
      provides information about the symbol.

### -param SymbolSize [in]

The size of the symbol, in bytes. The size is calculated and is actually a guess. In some cases, this value 
      can be zero.

### -param UserContext [in, optional]

The user-defined value passed from the 
      <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symenumsymbols">SymEnumSymbols</a> or 
      <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symenumtypes">SymEnumTypes</a> function, or 
      <b>NULL</b>. This parameter is typically used by an application to pass a pointer to a data 
      structure that provides context information for the callback function.

## -returns

If the function returns <b>TRUE</b>, the enumeration will continue.

If the function returns <b>FALSE</b>, the enumeration will stop.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-symbol_info">SYMBOL_INFO</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symenumsymbols">SymEnumSymbols</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symenumtypes">SymEnumTypes</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symenumtypesbyname">SymEnumTypesByName</a>

## -remarks

> [!NOTE]
> The dbghelp.h header defines PSYM_ENUMERATESYMBOLS_CALLBACK as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
