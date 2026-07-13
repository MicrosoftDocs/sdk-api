---
UID: NF:manipulations.IInertiaProcessor.put_InitialAngularVelocity
title: IInertiaProcessor::put_InitialAngularVelocity (manipulations.h)
description: The InitialAngularVelocity property specifies the rotational (angular) velocity of the target when movement begins. (Put)
helpviewer_keywords: ["IInertiaProcessor interface [Windows Touch]","InitialAngularVelocity property","IInertiaProcessor.InitialAngularVelocity","IInertiaProcessor.put_InitialAngularVelocity","IInertiaProcessor::InitialAngularVelocity","IInertiaProcessor::get_InitialAngularVelocity","IInertiaProcessor::put_InitialAngularVelocity","InitialAngularVelocity property [Windows Touch]","InitialAngularVelocity property [Windows Touch]","IInertiaProcessor interface","manipulations/IInertiaProcessor::InitialAngularVelocity","manipulations/IInertiaProcessor::get_InitialAngularVelocity","manipulations/IInertiaProcessor::put_InitialAngularVelocity","put_InitialAngularVelocity","wintouch.iinertiaprocessor_initialangularvelocity"]
old-location: wintouch\iinertiaprocessor_initialangularvelocity.htm
tech.root: wintouch
ms.assetid: a15ac600-ef03-4234-ac38-dc3cf212a3cb
ms.date: 12/05/2018
ms.keywords: IInertiaProcessor interface [Windows Touch],InitialAngularVelocity property, IInertiaProcessor.InitialAngularVelocity, IInertiaProcessor.put_InitialAngularVelocity, IInertiaProcessor::InitialAngularVelocity, IInertiaProcessor::get_InitialAngularVelocity, IInertiaProcessor::put_InitialAngularVelocity, InitialAngularVelocity property [Windows Touch], InitialAngularVelocity property [Windows Touch],IInertiaProcessor interface, manipulations/IInertiaProcessor::InitialAngularVelocity, manipulations/IInertiaProcessor::get_InitialAngularVelocity, manipulations/IInertiaProcessor::put_InitialAngularVelocity, put_InitialAngularVelocity, wintouch.iinertiaprocessor_initialangularvelocity
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
 - IInertiaProcessor::put_InitialAngularVelocity
 - manipulations/IInertiaProcessor::put_InitialAngularVelocity
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
 - IInertiaProcessor.InitialAngularVelocity
 - IInertiaProcessor.get_InitialAngularVelocity
 - IInertiaProcessor.put_InitialAngularVelocity
---

# IInertiaProcessor::put_InitialAngularVelocity


## -description

The <b>InitialAngularVelocity</b> property specifies the rotational (angular) velocity of the target when movement begins.

This property is read/write.

## -parameters

## -remarks

<a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredrotation">DesiredRotation</a> and <a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration">DesiredAngularDeceleration</a> are mutually exclusive.  If one is set, the other should be NaN.  If the <b>DesiredRotation</b> property is set, the API will set the <b>DesiredAngularDeceleration</b> property so that the object will stop after the desired number of radians.
       The unit of angular acceleration is radians.
      

If inertia processing has already started, setting <b>InitialAngularVelocity</b> will reset the inertia engine to the initial state with new velocity values applied.
		

Call this function to set the initial state of inertia. You would call this function most likely during the <a href="/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted">ManipulationCompleted</a> event of the <a href="/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor">IManipulationProcessor</a> or in the constructor of the <a href="/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a> interface.

## -see-also

<a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredrotation">DesiredRotation</a>



<a href="/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getangularvelocity">GetAngularVelocity</a>



<a href="/windows/desktop/wintouch/handling-inertia-in-unmanaged-code">Handling Inertia in Unmanaged Code</a>



<a href="/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a>



<a href="/windows/desktop/wintouch/inertia-mechanics">Inertia Mechanics</a>



<a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialexpansionvelocity">InitialExpansionVelocity</a>



<a href="/windows/desktop/wintouch/iinertiaprocessor-properties">Properties</a>
