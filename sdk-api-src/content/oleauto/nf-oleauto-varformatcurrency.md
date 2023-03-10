---
UID: NF:oleauto.VarFormatCurrency
title: VarFormatCurrency function (oleauto.h)
description: Formats a variant containing currency values into a string form.
helpviewer_keywords: ["VarFormatCurrency","VarFormatCurrency function [Automation]","_oa96_VarFormatCurrency","automat.varformatcurrency","oleauto/VarFormatCurrency"]
old-location: automat\varformatcurrency.htm
tech.root: automat
ms.assetid: a0ad0c42-1b61-4421-9ea6-a256812bb342
ms.date: 12/05/2018
ms.keywords: VarFormatCurrency, VarFormatCurrency function [Automation], _oa96_VarFormatCurrency, automat.varformatcurrency, oleauto/VarFormatCurrency
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
 - VarFormatCurrency
 - oleauto/VarFormatCurrency
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
 - VarFormatCurrency
---

# VarFormatCurrency function


## -description

Formats a variant containing currency values into a string form.

## -parameters

### -param pvarIn [in]

The variant.

### -param iNumDig [in]

The number of digits to pad to after the decimal point. Specify -1 to use the system default value.

### -param iIncLead [in]

Specifies whether to include the leading digit on numbers.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>-2</dt>
</dl>
</td>
<td width="60%">
Use the system default.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>-1</dt>
</dl>
</td>
<td width="60%">
Include the leading digit.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Do not include the leading digit.

</td>
</tr>
</table>

### -param iUseParens [in]

Specifies whether negative numbers should use parentheses.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>-2</dt>
</dl>
</td>
<td width="60%">
Use the system default.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>-1</dt>
</dl>
</td>
<td width="60%">
Use parentheses.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Do not use parentheses.

</td>
</tr>
</table>

### -param iGroup [in]

Specifies whether thousands should be grouped. For example 10,000 versus 10000. 

<div class="alert"><b>Note</b>  Regular numbers and currencies have separate system defaults for all the above options.</div>
<div> </div>
<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>-2</dt>
</dl>
</td>
<td width="60%">
Use the system default.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>-1</dt>
</dl>
</td>
<td width="60%">
Group thousands.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Do not group thousands.

</td>
</tr>
</table>

### -param dwFlags [in]

VAR_CALENDAR_HIJRI is the only flag that can be set.

### -param pbstrOut [out]

The formatted string that represents the variant.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments is not valid.

</td>
</tr>
</table>

## -remarks

This function uses the user's default locale while calling <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-vartokenizeformatstring">VarTokenizeFormatString</a> and <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-varformatfromtokens">VarFormatFromTokens</a>.

## -see-also

<a href="/previous-versions/windows/desktop/automat/formatting-functions">Formatting Routines</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-varformatfromtokens">VarFormatFromTokens</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-vartokenizeformatstring">VarTokenizeFormatString</a>