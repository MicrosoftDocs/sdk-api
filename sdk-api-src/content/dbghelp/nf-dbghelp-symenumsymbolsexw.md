---
UID: NF:dbghelp.SymEnumSymbolsExW
title: SymEnumSymbolsExW function (dbghelp.h)
author: windows-sdk-content
description: Enumerates all symbols in a process.
old-location: base\symenumsymbolsex.htm
tech.root: Debug
ms.assetid: 80fbe47d-702c-4cda-8e28-c72f8d7db3d2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*!*, SYMENUM_OPTIONS_DEFAULT, SYMENUM_OPTIONS_INLINE, SymEnumSymbolsEx, SymEnumSymbolsEx function, SymEnumSymbolsExW, base.symenumsymbolsex, dbghelp/SymEnumSymbolsEx, dbghelp/SymEnumSymbolsExW, foo, foo*!bar, foo?"
ms.topic: function
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymEnumSymbolsExW (Unicode) and SymEnumSymbolsEx (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: DbgHelp.lib
req.dll: DbgHelp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - DbgHelp.dll
api_name:
 - SymEnumSymbolsEx
 - SymEnumSymbolsEx
 - SymEnumSymbolsExW
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.2 or later
---

# SymEnumSymbolsExW function


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
         <a href="https://msdn.microsoft.com/e1232657-baf6-4e5b-9995-a382aa1391c2">SymEnumSymbols</a> will look for a global symbol named 
         "foo".

If <i>BaseOfDll</i> is zero, then 
         <a href="https://msdn.microsoft.com/e1232657-baf6-4e5b-9995-a382aa1391c2">SymEnumSymbols</a> will look for a local symbol named 
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
         <a href="https://msdn.microsoft.com/e1232657-baf6-4e5b-9995-a382aa1391c2">SymEnumSymbols</a> will look for a global symbol that 
         starts with "foo" and contains one extra character afterwards, such as 
         "fool" and "foot".

If <i>BaseOfDll</i> is zero, then 
         <a href="https://msdn.microsoft.com/e1232657-baf6-4e5b-9995-a382aa1391c2">SymEnumSymbols</a> will look for a symbol that starts 
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

<a href="https://msdn.microsoft.com/e1232657-baf6-4e5b-9995-a382aa1391c2">SymEnumSymbols</a> will look in every loaded module 
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

<a href="https://msdn.microsoft.com/e1232657-baf6-4e5b-9995-a382aa1391c2">SymEnumSymbols</a> will enumerate every symbol in 
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


### -param Options [in]

Indicates possible options.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SYMENUM_OPTIONS_DEFAULT"></a><a id="symenum_options_default"></a><dl>
<dt><b>SYMENUM_OPTIONS_DEFAULT</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Use the default options.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMENUM_OPTIONS_INLINE"></a><a id="symenum_options_inline"></a><dl>
<dt><b>SYMENUM_OPTIONS_INLINE</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Enumerate inline symbols.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error 
       information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



