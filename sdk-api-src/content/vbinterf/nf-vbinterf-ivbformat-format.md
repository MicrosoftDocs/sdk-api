---
UID: NF:vbinterf.IVBFormat.Format
title: IVBFormat::Format (vbinterf.h)
description: Formats a string according to a pattern.
helpviewer_keywords: ["Format","Format method [COM]","Format method [COM]","IVBFormat interface","IVBFormat interface [COM]","Format method","IVBFormat.Format","IVBFormat::Format","_com_IVBFormat_Format","com.ivbformat_format","vbFirstFourDays","vbFirstFullWeek","vbFirstJan1","vbFriday","vbMonday","vbSaturday","vbSunday","vbThursday","vbTuesday","vbUseSystem","vbWednesday","vbinterf/IVBFormat::Format"]
old-location: com\ivbformat_format.htm
tech.root: com
ms.assetid: 62200cb0-3704-4caf-9152-1b7b0c43856a
ms.date: 12/05/2018
ms.keywords: Format, Format method [COM], Format method [COM],IVBFormat interface, IVBFormat interface [COM],Format method, IVBFormat.Format, IVBFormat::Format, _com_IVBFormat_Format, com.ivbformat_format, vbFirstFourDays, vbFirstFullWeek, vbFirstJan1, vbFriday, vbMonday, vbSaturday, vbSunday, vbThursday, vbTuesday, vbUseSystem, vbWednesday, vbinterf/IVBFormat::Format
req.header: vbinterf.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVBFormat::Format
 - vbinterf/IVBFormat::Format
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VbInterf.h
api_name:
 - IVBFormat.Format
---

# IVBFormat::Format


## -description

Formats a string according to a pattern.
<div class="alert"><b>Note</b>  The use of this method is no longer recommended because containers other than Visual Basic do not support 
    it.</div><div> </div>

## -parameters

### -param vData [in]

Data to be formatted.

### -param bstrFormat [in]

Format string to be applied to the data.

### -param lpBuffer [in]

Pointer to result buffer.

### -param cb [in]

Length of result buffer.

### -param lcid [in]

Locale ID.

### -param sFirstDayOfWeek [in]

Affects the 'w', FirstDayOfWeek, format result.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="vbUseSystem"></a><a id="vbusesystem"></a><a id="VBUSESYSTEM"></a><dl>
<dt><b>vbUseSystem</b></dt>
</dl>
</td>
<td width="60%">
Use the <b>FirstWeekday</b> setting in the host UI. If no host value is provided, 
        use the current system value from the NLS API.

</td>
</tr>
<tr>
<td width="40%"><a id="vbSunday"></a><a id="vbsunday"></a><a id="VBSUNDAY"></a><dl>
<dt><b>vbSunday</b></dt>
</dl>
</td>
<td width="60%">
Sunday

</td>
</tr>
<tr>
<td width="40%"><a id="vbMonday"></a><a id="vbmonday"></a><a id="VBMONDAY"></a><dl>
<dt><b>vbMonday</b></dt>
</dl>
</td>
<td width="60%">
Monday

</td>
</tr>
<tr>
<td width="40%"><a id="vbTuesday"></a><a id="vbtuesday"></a><a id="VBTUESDAY"></a><dl>
<dt><b>vbTuesday</b></dt>
</dl>
</td>
<td width="60%">
Tuesday

</td>
</tr>
<tr>
<td width="40%"><a id="vbWednesday"></a><a id="vbwednesday"></a><a id="VBWEDNESDAY"></a><dl>
<dt><b>vbWednesday</b></dt>
</dl>
</td>
<td width="60%">
Wednesday

</td>
</tr>
<tr>
<td width="40%"><a id="vbThursday"></a><a id="vbthursday"></a><a id="VBTHURSDAY"></a><dl>
<dt><b>vbThursday</b></dt>
</dl>
</td>
<td width="60%">
Thursday

</td>
</tr>
<tr>
<td width="40%"><a id="vbFriday"></a><a id="vbfriday"></a><a id="VBFRIDAY"></a><dl>
<dt><b>vbFriday</b></dt>
</dl>
</td>
<td width="60%">
Friday

</td>
</tr>
<tr>
<td width="40%"><a id="vbSaturday"></a><a id="vbsaturday"></a><a id="VBSATURDAY"></a><dl>
<dt><b>vbSaturday</b></dt>
</dl>
</td>
<td width="60%">
Saturday

</td>
</tr>
</table>

### -param sFirstWeekOfYear [in]

Affects the 'ww', FirstWeekOfYear, format result.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="vbUseSystem"></a><a id="vbusesystem"></a><a id="VBUSESYSTEM"></a><dl>
<dt><b>vbUseSystem</b></dt>
</dl>
</td>
<td width="60%">
Use the <b>FirstWeekOfYear</b> setting in the host UI. If no host value is provided, 
        use the current system value from the NLS API.

</td>
</tr>
<tr>
<td width="40%"><a id="vbFirstJan1"></a><a id="vbfirstjan1"></a><a id="VBFIRSTJAN1"></a><dl>
<dt><b>vbFirstJan1</b></dt>
</dl>
</td>
<td width="60%">
Start on January 1 (default).

</td>
</tr>
<tr>
<td width="40%"><a id="vbFirstFourDays"></a><a id="vbfirstfourdays"></a><a id="VBFIRSTFOURDAYS"></a><dl>
<dt><b>vbFirstFourDays</b></dt>
</dl>
</td>
<td width="60%">
Start with the first four-day week.

</td>
</tr>
<tr>
<td width="40%"><a id="vbFirstFullWeek"></a><a id="vbfirstfullweek"></a><a id="VBFIRSTFULLWEEK"></a><dl>
<dt><b>vbFirstFullWeek</b></dt>
</dl>
</td>
<td width="60%">
Start with the first full week.

</td>
</tr>
</table>

### -param rcb [out]

Number of bytes copied to the result buffer.

## -returns

This method supports the standard return values <b>E_INVALIDARG</b>, 
      <b>E_OUTOFMEMORY</b>, and <b>E_UNEXPECTED</b>, as well as the 
      following:

## -remarks

When migrating a VBX control to an OLE control, 
    <b>Format</b> replaces the Visual Basic 
    <b>VBFormat</b>, which is no longer supported.

## -see-also

<a href="/windows/desktop/api/vbinterf/nn-vbinterf-ivbformat">IVBFormat</a>