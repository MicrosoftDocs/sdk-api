---
UID: NS:dbghelp._SYMBOL_INFOW
title: SYMBOL_INFOW (dbghelp.h)
description: The SYMBOL_INFOW (Unicode) structure (dbghelp.h) contains symbol information.
helpviewer_keywords: ["*PSYMBOL_INFOW","PSYMBOL_INFO","PSYMBOL_INFO structure pointer","SYMBOL_INFO","SYMBOL_INFO structure","SYMBOL_INFOW","SYMFLAG_CLR_TOKEN","SYMFLAG_CONSTANT","SYMFLAG_EXPORT","SYMFLAG_FORWARDER","SYMFLAG_FRAMEREL","SYMFLAG_FUNCTION","SYMFLAG_ILREL","SYMFLAG_LOCAL","SYMFLAG_METADATA","SYMFLAG_PARAMETER","SYMFLAG_REGISTER","SYMFLAG_REGREL","SYMFLAG_SLOT","SYMFLAG_THUNK","SYMFLAG_TLSREL","SYMFLAG_VALUEPRESENT","SYMFLAG_VIRTUAL","_SYMBOL_INFO","_SYMBOL_INFOW","_win32_symbol_info_str","base.symbol_info_str","dbghelp/PSYMBOL_INFO","dbghelp/SYMBOL_INFO","dbghelp/SYMBOL_INFOW"]
old-location: base\symbol_info_str.htm
tech.root: Debug
ms.assetid: 785a9702-8b77-4ce1-99df-143ce78490ab
ms.date: 08/04/2022
ms.keywords: '*PSYMBOL_INFOW, PSYMBOL_INFO, PSYMBOL_INFO structure pointer, SYMBOL_INFO, SYMBOL_INFO structure, SYMBOL_INFOW, SYMFLAG_CLR_TOKEN, SYMFLAG_CONSTANT, SYMFLAG_EXPORT, SYMFLAG_FORWARDER, SYMFLAG_FRAMEREL, SYMFLAG_FUNCTION, SYMFLAG_ILREL, SYMFLAG_LOCAL, SYMFLAG_METADATA, SYMFLAG_PARAMETER, SYMFLAG_REGISTER, SYMFLAG_REGREL, SYMFLAG_SLOT, SYMFLAG_THUNK, SYMFLAG_TLSREL, SYMFLAG_VALUEPRESENT, SYMFLAG_VIRTUAL, _SYMBOL_INFO, _SYMBOL_INFOW, _win32_symbol_info_str, base.symbol_info_str, dbghelp/PSYMBOL_INFO, dbghelp/SYMBOL_INFO, dbghelp/SYMBOL_INFOW'
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SYMBOL_INFOW (Unicode) and SYMBOL_INFO (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SYMBOL_INFOW, *PSYMBOL_INFOW
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _SYMBOL_INFOW
 - dbghelp/_SYMBOL_INFOW
 - PSYMBOL_INFOW
 - dbghelp/PSYMBOL_INFOW
 - SYMBOL_INFOW
 - dbghelp/SYMBOL_INFOW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DbgHelp.h
api_name:
 - SYMBOL_INFO
 - SYMBOL_INFO
 - SYMBOL_INFOW
---

# SYMBOL_INFOW structure


## -description

Contains symbol information.

## -struct-fields

### -field SizeOfStruct

The size of the structure, in bytes. This member must be set to <code>sizeof(SYMBOL_INFO)</code>. Note that the total size of the data is the <code>SizeOfStruct + (MaxNameLen - 1) * sizeof(TCHAR)</code>. The reason to subtract one is that the first character in the name is accounted for in the size of the structure.

### -field TypeIndex

A unique value that identifies the type data that describes the symbol.  This value does not persist between sessions.

### -field Reserved

This member is reserved for system use.

### -field Index

The unique value for the symbol. The value associated with a symbol is not guaranteed to be the same each time you run the process.

For PDB symbols, the index value for a symbol is not generated until the symbol is enumerated or retrieved through a search by name or address. The index values for all CodeView and COFF symbols are generated when the symbols are loaded.

### -field Size

The symbol size, in bytes. This value is meaningful only if the module symbols are from a pdb file;  otherwise, this value is typically zero and should be ignored.

### -field ModBase

The base address of the module that contains the symbol.

### -field Flags

This member can be one or more of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SYMFLAG_CLR_TOKEN"></a><a id="symflag_clr_token"></a><dl>
<dt><b>SYMFLAG_CLR_TOKEN</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
The symbol is a CLR token.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMFLAG_CONSTANT"></a><a id="symflag_constant"></a><dl>
<dt><b>SYMFLAG_CONSTANT</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
The symbol is a constant.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMFLAG_EXPORT"></a><a id="symflag_export"></a><dl>
<dt><b>SYMFLAG_EXPORT</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
The symbol is from the export table.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMFLAG_FORWARDER"></a><a id="symflag_forwarder"></a><dl>
<dt><b>SYMFLAG_FORWARDER</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
The symbol is a forwarder.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMFLAG_FRAMEREL"></a><a id="symflag_framerel"></a><dl>
<dt><b>SYMFLAG_FRAMEREL</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Offsets are frame relative.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMFLAG_FUNCTION"></a><a id="symflag_function"></a><dl>
<dt><b>SYMFLAG_FUNCTION</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
The symbol is a known function.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMFLAG_ILREL"></a><a id="symflag_ilrel"></a><dl>
<dt><b>SYMFLAG_ILREL</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
The symbol address is an offset relative to the beginning of the intermediate language block. This applies to managed code only.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMFLAG_LOCAL"></a><a id="symflag_local"></a><dl>
<dt><b>SYMFLAG_LOCAL</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
The symbol is a local variable.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMFLAG_METADATA"></a><a id="symflag_metadata"></a><dl>
<dt><b>SYMFLAG_METADATA</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
The symbol is managed metadata.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMFLAG_PARAMETER"></a><a id="symflag_parameter"></a><dl>
<dt><b>SYMFLAG_PARAMETER</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
The symbol is a parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMFLAG_REGISTER"></a><a id="symflag_register"></a><dl>
<dt><b>SYMFLAG_REGISTER</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The symbol is a register. The <b>Register</b> member is used.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMFLAG_REGREL"></a><a id="symflag_regrel"></a><dl>
<dt><b>SYMFLAG_REGREL</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Offsets are register relative.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMFLAG_SLOT"></a><a id="symflag_slot"></a><dl>
<dt><b>SYMFLAG_SLOT</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
The symbol is a managed code slot.
							

</td>
</tr>
<tr>
<td width="40%"><a id="SYMFLAG_THUNK"></a><a id="symflag_thunk"></a><dl>
<dt><b>SYMFLAG_THUNK</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
The symbol is a thunk.
							

</td>
</tr>
<tr>
<td width="40%"><a id="SYMFLAG_TLSREL"></a><a id="symflag_tlsrel"></a><dl>
<dt><b>SYMFLAG_TLSREL</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
The symbol is an offset into the TLS data area.
							

</td>
</tr>
<tr>
<td width="40%"><a id="SYMFLAG_VALUEPRESENT"></a><a id="symflag_valuepresent"></a><dl>
<dt><b>SYMFLAG_VALUEPRESENT</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The <b>Value</b> member is used.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMFLAG_VIRTUAL"></a><a id="symflag_virtual"></a><dl>
<dt><b>SYMFLAG_VIRTUAL</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
The symbol is a virtual symbol created by the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symaddsymbol">SymAddSymbol</a> function.
							

</td>
</tr>
</table>

### -field Value

The value of a constant.

### -field Address

The virtual address of the start of the symbol.

### -field Register

The register.

### -field Scope

The DIA scope. For more information, see the <i>Debug Interface Access SDK</i> in the Visual Studio documentation. (This resource may not be available in some languages 

and countries.)

### -field Tag

The PDB classification. These values are defined in Dbghelp.h in the <a href="/previous-versions/visualstudio/visual-studio-2010/bkedss5f(v=vs.100)">SymTagEnum</a> enumeration type.

### -field NameLen

The length of the name, in characters, not including the null-terminating character.

### -field MaxNameLen

The size of the <b>Name</b> buffer, in characters. If this member is 0, the <b>Name</b> member is not used.

### -field Name

The name of the symbol. The name can be undecorated if the SYMOPT_UNDNAME option is used with the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symsetoptions">SymSetOptions</a> function.

## -see-also

<a href="/windows/desktop/api/dbghelp/nc-dbghelp-psym_enumeratesymbols_callback">SymEnumSymbolsProc</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symfromaddr">SymFromAddr</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symfromname">SymFromName</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgettypefromname">SymGetTypeFromName</a>

## -remarks

> [!NOTE]
> The dbghelp.h header defines SYMBOL_INFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
