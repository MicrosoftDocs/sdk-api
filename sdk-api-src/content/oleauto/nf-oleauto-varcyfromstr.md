---
UID: NF:oleauto.VarCyFromStr
title: VarCyFromStr function (oleauto.h)
description: Converts an OLECHAR string to a currency value.
helpviewer_keywords: ["LOCALE_NOUSEROVERRIDE","VAR_DATEVALUEONLY","VAR_TIMEVALUEONLY","VarCyFromStr","VarCyFromStr function [Automation]","_oa96_VarCyFromStr","automat.varcyfromstr","oleauto/VarCyFromStr"]
old-location: automat\varcyfromstr.htm
tech.root: automat
ms.assetid: ad67fa19-f927-47ec-83b5-45a4f1f9cbe2
ms.date: 12/05/2018
ms.keywords: LOCALE_NOUSEROVERRIDE, VAR_DATEVALUEONLY, VAR_TIMEVALUEONLY, VarCyFromStr, VarCyFromStr function [Automation], _oa96_VarCyFromStr, automat.varcyfromstr, oleauto/VarCyFromStr
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
 - VarCyFromStr
 - oleauto/VarCyFromStr
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
 - VarCyFromStr
---

# VarCyFromStr function


## -description

Converts an OLECHAR string to a currency value.

## -parameters

### -param strIn [in]

The value to convert.

### -param lcid [in]

The locale identifier.

### -param dwFlags [in]

One of more of the following flags.

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

### -param pcyOut [out]

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

