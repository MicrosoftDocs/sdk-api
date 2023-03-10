---
UID: NF:manipulations.IInertiaProcessor.put_InitialVelocityY
title: IInertiaProcessor::put_InitialVelocityY (manipulations.h)
description: The InitialVelocityY property specifies the initial movement of the target object on the vertical axis. (Put)
helpviewer_keywords: ["IInertiaProcessor interface [Windows Touch]","InitialVelocityY property","IInertiaProcessor.InitialVelocityY","IInertiaProcessor.put_InitialVelocityY","IInertiaProcessor::InitialVelocityY","IInertiaProcessor::get_InitialVelocityY","IInertiaProcessor::put_InitialVelocityY","InitialVelocityY property [Windows Touch]","InitialVelocityY property [Windows Touch]","IInertiaProcessor interface","manipulations/IInertiaProcessor::InitialVelocityY","manipulations/IInertiaProcessor::get_InitialVelocityY","manipulations/IInertiaProcessor::put_InitialVelocityY","put_InitialVelocityY","wintouch.iinertiaprocessor_initialvelocityy"]
old-location: wintouch\iinertiaprocessor_initialvelocityy.htm
tech.root: wintouch
ms.assetid: 3ba0aa0c-a819-4833-883b-218702052ce1
ms.date: 12/05/2018
ms.keywords: IInertiaProcessor interface [Windows Touch],InitialVelocityY property, IInertiaProcessor.InitialVelocityY, IInertiaProcessor.put_InitialVelocityY, IInertiaProcessor::InitialVelocityY, IInertiaProcessor::get_InitialVelocityY, IInertiaProcessor::put_InitialVelocityY, InitialVelocityY property [Windows Touch], InitialVelocityY property [Windows Touch],IInertiaProcessor interface, manipulations/IInertiaProcessor::InitialVelocityY, manipulations/IInertiaProcessor::get_InitialVelocityY, manipulations/IInertiaProcessor::put_InitialVelocityY, put_InitialVelocityY, wintouch.iinertiaprocessor_initialvelocityy
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInertiaProcessor::put_InitialVelocityY
 - manipulations/IInertiaProcessor::put_InitialVelocityY
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
 - IInertiaProcessor.InitialVelocityY
 - IInertiaProcessor.get_InitialVelocityY
 - IInertiaProcessor.put_InitialVelocityY
---

# IInertiaProcessor::put_InitialVelocityY


## -description

The <b>InitialVelocityY</b> property specifies the initial movement of the target object on the vertical axis.

This property is read/write.

## -parameters

## -remarks

If inertia processing has already started, setting <b>InitialVelocityY</b> will reset the inertia engine to the initial state with new velocity values applied.		
		

Call this function to set the initial state of inertia. You would call this function most likely during the <a href="/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted">ManipulationCompleted</a> event of the <a href="/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor">IManipulationProcessor</a> or in the constructor of the <a href="/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a> interface.

## -see-also

<a href="/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getvelocityy">GetVelocityY</a>



<a href="/windows/desktop/wintouch/handling-inertia-in-unmanaged-code">Handling Inertia in Unmanaged Code</a>



<a href="/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a>



<a href="/windows/desktop/wintouch/inertia-mechanics">Inertia Mechanics</a>



<a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialvelocityx">InitialVelocityX</a>



<a href="/windows/desktop/wintouch/iinertiaprocessor-properties">Properties</a>
