---
UID: NN:d3d9helper.IDirect3DVolumeTexture9
title: IDirect3DVolumeTexture9 (d3d9helper.h)
description: The IDirect3DVolumeTexture9 interface (d3d9helper.h) provides methods that manipulate a volume texture resource.
helpviewer_keywords: ["IDirect3DVolumeTexture9","IDirect3DVolumeTexture9 interface [Direct3D 9]","IDirect3DVolumeTexture9 interface [Direct3D 9]","described","ac7e332f-4255-e077-7804-d9a2e2476d37","d3d9helper/IDirect3DVolumeTexture9","direct3d9.idirect3dvolumetexture9"]
old-location: direct3d9\idirect3dvolumetexture9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvolumetexture9.htm
ms.date: 08/12/2022
ms.keywords: IDirect3DVolumeTexture9, IDirect3DVolumeTexture9 interface [Direct3D 9], IDirect3DVolumeTexture9 interface [Direct3D 9],described, ac7e332f-4255-e077-7804-d9a2e2476d37, d3d9helper/IDirect3DVolumeTexture9, direct3d9.idirect3dvolumetexture9
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
 - IDirect3DVolumeTexture9
 - d3d9helper/IDirect3DVolumeTexture9
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
 - IDirect3DVolumeTexture9
---

# IDirect3DVolumeTexture9 interface


## -description

Applications use the methods of the IDirect3DVolumeTexture9 interface to manipulate a volume texture resource.

## -inheritance

The <b>IDirect3DVolumeTexture9</b> interface inherits from <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9">IDirect3DBaseTexture9</a>. <b>IDirect3DVolumeTexture9</b> also has these types of members:

## -remarks

The <b>IDirect3DVolumeTexture9</b> interface can be obtained by calling the <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvolumetexture">CreateVolumeTexture</a> method or one of the D3DXCreateVolumeTexture<i>xxx</i> functions.

This interface inherits additional functionality from the <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9">IDirect3DBaseTexture9</a> interface.

This interface, like all COM interfaces, inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.

The LPDIRECT3DVOLUMETEXTURE9 and PDIRECT3DVOLUMETEXTURE9 types are defined as pointers to the <b>IDirect3DVolumeTexture9</b> interface.
    

    


```

typedef struct IDirect3DVolumeTexture9 *LPDIRECT3DVOLUMETEXTURE9, *PDIRECT3DVOLUMETEXTURE9;

```

## -see-also

<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvolumetexture">CreateVolumeTexture</a>



<a href="/windows/desktop/direct3d9/d3dxcreatevolumetexture">D3DXCreateVolumeTexture</a>



<a href="/windows/desktop/direct3d9/d3dxcreatevolumetexturefromfile">D3DXCreateVolumeTextureFromFile</a>



<a href="/windows/desktop/direct3d9/d3dxcreatevolumetexturefromfileex">D3DXCreateVolumeTextureFromFileEx</a>



<a href="/windows/desktop/direct3d9/d3dxcreatevolumetexturefromfileinmemory">D3DXCreateVolumeTextureFromFileInMemory</a>



<a href="/windows/desktop/direct3d9/d3dxcreatevolumetexturefromfileinmemoryex">D3DXCreateVolumeTextureFromFileInMemoryEx</a>



<a href="/windows/desktop/direct3d9/d3dxcreatevolumetexturefromresource">D3DXCreateVolumeTextureFromResource</a>



<a href="/windows/desktop/direct3d9/d3dxcreatevolumetexturefromresourceex">D3DXCreateVolumeTextureFromResourceEx</a>



<a href="/windows/desktop/direct3d9/dx9-graphics-reference-d3d-interfaces">Direct3D Interfaces</a>



<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9">IDirect3DBaseTexture9</a>
