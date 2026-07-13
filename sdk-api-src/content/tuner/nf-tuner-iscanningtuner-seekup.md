---
UID: NF:tuner.IScanningTuner.SeekUp
title: IScanningTuner::SeekUp (tuner.h)
description: The SeekUp method changes the channel to the next higher channel with valid programming.
helpviewer_keywords: ["IScanningTuner interface [Microsoft TV Technologies]","SeekUp method","IScanningTuner.SeekUp","IScanningTuner::SeekUp","IScanningTunerSeekUp","SeekUp","SeekUp method [Microsoft TV Technologies]","SeekUp method [Microsoft TV Technologies]","IScanningTuner interface","mstv.iscanningtuner_seekup","tuner/IScanningTuner::SeekUp"]
old-location: mstv\iscanningtuner_seekup.htm
tech.root: mstv
ms.assetid: 43588b31-cac0-44c4-a282-b5939fed4ce7
ms.date: 12/05/2018
ms.keywords: IScanningTuner interface [Microsoft TV Technologies],SeekUp method, IScanningTuner.SeekUp, IScanningTuner::SeekUp, IScanningTunerSeekUp, SeekUp, SeekUp method [Microsoft TV Technologies], SeekUp method [Microsoft TV Technologies],IScanningTuner interface, mstv.iscanningtuner_seekup, tuner/IScanningTuner::SeekUp
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
 - IScanningTuner::SeekUp
 - tuner/IScanningTuner::SeekUp
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
 - IScanningTuner.SeekUp
---

# IScanningTuner::SeekUp


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>SeekUp</b> method changes the channel to the next higher channel with valid programming.



## -returns

When the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -remarks

This method returns immediately, and the seek continues in the background. The seek can be canceled by calling any other tuning operation.

Currently the DVB-C and DVB-S Network Provider filters do not implement this method, and return E_NOTIMPL. The method is implemented for DVB-T.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iscanningtuner">IScanningTuner Interface</a>
