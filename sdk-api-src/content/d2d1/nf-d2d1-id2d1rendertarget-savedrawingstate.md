---
UID: NF:d2d1.ID2D1RenderTarget.SaveDrawingState
title: ID2D1RenderTarget::SaveDrawingState (d2d1.h)
author: windows-sdk-content
description: Saves the current drawing state to the specified ID2D1DrawingStateBlock.
old-location: direct2d\ID2D1RenderTarget_SaveDrawingState.htm
tech.root: Direct2D
ms.assetid: 8658cdbf-979c-41e2-b180-eb21ad6b63c7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID2D1RenderTarget interface [Direct2D],SaveDrawingState method, ID2D1RenderTarget.SaveDrawingState, ID2D1RenderTarget::SaveDrawingState, SaveDrawingState, SaveDrawingState method [Direct2D], SaveDrawingState method [Direct2D],ID2D1RenderTarget interface, d2d1/ID2D1RenderTarget::SaveDrawingState, direct2d.ID2D1RenderTarget_SaveDrawingState
ms.topic: method
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1RenderTarget.SaveDrawingState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1RenderTarget::SaveDrawingState


## -description


Saves the current drawing state to the specified <a href="https://msdn.microsoft.com/9a3d9146-0e1b-4642-ad5d-ff1d09a93d2b">ID2D1DrawingStateBlock</a>.


## -parameters




### -param drawingStateBlock [in, out]

Type: <b><a href="https://msdn.microsoft.com/9a3d9146-0e1b-4642-ad5d-ff1d09a93d2b">ID2D1DrawingStateBlock</a>*</b>

When this method returns, contains the current drawing state of the render target. This parameter must be initialized before passing it to the method.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

