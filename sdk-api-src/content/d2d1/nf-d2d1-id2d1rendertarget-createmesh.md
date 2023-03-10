---
UID: NF:d2d1.ID2D1RenderTarget.CreateMesh
title: ID2D1RenderTarget::CreateMesh (d2d1.h)
description: Create a mesh that uses triangles to describe a shape.
helpviewer_keywords: ["CreateMesh","CreateMesh method [Direct2D]","CreateMesh method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","CreateMesh method","ID2D1RenderTarget.CreateMesh","ID2D1RenderTarget::CreateMesh","d2d1/ID2D1RenderTarget::CreateMesh","direct2d.ID2D1RenderTarget_CreateMesh"]
old-location: direct2d\ID2D1RenderTarget_CreateMesh.htm
tech.root: Direct2D
ms.assetid: 6c0036d8-1f91-4d90-a301-b58bde8da974
ms.date: 12/05/2018
ms.keywords: CreateMesh, CreateMesh method [Direct2D], CreateMesh method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateMesh method, ID2D1RenderTarget.CreateMesh, ID2D1RenderTarget::CreateMesh, d2d1/ID2D1RenderTarget::CreateMesh, direct2d.ID2D1RenderTarget_CreateMesh
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
 - ID2D1RenderTarget::CreateMesh
 - d2d1/ID2D1RenderTarget::CreateMesh
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
 - ID2D1RenderTarget.CreateMesh
---

# ID2D1RenderTarget::CreateMesh


## -description

Create a mesh that uses triangles to describe a shape.

## -parameters

### -param mesh [out]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1mesh">ID2D1Mesh</a>**</b>

When this method returns, contains a pointer to a pointer to the new mesh.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -remarks

To populate a mesh, use its <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1mesh-open">Open</a> method to obtain an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1tessellationsink">ID2D1TessellationSink</a>. To draw the mesh, use the render target's <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillmesh">FillMesh</a> method.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

