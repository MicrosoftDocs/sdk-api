---
UID: NN:d3d9helper.IDirect3DResource9
title: IDirect3DResource9 (d3d9helper.h)
description: The IDirect3DResource9 interface (d3d9helper.h) provides methods that query and prepare resources.
helpviewer_keywords: ["IDirect3DResource9","IDirect3DResource9 interface [Direct3D 9]","IDirect3DResource9 interface [Direct3D 9]","described","c545e88d-de95-aa8d-c5e1-4a5285f02095","d3d9helper/IDirect3DResource9","direct3d9.idirect3dresource9"]
old-location: direct3d9\idirect3dresource9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dresource9.htm
ms.date: 08/12/2022
ms.keywords: IDirect3DResource9, IDirect3DResource9 interface [Direct3D 9], IDirect3DResource9 interface [Direct3D 9],described, c545e88d-de95-aa8d-c5e1-4a5285f02095, d3d9helper/IDirect3DResource9, direct3d9.idirect3dresource9
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
 - IDirect3DResource9
 - d3d9helper/IDirect3DResource9
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
 - IDirect3DResource9
---

# IDirect3DResource9 interface


## -description

Applications use the methods of the <b>IDirect3DResource9</b> interface to query and prepare resources.

## -inheritance

The <b>IDirect3DResource9</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirect3DResource9</b> also has these types of members:

## -remarks

To create a texture resource, you can call one of the following methods.

<ul>
<li>
<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createcubetexture">IDirect3DDevice9::CreateCubeTexture</a>
</li>
<li>
<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createtexture">IDirect3DDevice9::CreateTexture</a>
</li>
<li>
<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvolumetexture">IDirect3DDevice9::CreateVolumeTexture</a>
</li>
</ul>
To create a geometry-oriented resource, you can call one of the following methods.

<ul>
<li>
<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createindexbuffer">IDirect3DDevice9::CreateIndexBuffer</a>
</li>
<li>
<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexbuffer">IDirect3DDevice9::CreateVertexBuffer</a>
</li>
</ul>
This interface, like all COM interfaces, inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.

The LPDIRECT3DRESOURCE9 and PDIRECT3DRESOURCE9 types are defined as pointers to the <b>IDirect3DResource9</b> interface. 


    


```

    typedef struct IDirect3DResource9 *LPDIRECT3DRESOURCE9, *PDIRECT3DRESOURCE9;

```

## -see-also

<a href="/windows/desktop/direct3d9/dx9-graphics-reference-d3d-interfaces">Direct3D Interfaces</a>



<a href="/windows/desktop/direct3d9/direct3d-resources">Direct3D Resources (Direct3D 9)</a>
