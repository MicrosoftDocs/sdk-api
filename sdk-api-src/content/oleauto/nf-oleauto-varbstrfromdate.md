---
UID: NF:oleauto.VarBstrFromDate
title: VarBstrFromDate function (oleauto.h)
description: Converts a date value to a BSTR value.
helpviewer_keywords: ["LOCALE_NOUSEROVERRIDE","VAR_CALENDAR_GREGORIAN","VAR_CALENDAR_HIJRI","VAR_CALENDAR_THAI","VAR_DATEVALUEONLY","VAR_FOURDIGITYEARS","VAR_TIMEVALUEONLY","VarBstrFromDate","VarBstrFromDate function [Automation]","_oa96_VarBstrFromDate","automat.varbstrfromdate","oleauto/VarBstrFromDate"]
old-location: automat\varbstrfromdate.htm
tech.root: automat
ms.assetid: f9b22626-0f9f-4ef9-ab6d-7cea44b01eb6
ms.date: 12/05/2018
ms.keywords: LOCALE_NOUSEROVERRIDE, VAR_CALENDAR_GREGORIAN, VAR_CALENDAR_HIJRI, VAR_CALENDAR_THAI, VAR_DATEVALUEONLY, VAR_FOURDIGITYEARS, VAR_TIMEVALUEONLY, VarBstrFromDate, VarBstrFromDate function [Automation], _oa96_VarBstrFromDate, automat.varbstrfromdate, oleauto/VarBstrFromDate
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
 - VarBstrFromDate
 - oleauto/VarBstrFromDate
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
 - VarBstrFromDate
---

# VarBstrFromDate function


## -description

Converts a date value to a BSTR value.

## -parameters

### -param dateIn [in]

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
<td width="40%"><a id="VAR_CALENDAR_HIJRI"></a><a id="var_calendar_hijri"></a><dl>
<dt><b>VAR_CALENDAR_HIJRI</b></dt>
</dl>
</td>
<td width="60%">
If set then the Hijri calendar is used. Otherwise the calendar set in the control panel is used.


</td>
</tr>
<tr>
<td width="40%"><a id="VAR_CALENDAR_THAI"></a><a id="var_calendar_thai"></a><dl>
<dt><b>VAR_CALENDAR_THAI</b></dt>
</dl>
</td>
<td width="60%">
If set then the Buddhist year is used.


</td>
</tr>
<tr>
<td width="40%"><a id="VAR_CALENDAR_GREGORIAN"></a><a id="var_calendar_gregorian"></a><dl>
<dt><b>VAR_CALENDAR_GREGORIAN</b></dt>
</dl>
</td>
<td width="60%">
If set the Gregorian year is used.


</td>
</tr>
<tr>
<td width="40%"><a id="VAR_FOURDIGITYEARS"></a><a id="var_fourdigityears"></a><dl>
<dt><b>VAR_FOURDIGITYEARS</b></dt>
</dl>
</td>
<td width="60%">
Use 4-digit years instead of 2-digit years.

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

