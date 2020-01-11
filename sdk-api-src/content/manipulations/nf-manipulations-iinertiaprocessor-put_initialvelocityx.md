---
UID: NF:manipulations.IInertiaProcessor.put_InitialVelocityX
title: IInertiaProcessor::put_InitialVelocityX (manipulations.h)
description: The InitialVelocityX property specifies the initial movement of the target object on the horizontal axis.
old-location: wintouch\iinertiaprocessor_initialvelocityx.htm
tech.root: wintouch
ms.assetid: 23ae7083-0a78-4628-8a04-f9bd762aac02
ms.date: 12/05/2018
ms.keywords: IInertiaProcessor interface [Windows Touch],InitialVelocityX property, IInertiaProcessor.InitialVelocityX, IInertiaProcessor.put_InitialVelocityX, IInertiaProcessor::InitialVelocityX, IInertiaProcessor::get_InitialVelocityX, IInertiaProcessor::put_InitialVelocityX, InitialVelocityX property [Windows Touch], InitialVelocityX property [Windows Touch],IInertiaProcessor interface, manipulations/IInertiaProcessor::InitialVelocityX, manipulations/IInertiaProcessor::get_InitialVelocityX, manipulations/IInertiaProcessor::put_InitialVelocityX, put_InitialVelocityX, wintouch.iinertiaprocessor_initialvelocityx
f1_keywords:
- manipulations/IInertiaProcessor.InitialVelocityX
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
- IInertiaProcessor.InitialVelocityX
- IInertiaProcessor.get_InitialVelocityX
- IInertiaProcessor.put_InitialVelocityX
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInertiaProcessor::put_InitialVelocityX


## -description


The <b>InitialVelocityX</b> property specifies the initial movement of the target object on the horizontal axis.

This property is read/write.


## -parameters


## -remarks



If Inertia processing has already started, setting <b>InitialVelocityX</b> will reset the inertia engine to the initial state with new velocity values applied.	 		
	 

Call this function to set the initial state of inertia. You would call this function most likely during the <a href="https://docs.microsoft.com/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted">ManipulationCompleted</a> event of the <a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor">IManipulationProcessor</a> or in the constructor of the <a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a> interface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getvelocityx">GetVelocityX</a>



<a href="https://docs.microsoft.com/windows/desktop/wintouch/handling-inertia-in-unmanaged-code">Handling Inertia in Unmanaged Code</a>



<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a>



<a href="https://docs.microsoft.com/windows/desktop/wintouch/inertia-mechanics">Inertia Mechanics</a>



<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialvelocityy">InitialVelocityY</a>



<a href="https://docs.microsoft.com/windows/desktop/wintouch/iinertiaprocessor-properties">Properties</a>
 

 

