---
UID: NF:dbghelp.SymFromAddr
title: SymFromAddr function
author: windows-driver-content
description: Retrieves symbol information for the specified address.
old-location: base\symfromaddr.htm
old-project: Debug
ms.assetid: 20338631-19ab-4ad8-9ba2-56fa4812b33e
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: SymFromAddr, SymFromAddr function, SymFromAddrW, _win32_symfromaddr, base.symfromaddr, dbghelp/SymFromAddr, dbghelp/SymFromAddrW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: IMAGEHLP_SYMBOL_TYPE_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dbghelp.dll
api_name:
-	SymFromAddr
-	SymFromAddr
-	SymFromAddrW
product: Windows
targetos: Windows
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
---

# SymFromAddr function


## -description


Retrieves symbol information for the specified address.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param Address [in]

The address for which a symbol should be located. The address does not have to be on a symbol boundary. If the address comes after the beginning of a symbol and before the end of the symbol, the symbol is found.


### -param Displacement [out, optional]

The displacement from the beginning of the symbol, or zero.


### -param Symbol [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/785a9702-8b77-4ce1-99df-143ce78490ab">SYMBOL_INFO</a> structure that provides information about the symbol. The symbol name is variable in length; therefore this buffer must be large enough to hold the name stored at the end of the 
<b>SYMBOL_INFO</b> structure. Be sure to set the <b>MaxNameLen</b> member to the number of bytes reserved for the name.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/63dfadea-b0c4-4050-add8-d1f3aef7a495">Retrieving Symbol Information by Address</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/785a9702-8b77-4ce1-99df-143ce78490ab">SYMBOL_INFO</a>
 

 

