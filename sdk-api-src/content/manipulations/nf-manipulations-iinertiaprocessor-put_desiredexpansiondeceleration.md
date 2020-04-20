---
UID: NF:manipulations.IInertiaProcessor.put_DesiredExpansionDeceleration
title: IInertiaProcessor::put_DesiredExpansionDeceleration (manipulations.h)
description: The DesiredExpansionDeceleration property specifies the rate at which the object will stop expanding.helpviewer_keywords: ["DesiredExpansionDeceleration property [Windows Touch]","DesiredExpansionDeceleration property [Windows Touch]","IInertiaProcessor interface","IInertiaProcessor interface [Windows Touch]","DesiredExpansionDeceleration property","IInertiaProcessor.DesiredExpansionDeceleration","IInertiaProcessor.put_DesiredExpansionDeceleration","IInertiaProcessor::DesiredExpansionDeceleration","IInertiaProcessor::get_DesiredExpansionDeceleration","IInertiaProcessor::put_DesiredExpansionDeceleration","manipulations/IInertiaProcessor::DesiredExpansionDeceleration","manipulations/IInertiaProcessor::get_DesiredExpansionDeceleration","manipulations/IInertiaProcessor::put_DesiredExpansionDeceleration","put_DesiredExpansionDeceleration","wintouch.iinertiaprocessor_desiredexpansiondeceleration"]
old-location: wintouch\iinertiaprocessor_desiredexpansiondeceleration.htm
tech.root: wintouch
ms.assetid: b21d9aa8-0c86-45fe-9573-023929cf7faa
ms.date: 12/05/2018
ms.keywords: DesiredExpansionDeceleration property [Windows Touch], DesiredExpansionDeceleration property [Windows Touch],IInertiaProcessor interface, IInertiaProcessor interface [Windows Touch],DesiredExpansionDeceleration property, IInertiaProcessor.DesiredExpansionDeceleration, IInertiaProcessor.put_DesiredExpansionDeceleration, IInertiaProcessor::DesiredExpansionDeceleration, IInertiaProcessor::get_DesiredExpansionDeceleration, IInertiaProcessor::put_DesiredExpansionDeceleration, manipulations/IInertiaProcessor::DesiredExpansionDeceleration, manipulations/IInertiaProcessor::get_DesiredExpansionDeceleration, manipulations/IInertiaProcessor::put_DesiredExpansionDeceleration, put_DesiredExpansionDeceleration, wintouch.iinertiaprocessor_desiredexpansiondeceleration
f1_keywords:
- manipulations/IInertiaProcessor.DesiredExpansionDeceleration
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- manipulations.h
api_name:
- IInertiaProcessor.DesiredExpansionDeceleration
- IInertiaProcessor.get_DesiredExpansionDeceleration
- IInertiaProcessor.put_DesiredExpansionDeceleration
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInertiaProcessor::put_DesiredExpansionDeceleration


## -description


The <b>DesiredExpansionDeceleration</b> property specifies the rate at which the object will stop expanding.

This property is read/write.


## -parameters


## -remarks



<b>DesiredExpansionDeceleration</b> and <a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredexpansion">DesiredExpansion</a> are mutually exclusive.  If one is set, the other should be NaN.

If inertia processing has already started, setting <b>DesiredExpansionDeceleration</b> will reset the inertia engine to the initial state with new deceleration value applied.
      

Call this function to set the initial state of inertia. You would call this function most likely during the <a href="https://docs.microsoft.com/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted">ManipulationCompleted</a> event of the <a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor">IManipulationProcessor</a> or in the constructor of the <a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a> interface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredexpansion">DesiredExpansion</a>



<a href="https://docs.microsoft.com/windows/desktop/wintouch/handling-inertia-in-unmanaged-code">Handling Inertia in Unmanaged Code</a>



<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a>



<a href="https://docs.microsoft.com/windows/desktop/wintouch/inertia-mechanics">Inertia Mechanics</a>



<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialexpansionvelocity">InitialExpansionVelocity</a>



<a href="https://docs.microsoft.com/windows/desktop/wintouch/iinertiaprocessor-properties">Properties</a>
 

 

