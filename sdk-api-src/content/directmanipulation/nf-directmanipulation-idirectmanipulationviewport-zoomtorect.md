---
UID: NF:directmanipulation.IDirectManipulationViewport.ZoomToRect
title: IDirectManipulationViewport::ZoomToRect
author: windows-sdk-content
description: Moves the viewport to a specific area of the primary content and specifies whether to animate the transition.
old-location: directmanipulation\idirectmanipulationviewport_zoomtorect.htm
old-project: directmanipulation
ms.assetid: ce87521d-bbce-43d3-920b-89eca101d260
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IDirectManipulationViewport interface [Direct Manipulation],ZoomToRect method, IDirectManipulationViewport.ZoomToRect, IDirectManipulationViewport::ZoomToRect, ZoomToRect, ZoomToRect method [Direct Manipulation], ZoomToRect method [Direct Manipulation],IDirectManipulationViewport interface, directmanipulation.idirectmanipulationviewport_zoomtorect, directmanipulation/IDirectManipulationViewport::ZoomToRect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DIRECTMANIPULATION_VIEWPORT_OPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationViewport.ZoomToRect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationViewport::ZoomToRect


## -description


Moves the viewport to a specific area of the primary content and specifies whether to animate the transition.


## -parameters




### -param left [in]

The leftmost coordinate of the rectangle in the primary content coordinate space.


### -param top [in]

The topmost coordinate of the rectangle in the primary content coordinate space.


### -param right [in]

The rightmost coordinate of the rectangle in the primary content coordinate space.


### -param bottom [in]

The bottommost coordinate of the rectangle in the primary content coordinate space.


### -param animate [in]

Specifies whether to animate the zoom behavior.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4c14143b-3b5f-401d-9df7-f17374abcd99">IDirectManipulationViewport</a>
 

 

