---
UID: NF:manipulations.IInertiaProcessor.put_DesiredRotation
title: IInertiaProcessor::put_DesiredRotation (manipulations.h)
description: The DesiredRotation property specifies how far the current inertia processor object should manipulate the target object in radians. (Put)
helpviewer_keywords: ["DesiredRotation property [Windows Touch]","DesiredRotation property [Windows Touch]","IInertiaProcessor interface","IInertiaProcessor interface [Windows Touch]","DesiredRotation property","IInertiaProcessor.DesiredRotation","IInertiaProcessor.put_DesiredRotation","IInertiaProcessor::DesiredRotation","IInertiaProcessor::get_DesiredRotation","IInertiaProcessor::put_DesiredRotation","manipulations/IInertiaProcessor::DesiredRotation","manipulations/IInertiaProcessor::get_DesiredRotation","manipulations/IInertiaProcessor::put_DesiredRotation","put_DesiredRotation","wintouch.iinertiaprocessor_desiredrotation"]
old-location: wintouch\iinertiaprocessor_desiredrotation.htm
tech.root: wintouch
ms.assetid: 42fcda66-8992-4a44-b4d5-04d4f2c7e25a
ms.date: 12/05/2018
ms.keywords: DesiredRotation property [Windows Touch], DesiredRotation property [Windows Touch],IInertiaProcessor interface, IInertiaProcessor interface [Windows Touch],DesiredRotation property, IInertiaProcessor.DesiredRotation, IInertiaProcessor.put_DesiredRotation, IInertiaProcessor::DesiredRotation, IInertiaProcessor::get_DesiredRotation, IInertiaProcessor::put_DesiredRotation, manipulations/IInertiaProcessor::DesiredRotation, manipulations/IInertiaProcessor::get_DesiredRotation, manipulations/IInertiaProcessor::put_DesiredRotation, put_DesiredRotation, wintouch.iinertiaprocessor_desiredrotation
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
 - IInertiaProcessor::put_DesiredRotation
 - manipulations/IInertiaProcessor::put_DesiredRotation
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
 - IInertiaProcessor.DesiredRotation
 - IInertiaProcessor.get_DesiredRotation
 - IInertiaProcessor.put_DesiredRotation
---

# IInertiaProcessor::put_DesiredRotation


## -description

The DesiredRotation property specifies how far the current inertia processor object should manipulate the target object in radians.

This property is read/write.

## -parameters

## -remarks

<b>DesiredRotation</b> and <a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration">DesiredAngularDeceleration</a> are mutually exclusive.  If one is set, the other should be NaN.

If inertia processing has already started, setting <b>DesiredRotation</b> will reset the inertia engine to the initial state with new deceleration value applied.
      

Call this function to set the initial state of inertia. You would call this function most likely during the <a href="/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted">ManipulationCompleted</a> event of the <a href="/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor">IManipulationProcessor</a> or in the constructor of the <a href="/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a> interface.

## -see-also

<a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration">DesiredAngularDeceleration</a>



<a href="/windows/desktop/wintouch/handling-inertia-in-unmanaged-code">Handling Inertia in Unmanaged Code</a>



<a href="/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a>



<a href="/windows/desktop/wintouch/inertia-mechanics">Inertia Mechanics</a>



<a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialangularvelocity">InitialAngularVelocity</a>



<a href="/windows/desktop/wintouch/iinertiaprocessor-properties">Properties</a>
