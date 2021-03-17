---
UID: NF:d2d1_1.ID2D1CommandSink.FillMesh
title: ID2D1CommandSink::FillMesh (d2d1_1.h)
description: Indicates a mesh to be filled by the command sink.
helpviewer_keywords: ["FillMesh","FillMesh method [Direct2D]","FillMesh method [Direct2D]","ID2D1CommandSink interface","ID2D1CommandSink interface [Direct2D]","FillMesh method","ID2D1CommandSink.FillMesh","ID2D1CommandSink::FillMesh","d2d1_1/ID2D1CommandSink::FillMesh","direct2d.id2d1commandsink_fillmesh"]
old-location: direct2d\id2d1commandsink_fillmesh.htm
tech.root: Direct2D
ms.assetid: b81ac1d2-06bb-4d39-b03d-c0abf7267c3a
ms.date: 12/05/2018
ms.keywords: FillMesh, FillMesh method [Direct2D], FillMesh method [Direct2D],ID2D1CommandSink interface, ID2D1CommandSink interface [Direct2D],FillMesh method, ID2D1CommandSink.FillMesh, ID2D1CommandSink::FillMesh, d2d1_1/ID2D1CommandSink::FillMesh, direct2d.id2d1commandsink_fillmesh
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1CommandSink::FillMesh
 - d2d1_1/ID2D1CommandSink::FillMesh
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
 - ID2D1CommandSink.FillMesh
---

# ID2D1CommandSink::FillMesh


## -description

Indicates a mesh to be filled by the command sink.

## -parameters

### -param mesh [in]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1mesh">ID2D1Mesh</a>*</b>

The mesh object to be filled.

### -param brush [in]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1brush">ID2D1Brush</a>*</b>

The brush with which to fill the mesh.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandlist-stream">ID2D1CommandList::Stream</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandsink">ID2D1CommandSink</a>



<a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-fillmesh">ID2D1RenderTarget::FillMesh</a>