---
UID: NF:tuner.IScanningTuner.AutoProgram
title: IScanningTuner::AutoProgram method
author: windows-driver-content
description: The AutoProgram method scans for all channels with valid programming.
old-location: mstv\iscanningtuner_autoprogram.htm
old-project: mstv
ms.assetid: 98d1b484-13e7-4eeb-9e0c-a1215712bdc8
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: AutoProgram method [Microsoft TV Technologies], AutoProgram method [Microsoft TV Technologies], IScanningTuner interface, AutoProgram,IScanningTuner.AutoProgram, IScanningTuner, IScanningTuner interface [Microsoft TV Technologies], AutoProgram method, IScanningTuner::AutoProgram, IScanningTunerAutoProgram, mstv.iscanningtuner_autoprogram, tuner/IScanningTuner::AutoProgram
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
-	IScanningTuner.AutoProgram
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IScanningTuner::AutoProgram method


## -description



The <b>AutoProgram</b> method scans for all channels with valid programming.




## -parameters






## -returns



When the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -remarks



This method returns immediately, and the scan continues in the background. If the device allows it, the scan can be canceled by calling any other tuning operation. Otherwise, the scan will complete once all channels have been visited once. Internal devices will likely have a software implementation of this feature, and will collect fine-tuning information resulting from the scan. External devices will likely implement this feature, so this is just a means to trigger the process.

Currently the DVB-C and DVB-S Network Provider filters do not implement this method, and return E_NOTIMPL. The method is implemented for DVB-T.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/faa99b87-ddbb-4e38-8681-bd5c8c4f81f3">IScanningTuner Interface</a>
 

 

