---
UID: NF:manipulations.IInertiaProcessor.ProcessTime
title: IInertiaProcessor::ProcessTime (manipulations.h)
author: windows-sdk-content
description: The ProcessTime method performs calculations for the given tick and can raise the Started, Delta, or Completed event depending on whether extrapolation is completed or not. If extrapolation finished at the previous tick, the method is no-op.
old-location: wintouch\iinertiaprocessor_processtime.htm
tech.root: wintouch
ms.assetid: 06132573-e198-4b2c-922b-3eeda53ac10b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IInertiaProcessor interface [Windows Touch],ProcessTime method, IInertiaProcessor.ProcessTime, IInertiaProcessor::ProcessTime, ProcessTime, ProcessTime method [Windows Touch], ProcessTime method [Windows Touch],IInertiaProcessor interface, manipulations/IInertiaProcessor::ProcessTime, wintouch.iinertiaprocessor_processtime
ms.topic: method
f1_keywords: 
 - "manipulations/IInertiaProcessor.ProcessTime"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - manipulations.h
api_name:
 - IInertiaProcessor.ProcessTime
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInertiaProcessor::ProcessTime


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




<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a>



<a href="https://docs.microsoft.com/windows/desktop/wintouch/imanipulationprocessor-methods">Methods</a>



<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process">Process</a>
 

 

