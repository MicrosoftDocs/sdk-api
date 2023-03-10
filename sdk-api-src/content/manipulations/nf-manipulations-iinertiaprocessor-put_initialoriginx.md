---
UID: NF:manipulations.IInertiaProcessor.put_InitialOriginX
title: IInertiaProcessor::put_InitialOriginX (manipulations.h)
description: The InitialOriginX property specifies the starting horizontal location for a target with inertia. (Put)
helpviewer_keywords: ["IInertiaProcessor interface [Windows Touch]","InitialOriginX property","IInertiaProcessor.InitialOriginX","IInertiaProcessor.put_InitialOriginX","IInertiaProcessor::InitialOriginX","IInertiaProcessor::get_InitialOriginX","IInertiaProcessor::put_InitialOriginX","InitialOriginX property [Windows Touch]","InitialOriginX property [Windows Touch]","IInertiaProcessor interface","manipulations/IInertiaProcessor::InitialOriginX","manipulations/IInertiaProcessor::get_InitialOriginX","manipulations/IInertiaProcessor::put_InitialOriginX","put_InitialOriginX","wintouch.iinertiaprocessor_initialoriginx"]
old-location: wintouch\iinertiaprocessor_initialoriginx.htm
tech.root: wintouch
ms.assetid: 6c710bd7-6fbe-4bc3-8966-b83d4500625a
ms.date: 12/05/2018
ms.keywords: IInertiaProcessor interface [Windows Touch],InitialOriginX property, IInertiaProcessor.InitialOriginX, IInertiaProcessor.put_InitialOriginX, IInertiaProcessor::InitialOriginX, IInertiaProcessor::get_InitialOriginX, IInertiaProcessor::put_InitialOriginX, InitialOriginX property [Windows Touch], InitialOriginX property [Windows Touch],IInertiaProcessor interface, manipulations/IInertiaProcessor::InitialOriginX, manipulations/IInertiaProcessor::get_InitialOriginX, manipulations/IInertiaProcessor::put_InitialOriginX, put_InitialOriginX, wintouch.iinertiaprocessor_initialoriginx
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
 - IInertiaProcessor::put_InitialOriginX
 - manipulations/IInertiaProcessor::put_InitialOriginX
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
 - IInertiaProcessor.InitialOriginX
 - IInertiaProcessor.get_InitialOriginX
 - IInertiaProcessor.put_InitialOriginX
---

# IInertiaProcessor::put_InitialOriginX


## -description

The <b>InitialOriginX</b> property specifies the starting horizontal location for a target with inertia.

This property is read/write.

## -parameters

## -remarks

A user can manipulate an object to set the <b>InitialOriginX</b> to be outside of the elastic bounds.
	 Setting <b>InitialOriginX</b> to a value outside of the elastic bounds will cause an exception to be thrown.
	 To prevent  users from setting the origin out of bounds, check that <b>InitialOriginX</b> is valid before 
	 setting it on an <a href="/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a> interface. If Inertia processing has already started, calling put_InitialOriginX()
	 will reset the inertia state to initial time stamp.
	 

All locations used for the inertia and manipulation processor are relative. If you want to use screen coordinates,
	      you pass screen coordinates to the manipulation (or inertia) processor; if you want to use absolute coordinates, 
			you pass those into the processor you are using. 

Call this function to set the initial state of inertia. You would call this function most likely during the <a href="/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted">ManipulationCompleted</a> event of the <a href="/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor">IManipulationProcessor</a> or in the constructor of the <a href="/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a> interface.

## -see-also

<a href="/windows/desktop/wintouch/handling-inertia-in-unmanaged-code">Handling Inertia in Unmanaged Code</a>



<a href="/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor">IInertiaProcessor</a>



<a href="/windows/desktop/wintouch/inertia-mechanics">Inertia Mechanics</a>



<a href="/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialoriginy">InitialOriginY</a>



<a href="/windows/desktop/wintouch/iinertiaprocessor-properties">Properties</a>
