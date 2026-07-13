---
UID: NF:manipulations.IInertiaProcessor.put_DesiredDisplacement
title: IInertiaProcessor::put_DesiredDisplacement (manipulations.h)
description: The DesiredDisplacement property specifies the desired distance that the object will travel. (Put)
helpviewer_keywords: ["DesiredDisplacement property [Windows Touch]","DesiredDisplacement property [Windows Touch]","IInertiaProcessor interface","IInertiaProcessor interface [Windows Touch]","DesiredDisplacement property","IInertiaProcessor.DesiredDisplacement","IInertiaProcessor.put_DesiredDisplacement","IInertiaProcessor::DesiredDisplacement","IInertiaProcessor::get_DesiredDisplacement","IInertiaProcessor::put_DesiredDisplacement","manipulations/IInertiaProcessor::DesiredDisplacement","manipulations/IInertiaProcessor::get_DesiredDisplacement","manipulations/IInertiaProcessor::put_DesiredDisplacement","put_DesiredDisplacement","wintouch.iinertiaprocessor_desireddisplacement"]
old-location: wintouch\iinertiaprocessor_desireddisplacement.htm
tech.root: wintouch
ms.assetid: cbcd7ce7-7df4-48d8-acfe-dc206f5d70d1
ms.date: 12/05/2018
ms.keywords: DesiredDisplacement property [Windows Touch], DesiredDisplacement property [Windows Touch],IInertiaProcessor interface, IInertiaProcessor interface [Windows Touch],DesiredDisplacement property, IInertiaProcessor.DesiredDisplacement, IInertiaProcessor.put_DesiredDisplacement, IInertiaProcessor::DesiredDisplacement, IInertiaProcessor::get_DesiredDisplacement, IInertiaProcessor::put_DesiredDisplacement, manipulations/IInertiaProcessor::DesiredDisplacement, manipulations/IInertiaProcessor::get_DesiredDisplacement, manipulations/IInertiaProcessor::put_DesiredDisplacement, put_DesiredDisplacement, wintouch.iinertiaprocessor_desireddisplacement
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
 - IInertiaProcessor::put_DesiredDisplacement
 - manipulations/IInertiaProcessor::put_DesiredDisplacement
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
 - IInertiaProcessor.DesiredDisplacement
 - IInertiaProcessor.get_DesiredDisplacement
 - IInertiaProcessor.put_DesiredDisplacement
---

# IInertiaProcessor::put_DesiredDisplacement


## -description

The <b>DesiredDisplacement</b> property specifies the desired distance that the object will travel.

This property is read/write.

## -parameters

## -remarks

<b>DesiredDisplacement</b> and <a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration">DesiredDeceleration</a> are mutually exclusive.  If one is set, the other should be NaN.

If inertia processing has already started, setting <b>DesiredDisplacement</b> will reset the inertia engine to the initial state with new deceleration value applied.
      

Call this function to set the initial state of inertia. You would call this function most likely during the <a href="/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted">ManipulationCompleted</a> event of the <a href="/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor">IManipulationProcessor</a> or in the constructor of the <a href="/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a> interface.

## -see-also

<a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration">DesiredDeceleration</a>



<a href="/windows/desktop/wintouch/handling-inertia-in-unmanaged-code">Handling Inertia in Unmanaged Code</a>



<a href="/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a>



<a href="/windows/desktop/wintouch/inertia-mechanics">Inertia Mechanics</a>



<a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialvelocityx">InitialVelocityX</a>



<a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialvelocityy">InitialVelocityY</a>



<a href="/windows/desktop/wintouch/iinertiaprocessor-properties">Properties</a>
