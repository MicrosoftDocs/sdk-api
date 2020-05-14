---
UID: NF:oleauto.VarBstrFromDec
title: VarBstrFromDec function (oleauto.h)
description: Converts a decimal value to a BSTR value.helpviewer_keywords: ["LOCALE_NOUSEROVERRIDE","VAR_DATEVALUEONLY","VAR_TIMEVALUEONLY","VarBstrFromDec","VarBstrFromDec function [Automation]","_oa96_VarBstrFromDec","automat.varbstrfromdec","oleauto/VarBstrFromDec"]
old-location: automat\varbstrfromdec.htm
tech.root: automat
ms.assetid: 8e4da8c0-b2e4-4611-8f7d-e415dfcc846c
ms.date: 12/05/2018
ms.keywords: LOCALE_NOUSEROVERRIDE, VAR_DATEVALUEONLY, VAR_TIMEVALUEONLY, VarBstrFromDec, VarBstrFromDec function [Automation], _oa96_VarBstrFromDec, automat.varbstrfromdec, oleauto/VarBstrFromDec
f1_keywords:
- oleauto/VarBstrFromDec
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- OleAut32.dll
api_name:
- VarBstrFromDec
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# VarBstrFromDec function


## -description


Converts a decimal value to a BSTR value.


## -parameters




### -param pdecIn [in]

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
Omits the date portion of a VT_DATE and returns only the time. Applies to conversions to or from dates. Not used for <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantchangetype">VariantChangeType</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantchangetypeex">VariantChangeTypeEx</a>.


</td>
</tr>
<tr>
<td width="40%"><a id="VAR_DATEVALUEONLY"></a><a id="var_datevalueonly"></a><dl>
<dt><b>VAR_DATEVALUEONLY</b></dt>
</dl>
</td>
<td width="60%">
Omits the time portion of a VT_DATE and returns only the date. Applies to conversions to or from dates. Not used for <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantchangetype">VariantChangeType</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantchangetypeex">VariantChangeTypeEx</a>.


</td>
</tr>
</table>
 


### -param pbstrOut [out]

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
 



