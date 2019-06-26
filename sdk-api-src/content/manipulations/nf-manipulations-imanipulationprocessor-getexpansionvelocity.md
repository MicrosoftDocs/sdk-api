---
UID: NF:manipulations.IManipulationProcessor.GetExpansionVelocity
title: IManipulationProcessor::GetExpansionVelocity (manipulations.h)
author: windows-sdk-content
description: The GetExpansionVelocity method calculates the rate that the target object is expanding at.
old-location: wintouch\imanipulationprocessor_getexpansionvelocity.htm
tech.root: wintouch
ms.assetid: 5dbaeaa3-4abf-485e-9f84-8450dce14fc9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetExpansionVelocity, GetExpansionVelocity method [Windows Touch], GetExpansionVelocity method [Windows Touch],IManipulationProcessor interface, IManipulationProcessor interface [Windows Touch],GetExpansionVelocity method, IManipulationProcessor.GetExpansionVelocity, IManipulationProcessor::GetExpansionVelocity, manipulations/IManipulationProcessor::GetExpansionVelocity, wintouch.imanipulationprocessor_getexpansionvelocity
ms.topic: method
f1_keywords: 
 - "manipulations/IManipulationProcessor.GetExpansionVelocity"
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
 - IManipulationProcessor.GetExpansionVelocity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IManipulationProcessor::GetExpansionVelocity


## -description


The <b>GetExpansionVelocity</b> method calculates the rate that the target object is expanding at.


## -parameters




### -param expansionVelocity [out]

The rate of expansion.


## -returns



Returns <b>S_OK</b> on success, otherwise returns an error code such as <b>E_FAIL</b>.




## -remarks



This value is useful when you are using the <a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a> interface. You should pass this value when the manipulation completes.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor">IManipulationProcessor</a>



<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialexpansionvelocity">InitialExpansionVelocity</a>



<a href="https://docs.microsoft.com/windows/desktop/wintouch/mtmethods">Methods</a>
 

 

