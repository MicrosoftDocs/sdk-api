---
UID: NF:manipulations.IManipulationProcessor.GetExpansionVelocity
title: IManipulationProcessor::GetExpansionVelocity (manipulations.h)
description: The GetExpansionVelocity method calculates the rate that the target object is expanding at.
helpviewer_keywords: ["GetExpansionVelocity","GetExpansionVelocity method [Windows Touch]","GetExpansionVelocity method [Windows Touch]","IManipulationProcessor interface","IManipulationProcessor interface [Windows Touch]","GetExpansionVelocity method","IManipulationProcessor.GetExpansionVelocity","IManipulationProcessor::GetExpansionVelocity","manipulations/IManipulationProcessor::GetExpansionVelocity","wintouch.imanipulationprocessor_getexpansionvelocity"]
old-location: wintouch\imanipulationprocessor_getexpansionvelocity.htm
tech.root: wintouch
ms.assetid: 5dbaeaa3-4abf-485e-9f84-8450dce14fc9
ms.date: 12/05/2018
ms.keywords: GetExpansionVelocity, GetExpansionVelocity method [Windows Touch], GetExpansionVelocity method [Windows Touch],IManipulationProcessor interface, IManipulationProcessor interface [Windows Touch],GetExpansionVelocity method, IManipulationProcessor.GetExpansionVelocity, IManipulationProcessor::GetExpansionVelocity, manipulations/IManipulationProcessor::GetExpansionVelocity, wintouch.imanipulationprocessor_getexpansionvelocity
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IManipulationProcessor::GetExpansionVelocity
 - manipulations/IManipulationProcessor::GetExpansionVelocity
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - manipulations.h
api_name:
 - IManipulationProcessor.GetExpansionVelocity
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

This value is useful when you are using the <a href="/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a> interface. You should pass this value when the manipulation completes.

## -see-also

<a href="/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor">IManipulationProcessor</a>



<a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialexpansionvelocity">InitialExpansionVelocity</a>



<a href="/windows/desktop/wintouch/mtmethods">Methods</a>