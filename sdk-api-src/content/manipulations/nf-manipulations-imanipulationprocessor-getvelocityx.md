---
UID: NF:manipulations.IManipulationProcessor.GetVelocityX
title: IManipulationProcessor::GetVelocityX (manipulations.h)
description: Calculates and returns the horizontal velocity for the target object.
helpviewer_keywords: ["GetVelocityX","GetVelocityX method [Windows Touch]","GetVelocityX method [Windows Touch]","IManipulationProcessor interface","IManipulationProcessor interface [Windows Touch]","GetVelocityX method","IManipulationProcessor.GetVelocityX","IManipulationProcessor::GetVelocityX","manipulations/IManipulationProcessor::GetVelocityX","wintouch.imanipulationprocessor_getvelocityx"]
old-location: wintouch\imanipulationprocessor_getvelocityx.htm
tech.root: wintouch
ms.assetid: 64524f01-f7b2-4e78-97b8-20686018469f
ms.date: 12/05/2018
ms.keywords: GetVelocityX, GetVelocityX method [Windows Touch], GetVelocityX method [Windows Touch],IManipulationProcessor interface, IManipulationProcessor interface [Windows Touch],GetVelocityX method, IManipulationProcessor.GetVelocityX, IManipulationProcessor::GetVelocityX, manipulations/IManipulationProcessor::GetVelocityX, wintouch.imanipulationprocessor_getvelocityx
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
 - IManipulationProcessor::GetVelocityX
 - manipulations/IManipulationProcessor::GetVelocityX
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
 - IManipulationProcessor.GetVelocityX
---

# IManipulationProcessor::GetVelocityX


## -description

Calculates and returns the horizontal velocity for the target object.

## -parameters

### -param velocityX [out]

The calculated horizontal velocity.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an HRESULT error code such as <b>E_FAIL</b>.

## -remarks

This value is useful when you are using the <a href="/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a> interface. You should pass this value when the manipulation completes.

## -see-also

<a href="/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getvelocityy">GetVelocityY</a>



<a href="/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor">IManipulationProcessor</a>



<a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialvelocityx">InitialVelocityX</a>



<a href="/windows/desktop/wintouch/mtmethods">Methods</a>