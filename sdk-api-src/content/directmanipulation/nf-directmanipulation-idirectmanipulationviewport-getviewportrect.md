---
UID: NF:directmanipulation.IDirectManipulationViewport.GetViewportRect
title: IDirectManipulationViewport::GetViewportRect
author: windows-sdk-content
description: Retrieves the rectangle for the viewport relative to the origin of the viewport coordinate system specified by SetViewportRect.
old-location: directmanipulation\idirectmanipulationviewport_getviewportrect.htm
tech.root: directmanipulation
ms.assetid: 0d20e7f7-aa2a-4c76-a3ff-da10d4dec3ea
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetViewportRect, GetViewportRect method [Direct Manipulation], GetViewportRect method [Direct Manipulation],IDirectManipulationViewport interface, IDirectManipulationViewport interface [Direct Manipulation],GetViewportRect method, IDirectManipulationViewport.GetViewportRect, IDirectManipulationViewport::GetViewportRect, directmanipulation.idirectmanipulationviewport_getviewportrect, directmanipulation/IDirectManipulationViewport::GetViewportRect
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationViewport.GetViewportRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectManipulationViewport::GetViewportRect


## -description


Retrieves the rectangle for the viewport relative to the origin of the viewport coordinate system specified by <a href="https://msdn.microsoft.com/45dfdf6e-aa4d-489a-bf9a-016e42eb57f6">SetViewportRect</a>.


## -parameters




### -param viewport [out, retval]

The bounding rectangle relative to the viewport coordinate system.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4c14143b-3b5f-401d-9df7-f17374abcd99">IDirectManipulationViewport</a>
 

 

