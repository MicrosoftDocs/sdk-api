---
UID: NF:dbghelp.SymEnumSymbolsW
title: SymEnumSymbolsW function
author: windows-driver-content
description: Enumerates all symbols in a process.
old-location: base\symenumsymbols.htm
old-project: Debug
ms.assetid: e1232657-baf6-4e5b-9995-a382aa1391c2
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: "*!*, SymEnumSymbols, SymEnumSymbols function, SymEnumSymbolsW, _win32_symenumsymbols, base.symenumsymbols, dbghelp/SymEnumSymbols, dbghelp/SymEnumSymbolsW, foo, foo*!bar, foo?"
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
req.unicode-ansi: SymEnumSymbolsW (Unicode) and SymEnumSymbols (ANSI)
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
-	SymEnumSymbols
-	SymEnumSymbols
-	SymEnumSymbolsW
product: Windows
targetos: Windows
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
---

# SymEnumSymbolsW function


## -description


Enumerates all symbols in a process.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
      <a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param BaseOfDll [in]

The base address of the module. If this value is zero and <i>Mask</i> contains an 
      exclamation point (!), the function looks across modules. If this value is zero and 
      <i>Mask</i> does not contain an exclamation point, the function uses the scope established by 
      the <a href="https://msdn.microsoft.com/0a9c6bfe-5e60-48c4-af98-b910df3032d5">SymSetContext</a> function.


### -param Mask [in, optional]

A wildcard string that indicates the names of the symbols to be enumerated. The text can optionally contain 
       the wildcards, "*" and "?".

To specify a specific module or set of modules, begin the text with a wildcard string specifying the module, 
       followed by an exclamation point. When specifying a module, <i>BaseOfDll</i> is ignored.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="foo"></a><a id="FOO"></a><dl>
<dt><b>foo</b></dt>
</dl>
</td>
<td width="60%">
If <i>BaseOfDll</i> is not zero, then 
         <b>SymEnumSymbols</b> will look for a global symbol named 
         "foo".

If <i>BaseOfDll</i> is zero, then 
         <b>SymEnumSymbols</b> will look for a local symbol named 
         "foo" within the scope established by the most recent call to the 
         <a href="https://msdn.microsoft.com/0a9c6bfe-5e60-48c4-af98-b910df3032d5">SymSetContext</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="foo_"></a><a id="FOO_"></a><dl>
<dt><b>foo?</b></dt>
</dl>
</td>
<td width="60%">
If <i>BaseOfDll</i> is not zero, then 
         <b>SymEnumSymbols</b> will look for a global symbol that 
         starts with "foo" and contains one extra character afterwards, such as 
         "fool" and "foot".

If <i>BaseOfDll</i> is zero, then 
         <b>SymEnumSymbols</b> will look for a symbol that starts 
         with "foo" and contains one extra character afterwards, such as "fool" and 
         "foot". The search would be within the scope established by the most recent call to the 
         <a href="https://msdn.microsoft.com/0a9c6bfe-5e60-48c4-af98-b910df3032d5">SymSetContext</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="foo__bar"></a><a id="FOO__BAR"></a><dl>
<dt><b>foo*!bar</b></dt>
</dl>
</td>
<td width="60%">
<b>SymEnumSymbols</b> will look in every loaded module 
         that starts with the text "foo" for a symbol called "bar".  It could find 
         matches such as these, "foot!bar", "footlocker!bar", and 
         "fool!bar".

</td>
</tr>
<tr>
<td width="40%"><a id="___"></a><dl>
<dt><b>*!*</b></dt>
</dl>
</td>
<td width="60%">
<b>SymEnumSymbols</b> will enumerate every symbol in 
         every loaded module.

</td>
</tr>
</table>
 


### -param EnumSymbolsCallback [in]

A <a href="https://msdn.microsoft.com/c9f9aad8-754d-4ec8-92a3-8cf1929b9d8a">SymEnumSymbolsProc</a> callback function that 
      receives the symbol information.


### -param UserContext [in, optional]

A user-defined value that is passed to the callback function, or <b>NULL</b>. This 
      parameter is typically used by an application to pass a pointer to a data structure that provides context for 
      the callback function.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error 
       information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to 
    this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize 
    all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define 
    <b>DBGHELP_TRANSLATE_TCHAR</b>.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/6ecdbd1e-406a-453e-9037-707ceb72074a">Enumerating Symbols</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/c9f9aad8-754d-4ec8-92a3-8cf1929b9d8a">SymEnumSymbolsProc</a>
 

 

