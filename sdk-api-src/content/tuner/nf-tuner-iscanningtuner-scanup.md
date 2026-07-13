---
UID: NF:tuner.IScanningTuner.ScanUp
title: IScanningTuner::ScanUp (tuner.h)
description: The ScanUp method changes the channel to the next higher channel with valid programming, pauses for the specified number of milliseconds, then repeats until canceled.
helpviewer_keywords: ["IScanningTuner interface [Microsoft TV Technologies]","ScanUp method","IScanningTuner.ScanUp","IScanningTuner::ScanUp","IScanningTunerScanUp","ScanUp","ScanUp method [Microsoft TV Technologies]","ScanUp method [Microsoft TV Technologies]","IScanningTuner interface","mstv.iscanningtuner_scanup","tuner/IScanningTuner::ScanUp"]
old-location: mstv\iscanningtuner_scanup.htm
tech.root: mstv
ms.assetid: 2fa4d316-9f92-47d6-962f-ffe5c7e90a28
ms.date: 12/05/2018
ms.keywords: IScanningTuner interface [Microsoft TV Technologies],ScanUp method, IScanningTuner.ScanUp, IScanningTuner::ScanUp, IScanningTunerScanUp, ScanUp, ScanUp method [Microsoft TV Technologies], ScanUp method [Microsoft TV Technologies],IScanningTuner interface, mstv.iscanningtuner_scanup, tuner/IScanningTuner::ScanUp
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
 - IScanningTuner::ScanUp
 - tuner/IScanningTuner::ScanUp
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IScanningTuner.ScanUp
---

# IScanningTuner::ScanUp


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>ScanUp</b> method changes the channel to the next higher channel with valid programming, pauses for the specified number of milliseconds, then repeats until canceled.

## -parameters

### -param MillisecondsPause [in]

The number of milliseconds to pause.

## -returns

When the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -remarks

The call returns immediately, while the scan continues in the background. The scan can be canceled by calling any other tuning operation.

Currently the DVB-C and DVB-S Network Provider filters do not implement this method, and return E_NOTIMPL. The method is implemented for DVB-T.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iscanningtuner">IScanningTuner Interface</a>