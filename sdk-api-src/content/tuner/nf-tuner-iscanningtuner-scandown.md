---
UID: NF:tuner.IScanningTuner.ScanDown
title: IScanningTuner::ScanDown (tuner.h)
author: windows-sdk-content
description: The ScanDown method changes the channel to the next lower channel with valid programming, pauses for the specified number of milliseconds, then repeats until canceled.
old-location: mstv\iscanningtuner_scandown.htm
tech.root: mstv
ms.assetid: 0e9120be-9f8c-442e-8253-812b2917f902
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IScanningTuner interface [Microsoft TV Technologies],ScanDown method, IScanningTuner.ScanDown, IScanningTuner::ScanDown, IScanningTunerScanDown, ScanDown, ScanDown method [Microsoft TV Technologies], ScanDown method [Microsoft TV Technologies],IScanningTuner interface, mstv.iscanningtuner_scandown, tuner/IScanningTuner::ScanDown
ms.topic: method
f1_keywords: 
 - "tuner/IScanningTuner.ScanDown"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IScanningTuner.ScanDown
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IScanningTuner::ScanDown


## -description



The <b>ScanDown</b> method changes the channel to the next lower channel with valid programming, pauses for the specified number of milliseconds, then repeats until canceled.




## -parameters




### -param MillisecondsPause [in]

The number of milliseconds to pause.


## -returns



When the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -remarks



The call returns immediately, while the scan continues in the background. The scan can be canceled by calling any other tuning operation.

Currently the DVB-C and DVB-S Network Provider filters do not implement this method, and return E_NOTIMPL. The method is implemented for DVB-T.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-iscanningtuner">IScanningTuner Interface</a>
 

 

