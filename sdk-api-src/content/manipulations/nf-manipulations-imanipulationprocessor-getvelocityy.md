---
UID: NF:manipulations.IManipulationProcessor.GetVelocityY
title: IManipulationProcessor::GetVelocityY (manipulations.h)
description: Calculates and returns the vertical velocity.
helpviewer_keywords: ["GetVelocityY","GetVelocityY method [Windows Touch]","GetVelocityY method [Windows Touch]","IManipulationProcessor interface","IManipulationProcessor interface [Windows Touch]","GetVelocityY method","IManipulationProcessor.GetVelocityY","IManipulationProcessor::GetVelocityY","manipulations/IManipulationProcessor::GetVelocityY","wintouch.imanipulationprocessor_getvelocityy"]
old-location: wintouch\imanipulationprocessor_getvelocityy.htm
tech.root: wintouch
ms.assetid: b531c4e5-8437-4869-9264-3fe131b8acc8
ms.date: 12/05/2018
ms.keywords: GetVelocityY, GetVelocityY method [Windows Touch], GetVelocityY method [Windows Touch],IManipulationProcessor interface, IManipulationProcessor interface [Windows Touch],GetVelocityY method, IManipulationProcessor.GetVelocityY, IManipulationProcessor::GetVelocityY, manipulations/IManipulationProcessor::GetVelocityY, wintouch.imanipulationprocessor_getvelocityy
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
 - IManipulationProcessor::GetVelocityY
 - manipulations/IManipulationProcessor::GetVelocityY
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
 - IManipulationProcessor.GetVelocityY
---

# IManipulationProcessor::GetVelocityY


## -description

Calculates and returns the vertical velocity.

## -parameters

### -param velocityY [out]

The calculated vertical velocity.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an HRESULT error code such as <b>E_FAIL</b>.

## -remarks

This value is useful when you are using the <a href="/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a> interface. You should pass this value when the manipulation completes.

## -see-also

<a href="/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getvelocityx">GetVelocityX</a>



<a href="/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor">IManipulationProcessor</a>



<a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialvelocityy">InitialVelocityY</a>



<a href="/windows/desktop/wintouch/mtmethods">Methods</a>