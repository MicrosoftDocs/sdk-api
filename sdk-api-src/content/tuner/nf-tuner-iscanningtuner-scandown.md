---
UID: NF:tuner.IScanningTuner.ScanDown
title: IScanningTuner::ScanDown
author: windows-sdk-content
description: The ScanDown method changes the channel to the next lower channel with valid programming, pauses for the specified number of milliseconds, then repeats until canceled.
old-location: mstv\iscanningtuner_scandown.htm
old-project: mstv
ms.assetid: 0e9120be-9f8c-442e-8253-812b2917f902
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IScanningTuner interface [Microsoft TV Technologies],ScanDown method, IScanningTuner.ScanDown, IScanningTuner::ScanDown, IScanningTunerScanDown, ScanDown, ScanDown method [Microsoft TV Technologies], ScanDown method [Microsoft TV Technologies],IScanningTuner interface, mstv.iscanningtuner_scandown, tuner/IScanningTuner::ScanDown
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IScanningTuner.ScanDown
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/faa99b87-ddbb-4e38-8681-bd5c8c4f81f3">IScanningTuner Interface</a>
 

 

