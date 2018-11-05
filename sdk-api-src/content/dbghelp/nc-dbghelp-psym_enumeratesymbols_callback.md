---
UID: NC:dbghelp.PSYM_ENUMERATESYMBOLS_CALLBACK
title: PSYM_ENUMERATESYMBOLS_CALLBACK
author: windows-sdk-content
description: An application-defined callback function used with the SymEnumSymbols, SymEnumTypes, and SymEnumTypesByName functions.
old-location: base\symenumsymbolsproc.htm
tech.root: debug
ms.assetid: c9f9aad8-754d-4ec8-92a3-8cf1929b9d8a
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: PSYM_ENUMERATESYMBOLS_CALLBACK, PSYM_ENUMERATESYMBOLS_CALLBACKW, PSYM_ENUMERATESYMBOLS_CALLBACKW callback function, SymEnumSymbolsProc, SymEnumSymbolsProc callback, SymEnumSymbolsProc callback function, _win32_symenumsymbolsproc, base.symenumsymbolsproc, dbghelp/PSYM_ENUMERATESYMBOLS_CALLBACK, dbghelp/PSYM_ENUMERATESYMBOLS_CALLBACKW, dbghelp/SymEnumSymbolsProc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
---

# PSYM_ENUMERATESYMBOLS_CALLBACK callback function


## -description


An application-defined callback function used with the 
    <a href="https://msdn.microsoft.com/e1232657-baf6-4e5b-9995-a382aa1391c2">SymEnumSymbols</a>, 
    <a href="https://msdn.microsoft.com/06f964bc-107a-468d-a35d-141b5da1780e">SymEnumTypes</a>, and 
    <a href="https://msdn.microsoft.com/48acb588-23fa-44f3-8b8c-f3c76371d1fd">SymEnumTypesByName</a> functions.

The <b>PSYM_ENUMERATESYMBOLS_CALLBACK</b> and 
    <b>PSYM_ENUMERATESYMBOLS_CALLBACKW</b> types define a pointer to this callback function. 
    <b>SymEnumSymbolsProc</b> is a placeholder for the 
    application-defined function name.


## -parameters




### -param pSymInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/785a9702-8b77-4ce1-99df-143ce78490ab">SYMBOL_INFO</a> structure that 
      provides information about the symbol.


### -param SymbolSize [in]

The size of the symbol, in bytes. The size is calculated and is actually a guess. In some cases, this value 
      can be zero.


### -param UserContext [in, optional]

The user-defined value passed from the 
      <a href="https://msdn.microsoft.com/e1232657-baf6-4e5b-9995-a382aa1391c2">SymEnumSymbols</a> or 
      <a href="https://msdn.microsoft.com/06f964bc-107a-468d-a35d-141b5da1780e">SymEnumTypes</a> function, or 
      <b>NULL</b>. This parameter is typically used by an application to pass a pointer to a data 
      structure that provides context information for the callback function.


## -returns



If the function returns <b>TRUE</b>, the enumeration will continue.

If the function returns <b>FALSE</b>, the enumeration will stop.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/785a9702-8b77-4ce1-99df-143ce78490ab">SYMBOL_INFO</a>



<a href="https://msdn.microsoft.com/e1232657-baf6-4e5b-9995-a382aa1391c2">SymEnumSymbols</a>



<a href="https://msdn.microsoft.com/06f964bc-107a-468d-a35d-141b5da1780e">SymEnumTypes</a>



<a href="https://msdn.microsoft.com/48acb588-23fa-44f3-8b8c-f3c76371d1fd">SymEnumTypesByName</a>
 

 

