---
UID: NF:d2d1.ID2D1RenderTarget.FillMesh
title: ID2D1RenderTarget::FillMesh (d2d1.h)
description: Paints the interior of the specified mesh.
helpviewer_keywords: ["FillMesh","FillMesh method [Direct2D]","FillMesh method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","FillMesh method","ID2D1RenderTarget.FillMesh","ID2D1RenderTarget::FillMesh","d2d1/ID2D1RenderTarget::FillMesh","direct2d.ID2D1RenderTarget_FillMesh"]
old-location: direct2d\ID2D1RenderTarget_FillMesh.htm
tech.root: Direct2D
ms.assetid: e22c9169-e770-4f3d-819b-b9363b6e6542
ms.date: 12/05/2018
ms.keywords: FillMesh, FillMesh method [Direct2D], FillMesh method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],FillMesh method, ID2D1RenderTarget.FillMesh, ID2D1RenderTarget::FillMesh, d2d1/ID2D1RenderTarget::FillMesh, direct2d.ID2D1RenderTarget_FillMesh
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
 - ID2D1RenderTarget::FillMesh
 - d2d1/ID2D1RenderTarget::FillMesh
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
 - ID2D1RenderTarget.FillMesh
---

# ID2D1RenderTarget::FillMesh


## -description

Paints the interior of the specified mesh.

## -parameters

### -param mesh [in]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1mesh">ID2D1Mesh</a>*</b>

The mesh to paint.

### -param brush [in]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

The brush used to paint the mesh.

## -remarks

The current antialias mode of the render target must be <a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_antialias_mode">D2D1_ANTIALIAS_MODE_ALIASED</a> when <b>FillMesh</b> is called. To change the render target's antialias mode, use the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode">SetAntialiasMode</a> method.

<b>FillMesh</b> does not expect a particular winding order for the triangles in the <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1mesh">ID2D1Mesh</a>; both clockwise and counter-clockwise will work. 

This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <b>FillMesh</b>) failed, check the result returned by the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">ID2D1RenderTarget::EndDraw</a> or <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush">ID2D1RenderTarget::Flush</a> methods.

## -see-also

<a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_antialias_mode">D2D1_ANTIALIAS_MODE_ALIASED</a>



<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>



<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode">SetAntialiasMode</a>

