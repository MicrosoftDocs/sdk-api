---
UID: NN:d3d9.IDirect3DCubeTexture9
title: IDirect3DCubeTexture9 (d3d9.h)
description: The IDirect3DCubeTexture9 (d3d9.h) interface applications use the methods of the IDirect3DCubeTexture9 interface to manipulate a cube texture resource.
helpviewer_keywords: ["44cd2690-0c08-62c5-decf-0c54344edb9b","IDirect3DCubeTexture9","IDirect3DCubeTexture9 interface [Direct3D 9]","IDirect3DCubeTexture9 interface [Direct3D 9]","described","d3d9helper/IDirect3DCubeTexture9","direct3d9.idirect3dcubetexture9"]
old-location: direct3d9\idirect3dcubetexture9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dcubetexture9.htm
ms.date: 08/11/2022
ms.keywords: 44cd2690-0c08-62c5-decf-0c54344edb9b, IDirect3DCubeTexture9, IDirect3DCubeTexture9 interface [Direct3D 9], IDirect3DCubeTexture9 interface [Direct3D 9],described, d3d9helper/IDirect3DCubeTexture9, direct3d9.idirect3dcubetexture9
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
 - IDirect3DCubeTexture9
 - d3d9/IDirect3DCubeTexture9
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
 - IDirect3DCubeTexture9
---

# IDirect3DCubeTexture9 interface


## -description

Applications use the methods of the IDirect3DCubeTexture9 interface to manipulate a cube texture resource.

## -inheritance

The <b>IDirect3DCubeTexture9</b> interface inherits from <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9">IDirect3DBaseTexture9</a>. <b>IDirect3DCubeTexture9</b> also has these types of members:

## -remarks

The <b>IDirect3DCubeTexture9</b> interface can be obtained by calling the <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createcubetexture">IDirect3DDevice9::CreateCubeTexture</a> method or one of the D3DXCreateCubeTexture<i>xxx</i> functions.

This interface inherits additional functionality from the <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9">IDirect3DBaseTexture9</a> interface.

This interface, like all COM interfaces, inherits additional functionality from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.

The LPDIRECT3DCUBETEXTURE9 and PDIRECT3DCubeTexture9 types are defined as pointers to the <b>IDirect3DCubeTexture9</b> interface.
    

    


```

typedef struct IDirect3DCubeTexture9 *LPDIRECT3DCUBETEXTURE9, *PDIRECT3DCubeTexture9;

```

## -see-also

<a href="/windows/desktop/direct3d9/d3dxcreatecubetexture">D3DXCreateCubeTexture</a>



<a href="/windows/desktop/direct3d9/d3dxcreatecubetexturefromfile">D3DXCreateCubeTextureFromFile</a>



<a href="/windows/desktop/direct3d9/d3dxcreatecubetexturefromfileex">D3DXCreateCubeTextureFromFileEx</a>



<a href="/windows/desktop/direct3d9/d3dxcreatecubetexturefromfileinmemory">D3DXCreateCubeTextureFromFileInMemory</a>



<a href="/windows/desktop/direct3d9/d3dxcreatecubetexturefromfileinmemoryex">D3DXCreateCubeTextureFromFileInMemoryEx</a>



<a href="/windows/desktop/direct3d9/d3dxcreatecubetexturefromresource">D3DXCreateCubeTextureFromResource</a>



<a href="/windows/desktop/direct3d9/d3dxcreatecubetexturefromresourceex">D3DXCreateCubeTextureFromResourceEx</a>



<a href="/windows/desktop/direct3d9/dx9-graphics-reference-d3d-interfaces">Direct3D Interfaces</a>



<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9">IDirect3DBaseTexture9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createcubetexture">IDirect3DDevice9::CreateCubeTexture</a>
