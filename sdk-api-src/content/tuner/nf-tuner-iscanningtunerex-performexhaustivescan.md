---
UID: NF:tuner.IScanningTunerEx.PerformExhaustiveScan
title: IScanningTunerEx::PerformExhaustiveScan (tuner.h)
description: This topic applies to Windows Vista and later.
helpviewer_keywords: ["IScanningTunerEx interface [Microsoft TV Technologies]","PerformExhaustiveScan method","IScanningTunerEx.PerformExhaustiveScan","IScanningTunerEx::PerformExhaustiveScan","IScanningTunerExPerformExhaustiveScan","PerformExhaustiveScan","PerformExhaustiveScan method [Microsoft TV Technologies]","PerformExhaustiveScan method [Microsoft TV Technologies]","IScanningTunerEx interface","mstv.iscanningtunerex_performexhaustivescan","tuner/IScanningTunerEx::PerformExhaustiveScan"]
old-location: mstv\iscanningtunerex_performexhaustivescan.htm
tech.root: mstv
ms.assetid: 35ed1b43-020e-4baa-9f15-eb316d9a137b
ms.date: 12/05/2018
ms.keywords: IScanningTunerEx interface [Microsoft TV Technologies],PerformExhaustiveScan method, IScanningTunerEx.PerformExhaustiveScan, IScanningTunerEx::PerformExhaustiveScan, IScanningTunerExPerformExhaustiveScan, PerformExhaustiveScan, PerformExhaustiveScan method [Microsoft TV Technologies], PerformExhaustiveScan method [Microsoft TV Technologies],IScanningTunerEx interface, mstv.iscanningtunerex_performexhaustivescan, tuner/IScanningTunerEx::PerformExhaustiveScan
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - IScanningTunerEx::PerformExhaustiveScan
 - tuner/IScanningTunerEx::PerformExhaustiveScan
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tuner.h
api_name:
 - IScanningTunerEx.PerformExhaustiveScan
---

# IScanningTunerEx::PerformExhaustiveScan


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Windows Vista and later.
        



The <b>PerformExhaustiveScan</b> method scans a range of frequencies until the tuner locks onto a signal.

## -parameters

### -param dwLowerFreq [in]

Lowest frequency in the range of frequencies to scan. A value of -1 specifies the minimum frequency as determined by the device.

### -param dwHigherFreq [in]

Highest frequency in the range of frequencies to scan. A value of -1 specifies the maximum frequency as determined by the device.

### -param bFineTune [in]

Specifies whether the tuner performs fine tuning. When the tuner locks onto a frequency, if this parameter is <b>VARIANT_TRUE</b>, the tuner does fine tuning to find the best possible signal around that frequency.

### -param hEvent [in]

Handle to an event created by the application. When the tuner locks onto a signal, it signals this event.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_FALSE</dt>
</dl>
</td>
<td width="60%">
No scan is currently in progress.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_INVALIDARG</dt>
</dl>
</td>
<td width="60%">
Invalid frequency argument (for example, 0 <i>dwLowerFrequency</i> or <i>dwHigherFreq</i> value or <i>dwLowerFrequency</i> &gt;= <i>dwHigherFreq</i>).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -remarks

This method is asynchronous.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iscanningtunerex">IScanningTunerEx Interface</a>