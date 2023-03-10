---
UID: NF:manipulations.IInertiaProcessor.get_DesiredAngularDeceleration
title: IInertiaProcessor::get_DesiredAngularDeceleration (manipulations.h)
description: The DesiredAngularDeceleration property specifies the desired rate that the target object will stop spinning in radians per msec squared. (Get)
helpviewer_keywords: ["DesiredAngularDeceleration property [Windows Touch]","DesiredAngularDeceleration property [Windows Touch]","IInertiaProcessor interface","IInertiaProcessor interface [Windows Touch]","DesiredAngularDeceleration property","IInertiaProcessor.DesiredAngularDeceleration","IInertiaProcessor.get_DesiredAngularDeceleration","IInertiaProcessor::DesiredAngularDeceleration","IInertiaProcessor::get_DesiredAngularDeceleration","IInertiaProcessor::put_DesiredAngularDeceleration","get_DesiredAngularDeceleration","manipulations/IInertiaProcessor::DesiredAngularDeceleration","manipulations/IInertiaProcessor::get_DesiredAngularDeceleration","manipulations/IInertiaProcessor::put_DesiredAngularDeceleration","wintouch.iinertiaprocessor_desiredangulardeceleration"]
old-location: wintouch\iinertiaprocessor_desiredangulardeceleration.htm
tech.root: wintouch
ms.assetid: ee3bb3c8-4d7d-424b-abc9-db7307793794
ms.date: 12/05/2018
ms.keywords: DesiredAngularDeceleration property [Windows Touch], DesiredAngularDeceleration property [Windows Touch],IInertiaProcessor interface, IInertiaProcessor interface [Windows Touch],DesiredAngularDeceleration property, IInertiaProcessor.DesiredAngularDeceleration, IInertiaProcessor.get_DesiredAngularDeceleration, IInertiaProcessor::DesiredAngularDeceleration, IInertiaProcessor::get_DesiredAngularDeceleration, IInertiaProcessor::put_DesiredAngularDeceleration, get_DesiredAngularDeceleration, manipulations/IInertiaProcessor::DesiredAngularDeceleration, manipulations/IInertiaProcessor::get_DesiredAngularDeceleration, manipulations/IInertiaProcessor::put_DesiredAngularDeceleration, wintouch.iinertiaprocessor_desiredangulardeceleration
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
 - IInertiaProcessor::get_DesiredAngularDeceleration
 - manipulations/IInertiaProcessor::get_DesiredAngularDeceleration
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
 - IInertiaProcessor.DesiredAngularDeceleration
 - IInertiaProcessor.get_DesiredAngularDeceleration
 - IInertiaProcessor.put_DesiredAngularDeceleration
---

# IInertiaProcessor::get_DesiredAngularDeceleration


## -description

The <b>DesiredAngularDeceleration</b> property specifies the desired rate that the target object will stop spinning in radians per  msec squared.

This property is read/write.

## -parameters

## -remarks

<b>DesiredAngularDeceleration</b> and <a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredrotation">DesiredRotation</a> are mutually exclusive.  If one is set, the other should be NaN.
		

If inertia processing has already started, setting <b>DesiredAngularDeceleration</b> will reset the inertia engine to the initial state with new deceleration value applied.
      

Call this function to set the initial state of inertia. You would call this function most likely during the <a href="/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted">ManipulationCompleted</a> event of the <a href="/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor">IManipulationProcessor</a> or in the constructor of the <a href="/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a> interface.

## -see-also

<a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredrotation">DesiredRotation</a>



<a href="/windows/desktop/wintouch/handling-inertia-in-unmanaged-code">Handling Inertia in Unmanaged Code</a>



<a href="/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a>



<a href="/windows/desktop/wintouch/inertia-mechanics">Inertia Mechanics</a>



<a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialangularvelocity">InitialAngularVelocity</a>



<a href="/windows/desktop/wintouch/iinertiaprocessor-properties">Properties</a>
