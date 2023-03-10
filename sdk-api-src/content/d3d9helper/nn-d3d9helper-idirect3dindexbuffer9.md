---
UID: NN:d3d9helper.IDirect3DIndexBuffer9
title: IDirect3DIndexBuffer9 (d3d9helper.h)
description: The IDirect3DIndexBuffer9 interface (d3d9helper.h) provides methods that manipulate an index buffer resource.
helpviewer_keywords: ["IDirect3DIndexBuffer9","IDirect3DIndexBuffer9 interface [Direct3D 9]","IDirect3DIndexBuffer9 interface [Direct3D 9]","described","bb9d32d9-1059-d4c2-6c8c-e4d5a1170082","d3d9helper/IDirect3DIndexBuffer9","direct3d9.idirect3dindexbuffer9"]
old-location: direct3d9\idirect3dindexbuffer9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dindexbuffer9.htm
ms.date: 08/12/2022
ms.keywords: IDirect3DIndexBuffer9, IDirect3DIndexBuffer9 interface [Direct3D 9], IDirect3DIndexBuffer9 interface [Direct3D 9],described, bb9d32d9-1059-d4c2-6c8c-e4d5a1170082, d3d9helper/IDirect3DIndexBuffer9, direct3d9.idirect3dindexbuffer9
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
 - IDirect3DIndexBuffer9
 - d3d9helper/IDirect3DIndexBuffer9
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
 - IDirect3DIndexBuffer9
---

# IDirect3DIndexBuffer9 interface


## -description

Applications use the methods of the IDirect3DIndexBuffer9 interface to manipulate an index buffer resource.

## -inheritance

The <b>IDirect3DIndexBuffer9</b> interface inherits from <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dresource9">IDirect3DResource9</a>. <b>IDirect3DIndexBuffer9</b> also has these types of members:

## -remarks

The <b>IDirect3DIndexBuffer9</b> interface is obtained by calling the <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createindexbuffer">IDirect3DDevice9::CreateIndexBuffer</a> method.

This interface inherits additional functionality from the <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dresource9">IDirect3DResource9</a> interface.

This interface, like all COM interfaces, inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.

The LPDIRECT3DINDEXBUFFER9 and PDIRECT3DINDEXBUFFER9 types are defined as pointers to the <b>IDirect3DIndexBuffer9</b> interface. 


```

typedef struct IDirect3DIndexBuffer9 *LPDIRECT3DINDEXBUFFER9, *PDIRECT3DINDEXBUFFER9;

```

## -see-also

<a href="/windows/desktop/direct3d9/dx9-graphics-reference-d3d-interfaces">Direct3D Interfaces</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createindexbuffer">IDirect3DDevice9::CreateIndexBuffer</a>



<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dresource9">IDirect3DResource9</a>



<a href="/windows/desktop/direct3d9/index-buffers">Index Buffers (Direct3D 9)</a>
