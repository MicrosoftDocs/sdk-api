---
UID: NF:tuner.IScanningTuner.SeekDown
title: IScanningTuner::SeekDown (tuner.h)
description: The SeekDown method changes the channel to the next lower channel with valid programming.
helpviewer_keywords: ["IScanningTuner interface [Microsoft TV Technologies]","SeekDown method","IScanningTuner.SeekDown","IScanningTuner::SeekDown","IScanningTunerSeekDown","SeekDown","SeekDown method [Microsoft TV Technologies]","SeekDown method [Microsoft TV Technologies]","IScanningTuner interface","mstv.iscanningtuner_seekdown","tuner/IScanningTuner::SeekDown"]
old-location: mstv\iscanningtuner_seekdown.htm
tech.root: mstv
ms.assetid: ef78bae1-238f-4774-ab9a-b3681ba53656
ms.date: 12/05/2018
ms.keywords: IScanningTuner interface [Microsoft TV Technologies],SeekDown method, IScanningTuner.SeekDown, IScanningTuner::SeekDown, IScanningTunerSeekDown, SeekDown, SeekDown method [Microsoft TV Technologies], SeekDown method [Microsoft TV Technologies],IScanningTuner interface, mstv.iscanningtuner_seekdown, tuner/IScanningTuner::SeekDown
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
 - IScanningTuner::SeekDown
 - tuner/IScanningTuner::SeekDown
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
 - IScanningTuner.SeekDown
---

# IScanningTuner::SeekDown


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>SeekDown</b> method changes the channel to the next lower channel with valid programming.



## -returns

When the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -remarks

This method returns immediately, and the seek continues in the background. The seek can be canceled by calling any other tuning operation.

Currently the DVB-C and DVB-S Network Provider filters do not implement this method, and return E_NOTIMPL. The method is implemented for DVB-T.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iscanningtuner">IScanningTuner Interface</a>
