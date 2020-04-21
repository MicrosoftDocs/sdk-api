---
UID: NN:d3d9helper.IDirect3DBaseTexture9
title: IDirect3DBaseTexture9 (d3d9helper.h)
description: Applications use the methods of the IDirect3DBaseTexture9 interface to manipulate texture resources including cube and volume textures.helpviewer_keywords: ["9a51f87c-558e-0e06-6372-a3753ac70d17","IDirect3DBaseTexture9","IDirect3DBaseTexture9 interface [Direct3D 9]","IDirect3DBaseTexture9 interface [Direct3D 9]","described","d3d9helper/IDirect3DBaseTexture9","direct3d9.idirect3dbasetexture9"]
old-location: direct3d9\idirect3dbasetexture9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dbasetexture9.htm
ms.date: 12/05/2018
ms.keywords: 9a51f87c-558e-0e06-6372-a3753ac70d17, IDirect3DBaseTexture9, IDirect3DBaseTexture9 interface [Direct3D 9], IDirect3DBaseTexture9 interface [Direct3D 9],described, d3d9helper/IDirect3DBaseTexture9, direct3d9.idirect3dbasetexture9
f1_keywords:
- d3d9helper/IDirect3DBaseTexture9
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
- IDirect3DBaseTexture9
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DBaseTexture9 interface


## -description


Applications use the methods of the IDirect3DBaseTexture9 interface to manipulate texture resources including cube and volume textures.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DBaseTexture9</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dresource9">IDirect3DResource9</a>. <b>IDirect3DBaseTexture9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirect3DBaseTexture9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3dbasetexture9-generatemipsublevels">GenerateMipSubLevels</a>
</td>
<td align="left" width="63%">
Generate mipmap sublevels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3dbasetexture9-getautogenfiltertype">GetAutoGenFilterType</a>
</td>
<td align="left" width="63%">
Get the filter type that is used for automatically generated mipmap sublevels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3dbasetexture9-getlevelcount">GetLevelCount</a>
</td>
<td align="left" width="63%">
Returns the number of texture levels in a multilevel texture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3dbasetexture9-getlod">GetLOD</a>
</td>
<td align="left" width="63%">
Returns a value clamped to the maximum level-of-detail set for a managed texture (this method is not supported for an unmanaged texture).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3dbasetexture9-setautogenfiltertype">SetAutoGenFilterType</a>
</td>
<td align="left" width="63%">
Set the filter type that is used for automatically generated mipmap sublevels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3dbasetexture9-setlod">SetLOD</a>
</td>
<td align="left" width="63%">
Sets the most detailed level-of-detail for a managed texture. 

</td>
</tr>
</table> 


## -remarks



The <b>IDirect3DBaseTexture9</b> interface assigned to a particular stage for a device is obtained by calling the <a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-gettexture">GetTexture</a> method.

The LPDIRECT3DBASETEXTURE9 and PDIRECT3DBASETEXTURE9 types are defined as pointers to the <b>IDirect3DBaseTexture9</b> interface.





```
typedef struct IDirect3DBaseTexture9 *LPDIRECT3DBASETEXTURE9, *PDIRECT3DBASETEXTURE9;
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d9/dx9-graphics-reference-d3d-interfaces">Direct3D Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dresource9">IDirect3DResource9</a>
 

 

