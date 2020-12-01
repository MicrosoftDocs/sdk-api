---
UID: NF:directmanipulation.IDirectManipulationViewport.SetViewportTransform
title: IDirectManipulationViewport::SetViewportTransform (directmanipulation.h)
description: Specifies the transform from the viewport coordinate system to the window client coordinate system.
helpviewer_keywords: ["IDirectManipulationViewport interface [Direct Manipulation]","SetViewportTransform method","IDirectManipulationViewport.SetViewportTransform","IDirectManipulationViewport::SetViewportTransform","SetViewportTransform","SetViewportTransform method [Direct Manipulation]","SetViewportTransform method [Direct Manipulation]","IDirectManipulationViewport interface","directmanipulation.idirectmanipulationviewport_setviewporttransform","directmanipulation/IDirectManipulationViewport::SetViewportTransform"]
old-location: directmanipulation\idirectmanipulationviewport_setviewporttransform.htm
tech.root: directmanipulation
ms.assetid: a35e0565-2833-45d3-b7dc-cf05bf644e96
ms.date: 12/05/2018
ms.keywords: IDirectManipulationViewport interface [Direct Manipulation],SetViewportTransform method, IDirectManipulationViewport.SetViewportTransform, IDirectManipulationViewport::SetViewportTransform, SetViewportTransform, SetViewportTransform method [Direct Manipulation], SetViewportTransform method [Direct Manipulation],IDirectManipulationViewport interface, directmanipulation.idirectmanipulationviewport_setviewporttransform, directmanipulation/IDirectManipulationViewport::SetViewportTransform
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectManipulationViewport::SetViewportTransform
 - directmanipulation/IDirectManipulationViewport::SetViewportTransform
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationViewport.SetViewportTransform
---

# IDirectManipulationViewport::SetViewportTransform


## -description

Specifies the transform from the viewport coordinate system to the window client coordinate system.

## -parameters

### -param matrix [in]

The transform matrix, in row-wise order: _11, _12, _21, _22, _31, _32.

### -param pointCount [in]

The size of the transform matrix. This value is always 6, because a 3x2 matrix is used for all direct manipulation transforms.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Call this function to specify the viewport position, scaling and orientation on the screen. Viewport position, scaling, orientation and size are uniquely determined by the viewport transform and the viewport rectangle. The application can specify the viewport transform using this method, and the viewport rectangle using <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setviewportrect">SetViewportRect</a>. 


The viewport rectangle (the rectangular area inside the content that is visible to the user) is specified in viewport coordinates. If the viewport rectangle top-left point is (0,0), the viewport rectangle is positioned exactly at the viewport coordinate system origin. Viewports offset from the viewport coordinate system origin can be specified in two ways:

<ul>
<li>Through the viewport rectangle top-left point</li>
<li>Through the viewport transform translation component (_31, _32)</li>
</ul>
The viewport transform converts from the viewport coordinate system to the window client coordinate system. <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> ignores the window RTL property, so the client area origin is always the top-left point. 
The transforms are applied in the following order:


<ol>
<li>Viewport rectangle offset</li>
<li>Viewport transform (from viewport to client coordinate system)</li>
<li>Client to screen mapping (from client to screen coordinate system)
</li>
</ol>

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewport">IDirectManipulationViewport</a>