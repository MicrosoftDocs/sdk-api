---
UID: NF:tuner.IScanningTunerEx.TerminateCurrentScan
title: IScanningTunerEx::TerminateCurrentScan (tuner.h)
description: This topic applies to Windows Vista and later.
helpviewer_keywords: ["IScanningTunerEx interface [Microsoft TV Technologies]","TerminateCurrentScan method","IScanningTunerEx.TerminateCurrentScan","IScanningTunerEx::TerminateCurrentScan","IScanningTunerExTerminateCurrentScan","TerminateCurrentScan","TerminateCurrentScan method [Microsoft TV Technologies]","TerminateCurrentScan method [Microsoft TV Technologies]","IScanningTunerEx interface","mstv.iscanningtunerex_terminatecurrentscan","tuner/IScanningTunerEx::TerminateCurrentScan"]
old-location: mstv\iscanningtunerex_terminatecurrentscan.htm
tech.root: mstv
ms.assetid: 5ab18d8a-1e79-45c2-a8b6-9c27ecb68de2
ms.date: 12/05/2018
ms.keywords: IScanningTunerEx interface [Microsoft TV Technologies],TerminateCurrentScan method, IScanningTunerEx.TerminateCurrentScan, IScanningTunerEx::TerminateCurrentScan, IScanningTunerExTerminateCurrentScan, TerminateCurrentScan, TerminateCurrentScan method [Microsoft TV Technologies], TerminateCurrentScan method [Microsoft TV Technologies],IScanningTunerEx interface, mstv.iscanningtunerex_terminatecurrentscan, tuner/IScanningTunerEx::TerminateCurrentScan
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
 - IScanningTunerEx::TerminateCurrentScan
 - tuner/IScanningTunerEx::TerminateCurrentScan
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
 - IScanningTunerEx.TerminateCurrentScan
---

# IScanningTunerEx::TerminateCurrentScan


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Windows Vista and later.
        



The <b>TerminateCurrentScan</b> method interrupts the current scan, if a scan is in progress.

## -parameters

### -param pcurrentFreq [out]

Receives the last frequency that the tuner scanned before halting.

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
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iscanningtunerex">IScanningTunerEx Interface</a>