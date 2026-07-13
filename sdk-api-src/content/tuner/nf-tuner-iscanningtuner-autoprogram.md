---
UID: NF:tuner.IScanningTuner.AutoProgram
title: IScanningTuner::AutoProgram (tuner.h)
description: The AutoProgram method scans for all channels with valid programming.
helpviewer_keywords: ["AutoProgram","AutoProgram method [Microsoft TV Technologies]","AutoProgram method [Microsoft TV Technologies]","IScanningTuner interface","IScanningTuner interface [Microsoft TV Technologies]","AutoProgram method","IScanningTuner.AutoProgram","IScanningTuner::AutoProgram","IScanningTunerAutoProgram","mstv.iscanningtuner_autoprogram","tuner/IScanningTuner::AutoProgram"]
old-location: mstv\iscanningtuner_autoprogram.htm
tech.root: mstv
ms.assetid: 98d1b484-13e7-4eeb-9e0c-a1215712bdc8
ms.date: 12/05/2018
ms.keywords: AutoProgram, AutoProgram method [Microsoft TV Technologies], AutoProgram method [Microsoft TV Technologies],IScanningTuner interface, IScanningTuner interface [Microsoft TV Technologies],AutoProgram method, IScanningTuner.AutoProgram, IScanningTuner::AutoProgram, IScanningTunerAutoProgram, mstv.iscanningtuner_autoprogram, tuner/IScanningTuner::AutoProgram
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
 - IScanningTuner::AutoProgram
 - tuner/IScanningTuner::AutoProgram
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
 - IScanningTuner.AutoProgram
---

# IScanningTuner::AutoProgram


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>AutoProgram</b> method scans for all channels with valid programming.



## -returns

When the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -remarks

This method returns immediately, and the scan continues in the background. If the device allows it, the scan can be canceled by calling any other tuning operation. Otherwise, the scan will complete once all channels have been visited once. Internal devices will likely have a software implementation of this feature, and will collect fine-tuning information resulting from the scan. External devices will likely implement this feature, so this is just a means to trigger the process.

Currently the DVB-C and DVB-S Network Provider filters do not implement this method, and return E_NOTIMPL. The method is implemented for DVB-T.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iscanningtuner">IScanningTuner Interface</a>
