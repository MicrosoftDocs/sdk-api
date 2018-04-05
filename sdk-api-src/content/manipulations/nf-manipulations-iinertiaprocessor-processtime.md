---
UID: NF:manipulations.IInertiaProcessor.ProcessTime
title: IInertiaProcessor::ProcessTime method
author: windows-driver-content
description: The ProcessTime method performs calculations for the given tick and can raise the Started, Delta, or Completed event depending on whether extrapolation is completed or not. If extrapolation finished at the previous tick, the method is no-op.
old-location: wintouch\iinertiaprocessor_processtime.htm
old-project: wintouch
ms.assetid: 06132573-e198-4b2c-922b-3eeda53ac10b
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IInertiaProcessor, IInertiaProcessor interface [Windows Touch], ProcessTime method, IInertiaProcessor::ProcessTime, ProcessTime method [Windows Touch], ProcessTime method [Windows Touch], IInertiaProcessor interface, ProcessTime,IInertiaProcessor.ProcessTime, manipulations/IInertiaProcessor::ProcessTime, wintouch.iinertiaprocessor_processtime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: manipulations.h
req.include-header: Manipulations.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MANIPULATION_PROCESSOR_MANIPULATIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	manipulations.h
api_name:
-	IInertiaProcessor.ProcessTime
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IInertiaProcessor::ProcessTime method


## -description


The <b>ProcessTime</b> method performs calculations for the given tick and can raise the <b>Started</b>, <b>Delta</b>, or <b>Completed</b> event depending on whether extrapolation is completed or not. If extrapolation finished at the previous tick, the method is no-op.


## -parameters




### -param timestamp [in]

A parameter that contains a timestamp (in millisecs) to process.


### -param completed [out]

Indicates whether an operation was performed. A value of false indicates extrapolation was finished at a previous tick and the operation was a no-op.


## -returns



Returns <b>S_OK</b> on success, otherwise returns an error code such as <b>E_FAIL</b>.




## -see-also




<a href="https://msdn.microsoft.com/8dc171eb-0c6e-41dd-b506-5f91ea703a53">IInertiaProcessor</a>



<a href="https://msdn.microsoft.com/e4acfcac-06c1-42a5-9722-4534a4492ab8">Methods</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn756307">Process</a>
 

 

