---
UID: NN:d3d9helper.IDirect3DVolumeTexture9
title: IDirect3DVolumeTexture9 (d3d9helper.h)
author: windows-sdk-content
description: Applications use the methods of the IDirect3DVolumeTexture9 interface to manipulate a volume texture resource.
old-location: direct3d9\idirect3dvolumetexture9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvolumetexture9.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDirect3DVolumeTexture9, IDirect3DVolumeTexture9 interface [Direct3D 9], IDirect3DVolumeTexture9 interface [Direct3D 9],described, ac7e332f-4255-e077-7804-d9a2e2476d37, d3d9helper/IDirect3DVolumeTexture9, direct3d9.idirect3dvolumetexture9
ms.topic: interface
f1_keywords: 
 - "d3d9helper/IDirect3DVolumeTexture9"
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
 - IDirect3DVolumeTexture9
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DVolumeTexture9 interface


## -description


Applications use the methods of the IDirect3DVolumeTexture9 interface to manipulate a volume texture resource.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DVolumeTexture9</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9">IDirect3DBaseTexture9</a>. <b>IDirect3DVolumeTexture9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirect3DVolumeTexture9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox">AddDirtyBox</a>
</td>
<td align="left" width="63%">
Adds a dirty region to a volume texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-getleveldesc">GetLevelDesc</a>
</td>
<td align="left" width="63%">
Retrieves a level description of a volume texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-getvolumelevel">GetVolumeLevel</a>
</td>
<td align="left" width="63%">
Retrieves the specified volume texture level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox">LockBox</a>
</td>
<td align="left" width="63%">
Locks a box on a volume texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-unlockbox">UnlockBox</a>
</td>
<td align="left" width="63%">
Unlocks a box on a volume texture resource.

</td>
</tr>
</table> 


## -remarks



The <b>IDirect3DVolumeTexture9</b> interface can be obtained by calling the <a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvolumetexture">CreateVolumeTexture</a> method or one of the D3DXCreateVolumeTexture<i>xxx</i> functions.

This interface inherits additional functionality from the <a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9">IDirect3DBaseTexture9</a> interface.

This interface, like all COM interfaces, inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.

The LPDIRECT3DVOLUMETEXTURE9 and PDIRECT3DVOLUMETEXTURE9 types are defined as pointers to the <b>IDirect3DVolumeTexture9</b> interface.
    

    


```

typedef struct IDirect3DVolumeTexture9 *LPDIRECT3DVOLUMETEXTURE9, *PDIRECT3DVOLUMETEXTURE9;

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvolumetexture">CreateVolumeTexture</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d9/d3dxcreatevolumetexture">D3DXCreateVolumeTexture</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d9/d3dxcreatevolumetexturefromfile">D3DXCreateVolumeTextureFromFile</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d9/d3dxcreatevolumetexturefromfileex">D3DXCreateVolumeTextureFromFileEx</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d9/d3dxcreatevolumetexturefromfileinmemory">D3DXCreateVolumeTextureFromFileInMemory</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d9/d3dxcreatevolumetexturefromfileinmemoryex">D3DXCreateVolumeTextureFromFileInMemoryEx</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d9/d3dxcreatevolumetexturefromresource">D3DXCreateVolumeTextureFromResource</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d9/d3dxcreatevolumetexturefromresourceex">D3DXCreateVolumeTextureFromResourceEx</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d9/dx9-graphics-reference-d3d-interfaces">Direct3D Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9">IDirect3DBaseTexture9</a>
 

 

