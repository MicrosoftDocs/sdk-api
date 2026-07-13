---
UID: NF:manipulations.IInertiaProcessor.get_DesiredDeceleration
title: IInertiaProcessor::get_DesiredDeceleration (manipulations.h)
description: The DesiredDeceleration property specifies the desired rate at which translation operations will decelerate. (Get)
helpviewer_keywords: ["DesiredDeceleration property [Windows Touch]","DesiredDeceleration property [Windows Touch]","IInertiaProcessor interface","IInertiaProcessor interface [Windows Touch]","DesiredDeceleration property","IInertiaProcessor.DesiredDeceleration","IInertiaProcessor.get_DesiredDeceleration","IInertiaProcessor::DesiredDeceleration","IInertiaProcessor::get_DesiredDeceleration","IInertiaProcessor::put_DesiredDeceleration","get_DesiredDeceleration","manipulations/IInertiaProcessor::DesiredDeceleration","manipulations/IInertiaProcessor::get_DesiredDeceleration","manipulations/IInertiaProcessor::put_DesiredDeceleration","wintouch.iinertiaprocessor_desireddeceleration"]
old-location: wintouch\iinertiaprocessor_desireddeceleration.htm
tech.root: wintouch
ms.assetid: 2ad39e7e-b433-4a40-aea2-53cf23247f25
ms.date: 12/05/2018
ms.keywords: DesiredDeceleration property [Windows Touch], DesiredDeceleration property [Windows Touch],IInertiaProcessor interface, IInertiaProcessor interface [Windows Touch],DesiredDeceleration property, IInertiaProcessor.DesiredDeceleration, IInertiaProcessor.get_DesiredDeceleration, IInertiaProcessor::DesiredDeceleration, IInertiaProcessor::get_DesiredDeceleration, IInertiaProcessor::put_DesiredDeceleration, get_DesiredDeceleration, manipulations/IInertiaProcessor::DesiredDeceleration, manipulations/IInertiaProcessor::get_DesiredDeceleration, manipulations/IInertiaProcessor::put_DesiredDeceleration, wintouch.iinertiaprocessor_desireddeceleration
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
 - IInertiaProcessor::get_DesiredDeceleration
 - manipulations/IInertiaProcessor::get_DesiredDeceleration
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
 - IInertiaProcessor.DesiredDeceleration
 - IInertiaProcessor.get_DesiredDeceleration
 - IInertiaProcessor.put_DesiredDeceleration
---

# IInertiaProcessor::get_DesiredDeceleration


## -description

The <b>DesiredDeceleration</b> property specifies the desired rate at which translation operations will decelerate.

This property is read/write.

## -parameters

## -remarks

<b>DesiredDeceleration</b> and <a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddisplacement">DesiredDisplacement</a> are mutually exclusive.  If one is set, the other should be NaN.

If inertia processing has already started, setting <b>DesiredDeceleration</b> will reset the inertia engine to the initial state with new deceleration value applied.
      

Call this function to set the initial state of inertia. You would call this function most likely during the <a href="/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted">ManipulationCompleted</a> event of the <a href="/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor">IManipulationProcessor</a> or in the constructor of the <a href="/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a> interface.

## -see-also

<a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddisplacement">DesiredDisplacement</a>



<a href="/windows/desktop/wintouch/handling-inertia-in-unmanaged-code">Handling Inertia in Unmanaged Code</a>



<a href="/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a>



<a href="/windows/desktop/wintouch/inertia-mechanics">Inertia Mechanics</a>



<a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialvelocityx">InitialVelocityX</a>



<a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialvelocityy">InitialVelocityY</a>



<a href="/windows/desktop/wintouch/iinertiaprocessor-properties">Properties</a>
