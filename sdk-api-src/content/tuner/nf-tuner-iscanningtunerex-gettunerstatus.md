---
UID: NF:tuner.IScanningTunerEx.GetTunerStatus
title: IScanningTunerEx::GetTunerStatus (tuner.h)
description: This topic applies to Windows Vista and later.
helpviewer_keywords: ["GetTunerStatus","GetTunerStatus method [Microsoft TV Technologies]","GetTunerStatus method [Microsoft TV Technologies]","IScanningTunerEx interface","IScanningTunerEx interface [Microsoft TV Technologies]","GetTunerStatus method","IScanningTunerEx.GetTunerStatus","IScanningTunerEx::GetTunerStatus","IScanningTunerExGetTunerStatus","mstv.iscanningtunerex_gettunerstatus","tuner/IScanningTunerEx::GetTunerStatus"]
old-location: mstv\iscanningtunerex_gettunerstatus.htm
tech.root: mstv
ms.assetid: 9e91f5ca-5a2e-414e-bf4c-882ba6a08b98
ms.date: 12/05/2018
ms.keywords: GetTunerStatus, GetTunerStatus method [Microsoft TV Technologies], GetTunerStatus method [Microsoft TV Technologies],IScanningTunerEx interface, IScanningTunerEx interface [Microsoft TV Technologies],GetTunerStatus method, IScanningTunerEx.GetTunerStatus, IScanningTunerEx::GetTunerStatus, IScanningTunerExGetTunerStatus, mstv.iscanningtunerex_gettunerstatus, tuner/IScanningTunerEx::GetTunerStatus
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
 - IScanningTunerEx::GetTunerStatus
 - tuner/IScanningTunerEx::GetTunerStatus
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
 - IScanningTunerEx.GetTunerStatus
---

# IScanningTunerEx::GetTunerStatus


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Windows Vista and later.
        



The <b>GetTunerStatus</b> method returns the current status of the most recent call to <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-iscanningtunerex-performexhaustivescan">PerformExhaustiveScan</a>.

## -parameters

### -param SecondsLeft [out]

Receives the estimated number of seconds remaining for the scan to complete.

### -param CurrentLockType [out]

Receives a member of the <a href="/previous-versions/windows/desktop/mstv/tunerlocktype">TunerLockType</a> enumeration, indicating how well the tuner locked onto a signal.

### -param AutoDetect [out]

Receives a Boolean value. If the value is <b>TRUE</b>, the tuner is in auto-detect mode.

### -param CurrentFreq [out]

Receives the frequency that was most recently scanned.

## -returns

When the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -remarks

While the scan is in progress, the application can use this method to estimate the total time required for the scan to complete. When the tuner locks onto a frequency and sets the application's event handle, the application can use this method to find the locked frequency.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iscanningtunerex">IScanningTunerEx Interface</a>