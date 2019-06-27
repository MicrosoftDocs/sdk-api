---
UID: NF:manipulations.IManipulationProcessor.ProcessUp
title: IManipulationProcessor::ProcessUp (manipulations.h)
author: windows-sdk-content
description: The ProcessUp method feeds data to a target's manipulation processor for touch up sequences.
old-location: wintouch\imanipulationprocessor_processup.htm
tech.root: wintouch
ms.assetid: c93f6729-5e50-41a1-867c-93e4ce9ecda9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IManipulationProcessor interface [Windows Touch],ProcessUp method, IManipulationProcessor.ProcessUp, IManipulationProcessor::ProcessUp, ProcessUp, ProcessUp method [Windows Touch], ProcessUp method [Windows Touch],IManipulationProcessor interface, manipulations/IManipulationProcessor::ProcessUp, wintouch.imanipulationprocessor_processup
ms.topic: method
f1_keywords: 
 - "manipulations/IManipulationProcessor.ProcessUp"
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
 - IManipulationProcessor.ProcessUp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IManipulationProcessor::ProcessUp


## -description


The <b>ProcessUp</b> method feeds data to a target's manipulation processor for touch up sequences.


## -parameters




### -param manipulatorId

The identifier for the touch contact that you want to process.


### -param x

The horizontal coordinate data associated with the target.


### -param y

The vertical coordinate data associated with the target.


## -returns



Returns <b>S_OK</b> on success, otherwise returns an error code such as <b>E_FAIL</b>.




## -remarks



This method takes a timestamp using system time rather than from the touch hardware. To improve the experience in 
    cases where performance is degrading you should use the <a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime">ProcessUpWithTime</a> method.    




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor">IManipulationProcessor</a>



<a href="https://docs.microsoft.com/windows/desktop/wintouch/mtmethods">Methods</a>



<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdown">ProcessDown</a>



<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmove">ProcessMove</a>



<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime">ProcessUpWithTime</a>
 

 

