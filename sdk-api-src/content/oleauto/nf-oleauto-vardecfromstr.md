---
UID: NF:oleauto.VarDecFromStr
title: VarDecFromStr function (oleauto.h)
description: Converts an OLECHAR string to a decimal value.
helpviewer_keywords: ["LOCALE_NOUSEROVERRIDE","VAR_DATEVALUEONLY","VAR_TIMEVALUEONLY","VarDecFromStr","VarDecFromStr function [Automation]","_oa96_VarDecFromStr","automat.vardecfromstr","oleauto/VarDecFromStr"]
old-location: automat\vardecfromstr.htm
tech.root: automat
ms.assetid: 6e036c9c-3b5d-4b5c-9992-526380bb544d
ms.date: 12/05/2018
ms.keywords: LOCALE_NOUSEROVERRIDE, VAR_DATEVALUEONLY, VAR_TIMEVALUEONLY, VarDecFromStr, VarDecFromStr function [Automation], _oa96_VarDecFromStr, automat.vardecfromstr, oleauto/VarDecFromStr
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
 - VarDecFromStr
 - oleauto/VarDecFromStr
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
 - VarDecFromStr
---

# VarDecFromStr function


## -description

Converts an OLECHAR string to a decimal value.

## -parameters

### -param strIn [in]

The value to convert.

### -param lcid [in]

The locale identifier.

### -param dwFlags [in]

One or more of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LOCALE_NOUSEROVERRIDE"></a><a id="locale_nouseroverride"></a><dl>
<dt><b>LOCALE_NOUSEROVERRIDE</b></dt>
</dl>
</td>
<td width="60%">
Uses the system default locale settings, rather than custom locale settings.

</td>
</tr>
<tr>
<td width="40%"><a id="VAR_TIMEVALUEONLY"></a><a id="var_timevalueonly"></a><dl>
<dt><b>VAR_TIMEVALUEONLY</b></dt>
</dl>
</td>
<td width="60%">
Omits the date portion of a VT_DATE and returns only the time. Applies to conversions to or from dates.

</td>
</tr>
<tr>
<td width="40%"><a id="VAR_DATEVALUEONLY"></a><a id="var_datevalueonly"></a><dl>
<dt><b>VAR_DATEVALUEONLY</b></dt>
</dl>
</td>
<td width="60%">
Omits the time portion of a VT_DATE and returns only the date. Applies to conversions to or from dates.

</td>
</tr>
</table>

### -param pdecOut [out]

The resulting value.

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
<dt><b>DISP_E_BADVARTYPE</b></dt>
</dl>
</td>
<td width="60%">
The input parameter is not a valid type of variant.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
The data pointed to by the output parameter does not fit in the destination type.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>

