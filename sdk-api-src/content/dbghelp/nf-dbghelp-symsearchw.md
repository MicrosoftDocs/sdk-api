---
UID: NF:dbghelp.SymSearchW
title: SymSearchW function (dbghelp.h)
description: The SymSearchW (Unicode) function (dbghelp.h) searches for PDB symbols that meet the specified criteria.
helpviewer_keywords: ["SYMSEARCH_ALLITEMS","SYMSEARCH_GLOBALSONLY","SYMSEARCH_MASKOBJS","SYMSEARCH_RECURSE","SymSearch","SymSearch function","SymSearchW","base.symsearch","dbghelp/SymSearch","dbghelp/SymSearchW"]
old-location: base\symsearch.htm
tech.root: Debug
ms.assetid: d6b3c06b-fcfd-436c-b267-99ec1380e744
ms.date: 08/04/2022
ms.keywords: SYMSEARCH_ALLITEMS, SYMSEARCH_GLOBALSONLY, SYMSEARCH_MASKOBJS, SYMSEARCH_RECURSE, SymSearch, SymSearch function, SymSearchW, base.symsearch, dbghelp/SymSearch, dbghelp/SymSearchW
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymSearchW (Unicode) and SymSearch (ANSI)
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
 - SymSearchW
 - dbghelp/SymSearchW
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
 - SymSearch
 - SymSearch
 - SymSearchW
---

# SymSearchW function


## -description

Searches for  PDB symbols that meet the specified criteria.

## -parameters

### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param BaseOfDll [in]

The base address of the module. If this value is zero and <i>Mask</i> contains an exclamation point (!), the function looks across modules. If this value is zero and <i>Mask</i> does not contain an exclamation point, the function uses the scope established by the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symsetcontext">SymSetContext</a> function.

### -param Index [in, optional]

A unique value for the symbol.

### -param SymTag [in, optional]

The PDB classification. These values are defined in Dbghelp.h in the <b>SymTagEnum</b> enumeration type. For  descriptions, see the PDB documentation.

### -param Mask [in, optional]

A wildcard expression that indicates the names of the symbols to be enumerated. To specify a module name, use the !<i>mod</i> syntax.

### -param Address [in, optional]

The address of the symbol.

### -param EnumSymbolsCallback [in]

 A 
<a href="/windows/desktop/api/dbghelp/nc-dbghelp-psym_enumeratesymbols_callback">SymEnumSymbolsProc</a> callback function that receives the symbol information.

### -param UserContext [in, optional]

 A user-defined value that is passed to the callback function, or <b>NULL</b>. This parameter is typically used by an application to pass a pointer to a data structure that provides context for the callback function.

### -param Options [in]

The options that control the behavior of this function.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SYMSEARCH_ALLITEMS"></a><a id="symsearch_allitems"></a><dl>
<dt><b>SYMSEARCH_ALLITEMS</b></dt>
<dt>0x08</dt>
</dl>
</td>
<td width="60%">
Include all symbols and other data in the .pdb files.

<b>DbgHelp 6.6 and earlier:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMSEARCH_GLOBALSONLY"></a><a id="symsearch_globalsonly"></a><dl>
<dt><b>SYMSEARCH_GLOBALSONLY</b></dt>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
Search only for global symbols.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMSEARCH_MASKOBJS"></a><a id="symsearch_maskobjs"></a><dl>
<dt><b>SYMSEARCH_MASKOBJS</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
For internal use only.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMSEARCH_RECURSE"></a><a id="symsearch_recurse"></a><dl>
<dt><b>SYMSEARCH_RECURSE</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
Recurse from the top to find all symbols.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is <b>TRUE</b>.
						

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.





> [!NOTE]
> The dbghelp.h header defines SymSearch as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nc-dbghelp-psym_enumeratesymbols_callback">SymEnumSymbolsProc</a>
