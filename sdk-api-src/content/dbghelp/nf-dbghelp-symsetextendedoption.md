---
UID: NF:dbghelp.SymSetExtendedOption
title: SymSetExtendedOption function (dbghelp.h)
description: Turns the specified extended symbol option on or off.
helpviewer_keywords: ["SYMOPT_EX_DISABLEACCESSTIMEUPDATE","SymSetExtendedOption","SymSetExtendedOption function","base.symsetextendedoption","dbghelp/SymSetExtendedOption"]
old-location: base\symsetextendedoption.htm
tech.root: Debug
ms.assetid: 25756250-D2B4-4D5A-BED0-238C34C18093
ms.date: 12/05/2018
ms.keywords: SYMOPT_EX_DISABLEACCESSTIMEUPDATE, SymSetExtendedOption, SymSetExtendedOption function, base.symsetextendedoption, dbghelp/SymSetExtendedOption
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
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
req.lib: DbgHelp.lib
req.dll: DbgHelp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 10.0.16232.1000 or later
ms.custom: 19H1
f1_keywords:
 - SymSetExtendedOption
 - dbghelp/SymSetExtendedOption
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - DbgHelp.dll
 - ImageHlp.dll
api_name:
 - SymSetExtendedOption
---

# SymSetExtendedOption function


## -description

Turns the specified extended symbol option on or off.

## -parameters

### -param option [in]

The extended symbol option to turn on or off. The following are valid values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SYMOPT_EX_DISABLEACCESSTIMEUPDATE"></a><a id="symopt_ex_disableaccesstimeupdate"></a><dl>
<dt><b>SYMOPT_EX_DISABLEACCESSTIMEUPDATE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
When set to TRUE, turns off explicitly updating the last access time of a symbol that is loaded. By default, DbgHelp updates the last access time of a symbol file that is consumed so that a symbol cache can be maintained by using a least recently used mechanism.

</td>
</tr>
</table>

### -param value [in]

The value to set for the specified option, either TRUE or FALSE.

## -returns

The previous value of the specified extended option.

## -see-also

<a href="/windows/desktop/api/dbghelp/ne-dbghelp-imagehlp_extended_options">IMAGEHLP_EXTENDED_OPTIONS</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetextendedoption">SymGetExtendedOption</a>