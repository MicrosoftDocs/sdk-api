---
UID: NF:dbghelp.SymEnumSymbolsW
title: SymEnumSymbolsW function (dbghelp.h)
description: The SymEnumSymbolsW (Unicode) function enumerates all symbols in a process.
helpviewer_keywords: ["*!*","SymEnumSymbols","SymEnumSymbols function","SymEnumSymbolsW","_win32_symenumsymbols","base.symenumsymbols","dbghelp/SymEnumSymbols","dbghelp/SymEnumSymbolsW","foo","foo*!bar","foo?"]
old-location: base\symenumsymbols.htm
tech.root: Debug
ms.assetid: e1232657-baf6-4e5b-9995-a382aa1391c2
ms.date: 08/04/2022
ms.keywords: '*!*, SymEnumSymbols, SymEnumSymbols function, SymEnumSymbolsW, _win32_symenumsymbols, base.symenumsymbols, dbghelp/SymEnumSymbols, dbghelp/SymEnumSymbolsW, foo, foo*!bar, foo?'
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
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - SymEnumSymbolsW
 - dbghelp/SymEnumSymbolsW
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
 - SymEnumSymbols
 - SymEnumSymbols
 - SymEnumSymbolsW
---

# SymEnumSymbolsW function


## -description

Enumerates all symbols in a process.

## -parameters

### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
      <a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param BaseOfDll [in]

The base address of the module. If this value is zero and <i>Mask</i> contains an 
      exclamation point (!), the function looks across modules. If this value is zero and 
      <i>Mask</i> does not contain an exclamation point, the function uses the scope established by 
      the <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symsetcontext">SymSetContext</a> function.

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
         <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symsetcontext">SymSetContext</a> function.

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
         <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symsetcontext">SymSetContext</a> function.

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

A <a href="/windows/desktop/api/dbghelp/nc-dbghelp-psym_enumeratesymbols_callback">SymEnumSymbolsProc</a> callback function that 
      receives the symbol information.

### -param UserContext [in, optional]

A user-defined value that is passed to the callback function, or <b>NULL</b>. This 
      parameter is typically used by an application to pass a pointer to a data structure that provides context for 
      the callback function.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error 
       information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to 
    this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize 
    all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define 
    <b>DBGHELP_TRANSLATE_TCHAR</b>.


#### Examples

For an example, see <a href="/windows/desktop/Debug/enumerating-symbols">Enumerating Symbols</a>.

<div class="code"></div>




> [!NOTE]
> The dbghelp.h header defines SymEnumSymbols as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nc-dbghelp-psym_enumeratesymbols_callback">SymEnumSymbolsProc</a>
