---
UID: NF:tuner.IScanningTunerEx.ResumeCurrentScan
title: IScanningTunerEx::ResumeCurrentScan (tuner.h)
description: This topic applies to Windows Vista and later.
helpviewer_keywords: ["IScanningTunerEx interface [Microsoft TV Technologies]","ResumeCurrentScan method","IScanningTunerEx.ResumeCurrentScan","IScanningTunerEx::ResumeCurrentScan","IScanningTunerExResumeCurrentScan","ResumeCurrentScan","ResumeCurrentScan method [Microsoft TV Technologies]","ResumeCurrentScan method [Microsoft TV Technologies]","IScanningTunerEx interface","mstv.iscanningtunerex_resumecurrentscan","tuner/IScanningTunerEx::ResumeCurrentScan"]
old-location: mstv\iscanningtunerex_resumecurrentscan.htm
tech.root: mstv
ms.assetid: 9d855ae4-a49c-43d6-9ba0-9f6158f4034f
ms.date: 12/05/2018
ms.keywords: IScanningTunerEx interface [Microsoft TV Technologies],ResumeCurrentScan method, IScanningTunerEx.ResumeCurrentScan, IScanningTunerEx::ResumeCurrentScan, IScanningTunerExResumeCurrentScan, ResumeCurrentScan, ResumeCurrentScan method [Microsoft TV Technologies], ResumeCurrentScan method [Microsoft TV Technologies],IScanningTunerEx interface, mstv.iscanningtunerex_resumecurrentscan, tuner/IScanningTunerEx::ResumeCurrentScan
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
 - IScanningTunerEx::ResumeCurrentScan
 - tuner/IScanningTunerEx::ResumeCurrentScan
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
 - IScanningTunerEx.ResumeCurrentScan
---

# IScanningTunerEx::ResumeCurrentScan


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Windows Vista and later.
        



The <b>ResumeCurrentScan</b> method resumes scanning the range of frequencies specified in <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-iscanningtunerex-performexhaustivescan">PerformExhaustiveScan</a>.

## -parameters

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
No scan has been started yet.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_INVALIDARG</dt>
</dl>
</td>
<td width="60%">
Invalid <i>hEvent</i> argument.

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
 

When the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -remarks

When the application calls <b>PerformExhaustiveScan</b>, the tuner scans until it locks onto a signal. Then it sets the application's event handle. To resume scanning for the next valid signal in original range of frequencies, the application can call <b>ResumeCurrentScan</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iscanningtunerex">IScanningTunerEx Interface</a>