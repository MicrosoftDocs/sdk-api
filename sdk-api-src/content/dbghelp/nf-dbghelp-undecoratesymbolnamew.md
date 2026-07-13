---
UID: NF:dbghelp.UnDecorateSymbolNameW
title: UnDecorateSymbolNameW function (dbghelp.h)
description: The UnDecorateSymbolNameW (Unicode) function (dbghelp.h) undecorates the specified decorated C++ symbol name.
helpviewer_keywords: ["UNDNAME_32_BIT_DECODE","UNDNAME_COMPLETE","UNDNAME_NAME_ONLY","UNDNAME_NO_ACCESS_SPECIFIERS","UNDNAME_NO_ALLOCATION_LANGUAGE","UNDNAME_NO_ALLOCATION_MODEL","UNDNAME_NO_ARGUMENTS","UNDNAME_NO_CV_THISTYPE","UNDNAME_NO_FUNCTION_RETURNS","UNDNAME_NO_LEADING_UNDERSCORES","UNDNAME_NO_MEMBER_TYPE","UNDNAME_NO_MS_KEYWORDS","UNDNAME_NO_MS_THISTYPE","UNDNAME_NO_RETURN_UDT_MODEL","UNDNAME_NO_SPECIAL_SYMS","UNDNAME_NO_THISTYPE","UNDNAME_NO_THROW_SIGNATURES","UnDecorateSymbolName","UnDecorateSymbolName function","UnDecorateSymbolNameW","_win32_undecoratesymbolname","base.undecoratesymbolname","dbghelp/UnDecorateSymbolName","dbghelp/UnDecorateSymbolNameW"]
old-location: base\undecoratesymbolname.htm
tech.root: Debug
ms.assetid: f52e8e3b-3113-4d8c-b44a-846c574cfbd8
ms.date: 08/04/2022
ms.keywords: UNDNAME_32_BIT_DECODE, UNDNAME_COMPLETE, UNDNAME_NAME_ONLY, UNDNAME_NO_ACCESS_SPECIFIERS, UNDNAME_NO_ALLOCATION_LANGUAGE, UNDNAME_NO_ALLOCATION_MODEL, UNDNAME_NO_ARGUMENTS, UNDNAME_NO_CV_THISTYPE, UNDNAME_NO_FUNCTION_RETURNS, UNDNAME_NO_LEADING_UNDERSCORES, UNDNAME_NO_MEMBER_TYPE, UNDNAME_NO_MS_KEYWORDS, UNDNAME_NO_MS_THISTYPE, UNDNAME_NO_RETURN_UDT_MODEL, UNDNAME_NO_SPECIAL_SYMS, UNDNAME_NO_THISTYPE, UNDNAME_NO_THROW_SIGNATURES, UnDecorateSymbolName, UnDecorateSymbolName function, UnDecorateSymbolNameW, _win32_undecoratesymbolname, base.undecoratesymbolname, dbghelp/UnDecorateSymbolName, dbghelp/UnDecorateSymbolNameW
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UnDecorateSymbolNameW (Unicode) and UnDecorateSymbolName (ANSI)
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
 - UnDecorateSymbolNameW
 - dbghelp/UnDecorateSymbolNameW
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
 - UnDecorateSymbolName
 - UnDecorateSymbolName
 - UnDecorateSymbolNameW
---

# UnDecorateSymbolNameW function


## -description

Undecorates the specified decorated C++ symbol name.

## -parameters

### -param name [in]

The decorated C++ symbol name. This name can be identified by the first character of the name, which is 
      always a question mark (?).

### -param outputString [out]

A pointer to a string buffer that receives the undecorated name.

### -param maxStringLength [in]

The size of the <i>UnDecoratedName</i> buffer, in characters.

### -param flags [in]

The options for how the decorated name is undecorated. This parameter can be zero or more of the following 
      values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="UNDNAME_32_BIT_DECODE"></a><a id="undname_32_bit_decode"></a><dl>
<dt><b>UNDNAME_32_BIT_DECODE</b></dt>
<dt>0x0800</dt>
</dl>
</td>
<td width="60%">
Undecorate 32-bit decorated names.

</td>
</tr>
<tr>
<td width="40%"><a id="UNDNAME_COMPLETE"></a><a id="undname_complete"></a><dl>
<dt><b>UNDNAME_COMPLETE</b></dt>
<dt>0x0000</dt>
</dl>
</td>
<td width="60%">
Enable full undecoration.

</td>
</tr>
<tr>
<td width="40%"><a id="UNDNAME_NAME_ONLY"></a><a id="undname_name_only"></a><dl>
<dt><b>UNDNAME_NAME_ONLY</b></dt>
<dt>0x1000</dt>
</dl>
</td>
<td width="60%">
Undecorate only the name for primary declaration. Returns [scope::]name. Does expand template 
        parameters.

</td>
</tr>
<tr>
<td width="40%"><a id="UNDNAME_NO_ACCESS_SPECIFIERS"></a><a id="undname_no_access_specifiers"></a><dl>
<dt><b>UNDNAME_NO_ACCESS_SPECIFIERS</b></dt>
<dt>0x0080</dt>
</dl>
</td>
<td width="60%">
Disable expansion of access specifiers for members.

</td>
</tr>
<tr>
<td width="40%"><a id="UNDNAME_NO_ALLOCATION_LANGUAGE"></a><a id="undname_no_allocation_language"></a><dl>
<dt><b>UNDNAME_NO_ALLOCATION_LANGUAGE</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
Disable expansion of the declaration language specifier.

</td>
</tr>
<tr>
<td width="40%"><a id="UNDNAME_NO_ALLOCATION_MODEL"></a><a id="undname_no_allocation_model"></a><dl>
<dt><b>UNDNAME_NO_ALLOCATION_MODEL</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
Disable expansion of the declaration model.

</td>
</tr>
<tr>
<td width="40%"><a id="UNDNAME_NO_ARGUMENTS"></a><a id="undname_no_arguments"></a><dl>
<dt><b>UNDNAME_NO_ARGUMENTS</b></dt>
<dt>0x2000</dt>
</dl>
</td>
<td width="60%">
Do not undecorate function arguments.

</td>
</tr>
<tr>
<td width="40%"><a id="UNDNAME_NO_CV_THISTYPE"></a><a id="undname_no_cv_thistype"></a><dl>
<dt><b>UNDNAME_NO_CV_THISTYPE</b></dt>
<dt>0x0040</dt>
</dl>
</td>
<td width="60%">
Disable expansion of CodeView modifiers on the <b>this</b> type for primary 
        declaration.

</td>
</tr>
<tr>
<td width="40%"><a id="UNDNAME_NO_FUNCTION_RETURNS"></a><a id="undname_no_function_returns"></a><dl>
<dt><b>UNDNAME_NO_FUNCTION_RETURNS</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
Disable expansion of return types for primary declarations.

</td>
</tr>
<tr>
<td width="40%"><a id="UNDNAME_NO_LEADING_UNDERSCORES"></a><a id="undname_no_leading_underscores"></a><dl>
<dt><b>UNDNAME_NO_LEADING_UNDERSCORES</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Remove leading underscores from Microsoft keywords.

</td>
</tr>
<tr>
<td width="40%"><a id="UNDNAME_NO_MEMBER_TYPE"></a><a id="undname_no_member_type"></a><dl>
<dt><b>UNDNAME_NO_MEMBER_TYPE</b></dt>
<dt>0x0200</dt>
</dl>
</td>
<td width="60%">
Disable expansion of the static or virtual attribute of members.

</td>
</tr>
<tr>
<td width="40%"><a id="UNDNAME_NO_MS_KEYWORDS"></a><a id="undname_no_ms_keywords"></a><dl>
<dt><b>UNDNAME_NO_MS_KEYWORDS</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Disable expansion of Microsoft keywords.

</td>
</tr>
<tr>
<td width="40%"><a id="UNDNAME_NO_MS_THISTYPE"></a><a id="undname_no_ms_thistype"></a><dl>
<dt><b>UNDNAME_NO_MS_THISTYPE</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
Disable expansion of Microsoft keywords on the <b>this</b> type for primary 
        declaration.

</td>
</tr>
<tr>
<td width="40%"><a id="UNDNAME_NO_RETURN_UDT_MODEL"></a><a id="undname_no_return_udt_model"></a><dl>
<dt><b>UNDNAME_NO_RETURN_UDT_MODEL</b></dt>
<dt>0x0400</dt>
</dl>
</td>
<td width="60%">
Disable expansion of the Microsoft model for user-defined type returns.

</td>
</tr>
<tr>
<td width="40%"><a id="UNDNAME_NO_SPECIAL_SYMS"></a><a id="undname_no_special_syms"></a><dl>
<dt><b>UNDNAME_NO_SPECIAL_SYMS</b></dt>
<dt>0x4000</dt>
</dl>
</td>
<td width="60%">
Do not undecorate special names, such as vtable, vcall, vector, metatype, and so on.

</td>
</tr>
<tr>
<td width="40%"><a id="UNDNAME_NO_THISTYPE"></a><a id="undname_no_thistype"></a><dl>
<dt><b>UNDNAME_NO_THISTYPE</b></dt>
<dt>0x0060</dt>
</dl>
</td>
<td width="60%">
Disable all modifiers on the <b>this</b> type.

</td>
</tr>
<tr>
<td width="40%"><a id="UNDNAME_NO_THROW_SIGNATURES"></a><a id="undname_no_throw_signatures"></a><dl>
<dt><b>UNDNAME_NO_THROW_SIGNATURES</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
Disable expansion of throw-signatures for functions and pointers to functions.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is the number of characters in the 
       <i>UnDecoratedName</i> buffer, not including the NULL terminator.

If the function fails, the return value is zero. To retrieve extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If the function fails and returns zero, the content of the <i>UnDecoratedName</i> buffer 
       is undetermined.

## -remarks

To use undecorated symbols, call the <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symsetoptions">SymSetOptions</a> 
    function with the <b>SYMOPT_UNDNAME</b> option.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to 
    this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize 
    all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define <b>DBGHELP_TRANSLATE_TCHAR</b>.


#### Examples

For an example, see 
     <a href="/windows/desktop/Debug/retrieving-undecorated-symbol-names">Retrieving Undecorated Symbol Names</a>.

<div class="code"></div>




> [!NOTE]
> The dbghelp.h header defines UnDecorateSymbolName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symsetoptions">SymSetOptions</a>
