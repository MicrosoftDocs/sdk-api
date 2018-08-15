---
UID: NF:tuner.IScanningTuner.SeekUp
title: IScanningTuner::SeekUp
author: windows-sdk-content
description: The SeekUp method changes the channel to the next higher channel with valid programming.
old-location: mstv\iscanningtuner_seekup.htm
old-project: mstv
ms.assetid: 43588b31-cac0-44c4-a282-b5939fed4ce7
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IScanningTuner interface [Microsoft TV Technologies],SeekUp method, IScanningTuner.SeekUp, IScanningTuner::SeekUp, IScanningTunerSeekUp, SeekUp, SeekUp method [Microsoft TV Technologies], SeekUp method [Microsoft TV Technologies],IScanningTuner interface, mstv.iscanningtuner_seekup, tuner/IScanningTuner::SeekUp
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tuner.h
req.include-header: 
req.redist: 
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
 - IScanningTuner.SeekUp
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IScanningTuner::SeekUp


## -description



The <b>SeekUp</b> method changes the channel to the next higher channel with valid programming.




## -parameters






## -returns



When the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -remarks



This method returns immediately, and the seek continues in the background. The seek can be canceled by calling any other tuning operation.

Currently the DVB-C and DVB-S Network Provider filters do not implement this method, and return E_NOTIMPL. The method is implemented for DVB-T.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/faa99b87-ddbb-4e38-8681-bd5c8c4f81f3">IScanningTuner Interface</a>
 

 

