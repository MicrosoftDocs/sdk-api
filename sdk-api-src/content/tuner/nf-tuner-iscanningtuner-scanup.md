---
UID: NF:tuner.IScanningTuner.ScanUp
title: IScanningTuner::ScanUp
author: windows-driver-content
description: The ScanUp method changes the channel to the next higher channel with valid programming, pauses for the specified number of milliseconds, then repeats until canceled.
old-location: mstv\iscanningtuner_scanup.htm
old-project: mstv
ms.assetid: 2fa4d316-9f92-47d6-962f-ffe5c7e90a28
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IScanningTuner interface [Microsoft TV Technologies],ScanUp method, IScanningTuner.ScanUp, IScanningTuner::ScanUp, IScanningTunerScanUp, ScanUp, ScanUp method [Microsoft TV Technologies], ScanUp method [Microsoft TV Technologies],IScanningTuner interface, mstv.iscanningtuner_scanup, tuner/IScanningTuner::ScanUp
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IScanningTuner.ScanUp
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IScanningTuner::ScanUp


## -description



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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/faa99b87-ddbb-4e38-8681-bd5c8c4f81f3">IScanningTuner Interface</a>
 

 

