---
UID: NF:manipulations.IInertiaProcessor.put_InitialExpansionVelocity
title: IInertiaProcessor::put_InitialExpansionVelocity (manipulations.h)
description: The InitialExpansionVelocity property specifies the rate of radius expansion for a target when the target was affected by inertia. (Put)
helpviewer_keywords: ["IInertiaProcessor interface [Windows Touch]","InitialExpansionVelocity property","IInertiaProcessor.InitialExpansionVelocity","IInertiaProcessor.put_InitialExpansionVelocity","IInertiaProcessor::InitialExpansionVelocity","IInertiaProcessor::get_InitialExpansionVelocity","IInertiaProcessor::put_InitialExpansionVelocity","InitialExpansionVelocity property [Windows Touch]","InitialExpansionVelocity property [Windows Touch]","IInertiaProcessor interface","manipulations/IInertiaProcessor::InitialExpansionVelocity","manipulations/IInertiaProcessor::get_InitialExpansionVelocity","manipulations/IInertiaProcessor::put_InitialExpansionVelocity","put_InitialExpansionVelocity","wintouch.iinertiaprocessor_initialexpansionvelocity"]
old-location: wintouch\iinertiaprocessor_initialexpansionvelocity.htm
tech.root: wintouch
ms.assetid: c0e60b1c-98d0-4b50-ba5d-deda44debf56
ms.date: 12/05/2018
ms.keywords: IInertiaProcessor interface [Windows Touch],InitialExpansionVelocity property, IInertiaProcessor.InitialExpansionVelocity, IInertiaProcessor.put_InitialExpansionVelocity, IInertiaProcessor::InitialExpansionVelocity, IInertiaProcessor::get_InitialExpansionVelocity, IInertiaProcessor::put_InitialExpansionVelocity, InitialExpansionVelocity property [Windows Touch], InitialExpansionVelocity property [Windows Touch],IInertiaProcessor interface, manipulations/IInertiaProcessor::InitialExpansionVelocity, manipulations/IInertiaProcessor::get_InitialExpansionVelocity, manipulations/IInertiaProcessor::put_InitialExpansionVelocity, put_InitialExpansionVelocity, wintouch.iinertiaprocessor_initialexpansionvelocity
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
 - IInertiaProcessor::put_InitialExpansionVelocity
 - manipulations/IInertiaProcessor::put_InitialExpansionVelocity
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
 - IInertiaProcessor.InitialExpansionVelocity
 - IInertiaProcessor.get_InitialExpansionVelocity
 - IInertiaProcessor.put_InitialExpansionVelocity
---

# IInertiaProcessor::put_InitialExpansionVelocity


## -description

The <b>InitialExpansionVelocity</b> property specifies the rate of radius expansion for a target when the target was affected by inertia.

This property is read/write.

## -parameters

## -remarks

The amount of expansion that the <a href="/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a> extrapolates will be determined by the <a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredexpansion">DesiredExpansion</a> or <a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredexpansiondeceleration">DesiredExpansionDeceleration</a> property.
      <b>DesiredExpansion</b> and <b>DesiredExpansionDeceleration</b> are mutually exclusive.  If one is set, the other should be NaN.
    If using the <b>DesiredExpansion</b> property, the API will set the appropriate <b>DesiredExpansionDeceleration</b> value to expand the requested amount.

If inertia processing has already started, setting <b>InitialExpansionVelocity</b> will reset the inertia engine to the initial state with new velocity values applied.

Call this function to set the initial state of inertia. You would call this function most likely during the <a href="/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted">ManipulationCompleted</a> event of the <a href="/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor">IManipulationProcessor</a> or in the constructor of the <a href="/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a> interface.

## -see-also

<a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredexpansion">DesiredExpansion</a>



<a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredexpansiondeceleration">DesiredExpansionDeceleration</a>



<a href="/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getexpansionvelocity">GetExpansionVelocity</a>



<a href="/windows/desktop/wintouch/handling-inertia-in-unmanaged-code">Handling Inertia in Unmanaged Code</a>



<a href="/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a>



<a href="/windows/desktop/wintouch/inertia-mechanics">Inertia Mechanics</a>



<a href="/windows/desktop/wintouch/iinertiaprocessor-properties">Properties</a>
