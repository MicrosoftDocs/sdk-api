---
UID: NF:oleauto.VarParseNumFromStr
title: VarParseNumFromStr function (oleauto.h)
description: Parses a string, and creates a type-independent description of the number it represents.
helpviewer_keywords: ["VarParseNumFromStr","VarParseNumFromStr function [Automation]","_oa96_VarParseNumFromStr","automat.varparsenumfromstr","oleauto/VarParseNumFromStr"]
old-location: automat\varparsenumfromstr.htm
tech.root: automat
ms.assetid: b77ce0df-5635-4760-8b42-f3afec49482b
ms.date: 12/05/2018
ms.keywords: VarParseNumFromStr, VarParseNumFromStr function [Automation], _oa96_VarParseNumFromStr, automat.varparsenumfromstr, oleauto/VarParseNumFromStr
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
 - VarParseNumFromStr
 - oleauto/VarParseNumFromStr
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
 - VarParseNumFromStr
---

# VarParseNumFromStr function


## -description

Parses a string, and creates a type-independent description of the number it represents.

## -parameters

### -param strIn [in]

The input string to convert.

### -param lcid [in]

The locale identifier.

### -param dwFlags [in]

Enables the caller to control parsing, therefore defining the acceptable syntax of a number. If this field is set to zero, the input string must contain nothing but decimal digits. Setting each defined flag bit enables parsing of that syntactic feature. Standard Automation parsing (for example, as used by <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-vari2fromstr">VarI2FromStr</a>) has all flags set (NUMPRS_STD).

### -param pnumprs [out]

The parsed results.

### -param rgbDig [out]

The values for the digits in the range 0–7, 0–9, or 0–15, depending on whether the number is octal, decimal, or hexadecimal. All leading zeros have been stripped off. For decimal numbers, trailing zeros are also stripped off, unless the number is zero, in which case a single zero digit will be present.

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
Internal memory allocation failed. (Used for DBCS only to create a copy with all wide characters mapped narrow.)


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_TYPEMISMATCH</b></dt>
</dl>
</td>
<td width="60%">
There is no valid number in the string, or there is no closing parenthesis to match an opening one. In the former case, cDig and cchUsed in the NUMPARSE structure will be zero. In the latter, the NUMPARSE structure and digit array are fully updated, as if the closing parenthesis was present.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
For hexadecimal and octal digits, there are more digits than will fit into the array. For decimal, the exponent exceeds the maximum possible. In both cases, the NUMPARSE structure and digit array are fully updated (for decimal, the cchUsed field excludes the entire exponent).


</td>
</tr>
</table>