---
UID: NF:manipulations.IInertiaProcessor.put_DesiredExpansion
title: IInertiaProcessor::put_DesiredExpansion (manipulations.h)
description: The DesiredExpansion property specifies the desired change in the object's average radius. (Put)
helpviewer_keywords: ["DesiredExpansion property [Windows Touch]","DesiredExpansion property [Windows Touch]","IInertiaProcessor interface","IInertiaProcessor interface [Windows Touch]","DesiredExpansion property","IInertiaProcessor.DesiredExpansion","IInertiaProcessor.put_DesiredExpansion","IInertiaProcessor::DesiredExpansion","IInertiaProcessor::get_DesiredExpansion","IInertiaProcessor::put_DesiredExpansion","manipulations/IInertiaProcessor::DesiredExpansion","manipulations/IInertiaProcessor::get_DesiredExpansion","manipulations/IInertiaProcessor::put_DesiredExpansion","put_DesiredExpansion","wintouch.iinertiaprocessor_desiredexpansion"]
old-location: wintouch\iinertiaprocessor_desiredexpansion.htm
tech.root: wintouch
ms.assetid: 1d686bb1-a00b-43fc-804b-5a1d8bb69499
ms.date: 12/05/2018
ms.keywords: DesiredExpansion property [Windows Touch], DesiredExpansion property [Windows Touch],IInertiaProcessor interface, IInertiaProcessor interface [Windows Touch],DesiredExpansion property, IInertiaProcessor.DesiredExpansion, IInertiaProcessor.put_DesiredExpansion, IInertiaProcessor::DesiredExpansion, IInertiaProcessor::get_DesiredExpansion, IInertiaProcessor::put_DesiredExpansion, manipulations/IInertiaProcessor::DesiredExpansion, manipulations/IInertiaProcessor::get_DesiredExpansion, manipulations/IInertiaProcessor::put_DesiredExpansion, put_DesiredExpansion, wintouch.iinertiaprocessor_desiredexpansion
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
 - IInertiaProcessor::put_DesiredExpansion
 - manipulations/IInertiaProcessor::put_DesiredExpansion
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
 - IInertiaProcessor.DesiredExpansion
 - IInertiaProcessor.get_DesiredExpansion
 - IInertiaProcessor.put_DesiredExpansion
---

# IInertiaProcessor::put_DesiredExpansion


## -description

The <b>DesiredExpansion</b> property specifies the desired change in the object's average radius.

This property is read/write.

## -parameters

## -remarks

<b>DesiredExpansion</b> and <a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredexpansiondeceleration">DesiredExpansionDeceleration</a> are mutually exclusive.  If one is set, the other should be NaN.

If inertia processing has already started, setting <b>DesiredExpansion</b> will reset the inertia engine to the initial state with new deceleration value applied.
      

Call this function to set the initial state of inertia. You would call this function most likely during the <a href="/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted">ManipulationCompleted</a> event of the <a href="/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor">IManipulationProcessor</a> or in the constructor of the <a href="/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a> interface.

## -see-also

<a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredexpansiondeceleration">DesiredExpansionDeceleration</a>



<a href="/windows/desktop/wintouch/handling-inertia-in-unmanaged-code">Handling Inertia in Unmanaged Code</a>



<a href="/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a>



<a href="/windows/desktop/wintouch/inertia-mechanics">Inertia Mechanics</a>



<a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialexpansionvelocity">InitialExpansionVelocity</a>



<a href="/windows/desktop/wintouch/iinertiaprocessor-properties">Properties</a>
