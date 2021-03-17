---
UID: NF:d2d1.ID2D1RenderTarget.SaveDrawingState
title: ID2D1RenderTarget::SaveDrawingState (d2d1.h)
description: Saves the current drawing state to the specified ID2D1DrawingStateBlock.
helpviewer_keywords: ["ID2D1RenderTarget interface [Direct2D]","SaveDrawingState method","ID2D1RenderTarget.SaveDrawingState","ID2D1RenderTarget::SaveDrawingState","SaveDrawingState","SaveDrawingState method [Direct2D]","SaveDrawingState method [Direct2D]","ID2D1RenderTarget interface","d2d1/ID2D1RenderTarget::SaveDrawingState","direct2d.ID2D1RenderTarget_SaveDrawingState"]
old-location: direct2d\ID2D1RenderTarget_SaveDrawingState.htm
tech.root: Direct2D
ms.assetid: 8658cdbf-979c-41e2-b180-eb21ad6b63c7
ms.date: 12/05/2018
ms.keywords: ID2D1RenderTarget interface [Direct2D],SaveDrawingState method, ID2D1RenderTarget.SaveDrawingState, ID2D1RenderTarget::SaveDrawingState, SaveDrawingState, SaveDrawingState method [Direct2D], SaveDrawingState method [Direct2D],ID2D1RenderTarget interface, d2d1/ID2D1RenderTarget::SaveDrawingState, direct2d.ID2D1RenderTarget_SaveDrawingState
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1RenderTarget::SaveDrawingState
 - d2d1/ID2D1RenderTarget::SaveDrawingState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1RenderTarget.SaveDrawingState
---

# ID2D1RenderTarget::SaveDrawingState


## -description

Saves the current drawing state to the specified <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1drawingstateblock">ID2D1DrawingStateBlock</a>.

## -parameters

### -param drawingStateBlock [in, out]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1drawingstateblock">ID2D1DrawingStateBlock</a>*</b>

When this method returns, contains the current drawing state of the render target. This parameter must be initialized before passing it to the method.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

