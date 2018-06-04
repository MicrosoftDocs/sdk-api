---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

