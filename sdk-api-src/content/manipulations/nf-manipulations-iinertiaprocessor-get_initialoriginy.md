---
UID: NF:manipulations.IInertiaProcessor.get_InitialOriginY
title: IInertiaProcessor::get_InitialOriginY (manipulations.h)
description: The InitialOriginY property specifies the starting vertical location for a target with inertia. (Get)
helpviewer_keywords: ["IInertiaProcessor interface [Windows Touch]","InitialOriginY property","IInertiaProcessor.InitialOriginY","IInertiaProcessor.get_InitialOriginY","IInertiaProcessor::InitialOriginY","IInertiaProcessor::get_InitialOriginY","IInertiaProcessor::put_InitialOriginY","InitialOriginY property [Windows Touch]","InitialOriginY property [Windows Touch]","IInertiaProcessor interface","get_InitialOriginY","manipulations/IInertiaProcessor::InitialOriginY","manipulations/IInertiaProcessor::get_InitialOriginY","manipulations/IInertiaProcessor::put_InitialOriginY","wintouch.iinertiaprocessor_initialoriginy"]
old-location: wintouch\iinertiaprocessor_initialoriginy.htm
tech.root: wintouch
ms.assetid: 4b817f8b-79e9-4409-a6b2-2096759bab59
ms.date: 12/05/2018
ms.keywords: IInertiaProcessor interface [Windows Touch],InitialOriginY property, IInertiaProcessor.InitialOriginY, IInertiaProcessor.get_InitialOriginY, IInertiaProcessor::InitialOriginY, IInertiaProcessor::get_InitialOriginY, IInertiaProcessor::put_InitialOriginY, InitialOriginY property [Windows Touch], InitialOriginY property [Windows Touch],IInertiaProcessor interface, get_InitialOriginY, manipulations/IInertiaProcessor::InitialOriginY, manipulations/IInertiaProcessor::get_InitialOriginY, manipulations/IInertiaProcessor::put_InitialOriginY, wintouch.iinertiaprocessor_initialoriginy
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
 - IInertiaProcessor::get_InitialOriginY
 - manipulations/IInertiaProcessor::get_InitialOriginY
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
 - IInertiaProcessor.InitialOriginY
 - IInertiaProcessor.get_InitialOriginY
 - IInertiaProcessor.put_InitialOriginY
---

# IInertiaProcessor::get_InitialOriginY


## -description

The <b>InitialOriginY</b> property specifies the starting vertical location for a target with inertia.

This property is read/write.

## -parameters

## -remarks

A user can manipulate an object to set the <b>InitialOriginY</b> to be outside of the elastic bounds.
	 Setting <b>InitialOriginY</b> to a value outside of the elastic bounds will cause an exception to be thrown.
	 To prevent  users from setting the origin out of bounds, check that <b>InitialOriginY</b> is valid before setting it 
	 on an <a href="/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a> interface.	 If Inertia processing has already started, calling put_InitialOriginY() 
	 will reset the inertia state to initial time stamp.
	 

All locations used for the inertia and manipulation processor are relative. If you want to use screen coordinates, 
		  you pass screen coordinates to the manipulation (or inertia) processor; if you want to use absolute coordinates, you 
		  pass those into the processor you are using. 	 
	 

Call this function to set the initial state of inertia. You would call this function most likely during the <a href="/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted">ManipulationCompleted</a> event of the <a href="/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor">IManipulationProcessor</a> or in the constructor of the <a href="/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a> interface.

## -see-also

<a href="/windows/desktop/wintouch/handling-inertia-in-unmanaged-code">Handling Inertia in Unmanaged Code</a>



<a href="/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a>



<a href="/windows/desktop/wintouch/inertia-mechanics">Inertia Mechanics</a>



<a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialoriginy">InitialOriginY</a>



<a href="/windows/desktop/wintouch/iinertiaprocessor-properties">Properties</a>
