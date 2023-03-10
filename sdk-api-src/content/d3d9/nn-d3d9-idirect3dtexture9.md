---
UID: NN:d3d9.IDirect3DTexture9
title: IDirect3DTexture9 (d3d9.h)
description: The IDirect3DTexture9 (d3d9.h) interface is used by applications to manipulate a texture resource.
helpviewer_keywords: ["IDirect3DTexture9","IDirect3DTexture9 interface [Direct3D 9]","IDirect3DTexture9 interface [Direct3D 9]","described","d3d9helper/IDirect3DTexture9","direct3d9.idirect3dtexture9","f2bb39fa-d156-a3ea-9ea0-656a78998f7a"]
old-location: direct3d9\idirect3dtexture9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dtexture9.htm
ms.date: 08/11/2022
ms.keywords: IDirect3DTexture9, IDirect3DTexture9 interface [Direct3D 9], IDirect3DTexture9 interface [Direct3D 9],described, d3d9helper/IDirect3DTexture9, direct3d9.idirect3dtexture9, f2bb39fa-d156-a3ea-9ea0-656a78998f7a
req.header: d3d9.h
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
 - IDirect3DTexture9
 - d3d9/IDirect3DTexture9
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
 - IDirect3DTexture9
---

# IDirect3DTexture9 interface


## -description

Applications use the methods of the IDirect3DTexture9 interface to manipulate a texture resource.

## -inheritance

The <b>IDirect3DTexture9</b> interface inherits from <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9">IDirect3DBaseTexture9</a>. <b>IDirect3DTexture9</b> also has these types of members:

## -remarks

The <b>IDirect3DTexture9</b> interface can be obtained by calling the <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createtexture">IDirect3DDevice9::CreateTexture</a> method or one of the D3DXCreateTexture<i>xxx</i> functions.

This interface inherits additional functionality from the <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9">IDirect3DBaseTexture9</a> interface.

This interface, like all COM interfaces, inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.

The LPDIRECT3DTEXTURE9 and PDIRECT3DTEXTURE9 types are defined as pointers to the <b>IDirect3DTexture9</b> interface.
    

    


```

typedef struct IDirect3DTexture9 *LPDIRECT3DTEXTURE9, *PDIRECT3DTEXTURE9;

```

## -see-also

<a href="/windows/desktop/direct3d9/d3dxcreatetexture">D3DXCreateTexture</a>



<a href="/windows/desktop/direct3d9/d3dxcreatetexturefromfile">D3DXCreateTextureFromFile</a>



<a href="/windows/desktop/direct3d9/d3dxcreatetexturefromfileex">D3DXCreateTextureFromFileEx</a>



<a href="/windows/desktop/direct3d9/d3dxcreatetexturefromfileinmemory">D3DXCreateTextureFromFileInMemory</a>



<a href="/windows/desktop/direct3d9/d3dxcreatetexturefromfileinmemoryex">D3DXCreateTextureFromFileInMemoryEx</a>



<a href="/windows/desktop/direct3d9/d3dxcreatetexturefromresource">D3DXCreateTextureFromResource</a>



<a href="/windows/desktop/direct3d9/d3dxcreatetexturefromresourceex">D3DXCreateTextureFromResourceEx</a>



<a href="/windows/desktop/direct3d9/dx9-graphics-reference-d3d-interfaces">Direct3D Interfaces</a>



<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9">IDirect3DBaseTexture9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createtexture">IDirect3DDevice9::CreateTexture</a>
