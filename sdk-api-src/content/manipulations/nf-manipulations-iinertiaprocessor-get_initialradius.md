---
UID: NF:manipulations.IInertiaProcessor.get_InitialRadius
title: IInertiaProcessor::get_InitialRadius (manipulations.h)
description: The InitialRadius property specifies the distance from the edge of the target to its center before the object was changed.
helpviewer_keywords: ["IInertiaProcessor interface [Windows Touch]","InitialRadius property","IInertiaProcessor.InitialRadius","IInertiaProcessor.get_InitialRadius","IInertiaProcessor::InitialRadius","IInertiaProcessor::get_InitialRadius","IInertiaProcessor::put_InitialRadius","InitialRadius property [Windows Touch]","InitialRadius property [Windows Touch]","IInertiaProcessor interface","get_InitialRadius","manipulations/IInertiaProcessor::InitialRadius","manipulations/IInertiaProcessor::get_InitialRadius","manipulations/IInertiaProcessor::put_InitialRadius","wintouch.iinertiaprocessor_initialradius"]
old-location: wintouch\iinertiaprocessor_initialradius.htm
tech.root: wintouch
ms.assetid: 53179559-e65a-4b5b-b82a-f1fea0cb4509
ms.date: 12/05/2018
ms.keywords: IInertiaProcessor interface [Windows Touch],InitialRadius property, IInertiaProcessor.InitialRadius, IInertiaProcessor.get_InitialRadius, IInertiaProcessor::InitialRadius, IInertiaProcessor::get_InitialRadius, IInertiaProcessor::put_InitialRadius, InitialRadius property [Windows Touch], InitialRadius property [Windows Touch],IInertiaProcessor interface, get_InitialRadius, manipulations/IInertiaProcessor::InitialRadius, manipulations/IInertiaProcessor::get_InitialRadius, manipulations/IInertiaProcessor::put_InitialRadius, wintouch.iinertiaprocessor_initialradius
f1_keywords:
- manipulations/IInertiaProcessor.InitialRadius
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
- IInertiaProcessor.InitialRadius
- IInertiaProcessor.get_InitialRadius
- IInertiaProcessor.put_InitialRadius
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInertiaProcessor::get_InitialRadius


## -description


The <b>InitialRadius</b> property specifies the distance from the edge of the target to its center before the object was changed.

This property is read/write.


## -parameters


## -remarks



If Inertia processing has already started, setting <b>InitialRadius</b> will reset the inertia engine to the initial state with new radius value applied.
	 

Call this function to set initial state of inertia. You would call this function most likely during the <a href="/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted">ManipulationCompleted</a> event of the <a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor">IManipulationProcessor</a>, or in the constructor of the <a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a> interface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wintouch/handling-inertia-in-unmanaged-code">Handling Inertia in Unmanaged Code</a>



<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a>



<a href="https://docs.microsoft.com/windows/desktop/wintouch/inertia-mechanics">Inertia Mechanics</a>



<a href="https://docs.microsoft.com/windows/desktop/wintouch/iinertiaprocessor-properties">Properties</a>
 

 

