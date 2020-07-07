---
UID: NF:manipulations.IManipulationProcessor.CompleteManipulation
title: IManipulationProcessor::CompleteManipulation (manipulations.h)
description: The CompleteManipulation method is called when the developer chooses to end the manipulation.
helpviewer_keywords: ["CompleteManipulation","CompleteManipulation method [Windows Touch]","CompleteManipulation method [Windows Touch]","IManipulationProcessor interface","IManipulationProcessor interface [Windows Touch]","CompleteManipulation method","IManipulationProcessor.CompleteManipulation","IManipulationProcessor::CompleteManipulation","manipulations/IManipulationProcessor::CompleteManipulation","wintouch.imanipulationprocessor_completemanipulation"]
old-location: wintouch\imanipulationprocessor_completemanipulation.htm
tech.root: wintouch
ms.assetid: 01779628-1f46-4cea-90fa-1093e26e0285
ms.date: 12/05/2018
ms.keywords: CompleteManipulation, CompleteManipulation method [Windows Touch], CompleteManipulation method [Windows Touch],IManipulationProcessor interface, IManipulationProcessor interface [Windows Touch],CompleteManipulation method, IManipulationProcessor.CompleteManipulation, IManipulationProcessor::CompleteManipulation, manipulations/IManipulationProcessor::CompleteManipulation, wintouch.imanipulationprocessor_completemanipulation
f1_keywords:
- manipulations/IManipulationProcessor.CompleteManipulation
dev_langs:
- c++
req.header: manipulations.h
req.include-header: Manipulations_i.c
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
- IManipulationProcessor.CompleteManipulation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IManipulationProcessor::CompleteManipulation


## -description


The <b>CompleteManipulation</b> method is called when the developer chooses to end the manipulation. 


## -parameters






## -returns



Returns <b>S_OK</b> on success, otherwise returns an error code such as <b>E_FAIL</b>.




## -remarks



This method raises the ManipulationCompleted() event in response.
  

During a Windows Touch gesture, manipulation gets started as soon as first touch input is sent for processing. 
  If <b>CompleteManipulation</b> is called before the second touch input gets a chance to be processed, 
  the second touch input will start a new manipulation.  
  




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor">IManipulationProcessor</a>



<a href="https://docs.microsoft.com/windows/desktop/wintouch/mtmethods">Methods</a>
 

 

