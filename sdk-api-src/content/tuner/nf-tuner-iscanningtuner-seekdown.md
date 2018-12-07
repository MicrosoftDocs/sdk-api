---
UID: NF:tuner.IScanningTuner.SeekDown
title: IScanningTuner::SeekDown
author: windows-sdk-content
description: The SeekDown method changes the channel to the next lower channel with valid programming.
old-location: mstv\iscanningtuner_seekdown.htm
tech.root: mstv
ms.assetid: ef78bae1-238f-4774-ab9a-b3681ba53656
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IScanningTuner interface [Microsoft TV Technologies],SeekDown method, IScanningTuner.SeekDown, IScanningTuner::SeekDown, IScanningTunerSeekDown, SeekDown, SeekDown method [Microsoft TV Technologies], SeekDown method [Microsoft TV Technologies],IScanningTuner interface, mstv.iscanningtuner_seekdown, tuner/IScanningTuner::SeekDown
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
 - IScanningTuner.SeekDown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IScanningTuner::SeekDown


## -description



The <b>SeekDown</b> method changes the channel to the next lower channel with valid programming.




## -parameters






## -returns



When the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -remarks



This method returns immediately, and the seek continues in the background. The seek can be canceled by calling any other tuning operation.

Currently the DVB-C and DVB-S Network Provider filters do not implement this method, and return E_NOTIMPL. The method is implemented for DVB-T.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/faa99b87-ddbb-4e38-8681-bd5c8c4f81f3">IScanningTuner Interface</a>
 

 

