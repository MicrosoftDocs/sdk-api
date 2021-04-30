---
UID: NF:oleauto.VarFormatFromTokens
title: VarFormatFromTokens function (oleauto.h)
description: Takes a tokenized format string and applies it to a variant to produce a formatted output string.
helpviewer_keywords: ["VarFormatFromTokens","VarFormatFromTokens function [Automation]","_oa96_VarFormatFromTokens","automat.varformatfromtokens","oleauto/VarFormatFromTokens"]
old-location: automat\varformatfromtokens.htm
tech.root: automat
ms.assetid: 36437d1a-970d-4a52-a8a5-1cddfe3d42f3
ms.date: 12/05/2018
ms.keywords: VarFormatFromTokens, VarFormatFromTokens function [Automation], _oa96_VarFormatFromTokens, automat.varformatfromtokens, oleauto/VarFormatFromTokens
req.header: oleauto.h
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
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VarFormatFromTokens
 - oleauto/VarFormatFromTokens
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - VarFormatFromTokens
---

# VarFormatFromTokens function


## -description

Takes a tokenized format string and applies it to a variant to produce a formatted output string.

## -parameters

### -param pvarIn [in]

The variant containing the value to format.

### -param pstrFormat [in, optional]

The original format string.

### -param pbTokCur [in]

The tokenized format string from <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-vartokenizeformatstring">VarTokenizeFormatString</a>.

### -param dwFlags [in]

The only flags that can be set are VAR_CALENDAR_HIJRI or VAR_FORMAT_NOSUBSTITUTE.

### -param pbstrOut [out]

The formatted output string.

### -param lcid [in]

The locale to use for the formatted output string.

## -returns

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments is not valid.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_TYPEMISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The argument could not be coerced to the specified type.


</td>
</tr>
</table>

## -remarks

The locale <i>lcid</i> controls the formatted output string.