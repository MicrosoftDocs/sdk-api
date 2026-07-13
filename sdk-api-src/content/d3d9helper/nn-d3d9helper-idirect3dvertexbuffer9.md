---
UID: NN:d3d9helper.IDirect3DVertexBuffer9
title: IDirect3DVertexBuffer9 (d3d9helper.h)
description: The IDirect3DVertexBuffer9 interface (d3d9helper.h) provides methods that manipulate vertex buffer resources.
helpviewer_keywords: ["618275d7-1a22-b2cf-581b-9cf2495dc642","IDirect3DVertexBuffer9","IDirect3DVertexBuffer9 interface [Direct3D 9]","IDirect3DVertexBuffer9 interface [Direct3D 9]","described","d3d9helper/IDirect3DVertexBuffer9","direct3d9.idirect3dvertexbuffer9"]
old-location: direct3d9\idirect3dvertexbuffer9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvertexbuffer9.htm
ms.date: 08/12/2022
ms.keywords: 618275d7-1a22-b2cf-581b-9cf2495dc642, IDirect3DVertexBuffer9, IDirect3DVertexBuffer9 interface [Direct3D 9], IDirect3DVertexBuffer9 interface [Direct3D 9],described, d3d9helper/IDirect3DVertexBuffer9, direct3d9.idirect3dvertexbuffer9
req.header: d3d9helper.h
req.include-header: D3D9.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3d9.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DVertexBuffer9
 - d3d9helper/IDirect3DVertexBuffer9
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d9.lib
 - d3d9.dll
api_name:
 - IDirect3DVertexBuffer9
---

# IDirect3DVertexBuffer9 interface


## -description

Applications use the methods of the IDirect3DVertexBuffer9 interface to manipulate vertex buffer resources.

## -inheritance

The <b>IDirect3DVertexBuffer9</b> interface inherits from <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dresource9">IDirect3DResource9</a>. <b>IDirect3DVertexBuffer9</b> also has these types of members:

## -remarks

The <b>IDirect3DVertexBuffer9</b> interface is obtained by calling the <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexbuffer">IDirect3DDevice9::CreateVertexBuffer</a> method.

This interface inherits additional functionality from the <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dresource9">IDirect3DResource9</a> interface.

This interface, like all COM interfaces, inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.

The LPDIRECT3DVERTEXBUFFER9 and PDIRECT3DVERTEXBUFFER9 types are defined as pointers to the <b>IDirect3DVertexBuffer9</b> interface.
    

    


```

typedef struct IDirect3DVertexBuffer9 *LPDIRECT3DVERTEXBUFFER9, *PDIRECT3DVERTEXBUFFER9;

```

## -see-also

<a href="/windows/desktop/direct3d9/dx9-graphics-reference-d3d-interfaces">Direct3D Interfaces</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexbuffer">IDirect3DDevice9::CreateVertexBuffer</a>



<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dresource9">IDirect3DResource9</a>



<a href="/windows/desktop/direct3d9/vertex-buffers">Vertex Buffers (Direct3D 9)</a>
