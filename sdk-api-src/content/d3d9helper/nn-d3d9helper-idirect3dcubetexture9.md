---
UID: NN:d3d9helper.IDirect3DCubeTexture9
title: IDirect3DCubeTexture9 (d3d9helper.h)
description: Applications use the methods of the IDirect3DCubeTexture9 interface to manipulate a cube texture resource.
old-location: direct3d9\idirect3dcubetexture9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dcubetexture9.htm
ms.date: 12/05/2018
ms.keywords: 44cd2690-0c08-62c5-decf-0c54344edb9b, IDirect3DCubeTexture9, IDirect3DCubeTexture9 interface [Direct3D 9], IDirect3DCubeTexture9 interface [Direct3D 9],described, d3d9helper/IDirect3DCubeTexture9, direct3d9.idirect3dcubetexture9
f1_keywords:
- d3d9helper/IDirect3DCubeTexture9
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DCubeTexture9 interface


## -description


Applications use the methods of the IDirect3DCubeTexture9 interface to manipulate a cube texture resource.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DCubeTexture9</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9">IDirect3DBaseTexture9</a>. <b>IDirect3DCubeTexture9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirect3DCubeTexture9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3dcubetexture9-adddirtyrect">AddDirtyRect</a>
</td>
<td align="left" width="63%">
Adds a dirty region to a cube texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3dcubetexture9-getcubemapsurface">GetCubeMapSurface</a>
</td>
<td align="left" width="63%">
Retrieves a cube texture map surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3dcubetexture9-getleveldesc">GetLevelDesc</a>
</td>
<td align="left" width="63%">
Retrieves a description of one face of the specified cube texture level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3dcubetexture9-lockrect">LockRect</a>
</td>
<td align="left" width="63%">
Locks a rectangle on a cube texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3dcubetexture9-unlockrect">UnlockRect</a>
</td>
<td align="left" width="63%">
Unlocks a rectangle on a cube texture resource.

</td>
</tr>
</table> 


## -remarks



The <b>IDirect3DCubeTexture9</b> interface can be obtained by calling the <a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createcubetexture">IDirect3DDevice9::CreateCubeTexture</a> method or one of the D3DXCreateCubeTexture<i>xxx</i> functions.

This interface inherits additional functionality from the <a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9">IDirect3DBaseTexture9</a> interface.

This interface, like all COM interfaces, inherits additional functionality from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.

The LPDIRECT3DCUBETEXTURE9 and PDIRECT3DCubeTexture9 types are defined as pointers to the <b>IDirect3DCubeTexture9</b> interface.
    

    


```

typedef struct IDirect3DCubeTexture9 *LPDIRECT3DCUBETEXTURE9, *PDIRECT3DCubeTexture9;

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d9/d3dxcreatecubetexture">D3DXCreateCubeTexture</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d9/d3dxcreatecubetexturefromfile">D3DXCreateCubeTextureFromFile</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d9/d3dxcreatecubetexturefromfileex">D3DXCreateCubeTextureFromFileEx</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d9/d3dxcreatecubetexturefromfileinmemory">D3DXCreateCubeTextureFromFileInMemory</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d9/d3dxcreatecubetexturefromfileinmemoryex">D3DXCreateCubeTextureFromFileInMemoryEx</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d9/d3dxcreatecubetexturefromresource">D3DXCreateCubeTextureFromResource</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d9/d3dxcreatecubetexturefromresourceex">D3DXCreateCubeTextureFromResourceEx</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d9/dx9-graphics-reference-d3d-interfaces">Direct3D Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9">IDirect3DBaseTexture9</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createcubetexture">IDirect3DDevice9::CreateCubeTexture</a>
 

 

