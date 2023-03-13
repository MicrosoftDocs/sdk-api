---
UID: NF:d3d9.IDirect3DBaseTexture9.SetLOD
title: IDirect3DBaseTexture9::SetLOD (d3d9.h)
description: The IDirect3DBaseTexture9::SetLOD sets the most detailed level-of-detail for a managed texture.
helpviewer_keywords: ["IDirect3DBaseTexture9 interface [Direct3D 9]","SetLOD method","IDirect3DBaseTexture9.SetLOD","IDirect3DBaseTexture9::SetLOD","SetLOD","SetLOD method [Direct3D 9]","SetLOD method [Direct3D 9]","IDirect3DBaseTexture9 interface","d3d9helper/IDirect3DBaseTexture9::SetLOD","direct3d9.idirect3dbasetexture9__setlod","e09d34c8-aef0-62f8-8160-11d659b8bb51"]
old-location: direct3d9\idirect3dbasetexture9__setlod.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dbasetexture9__setlod.htm
ms.date: 08/10/2022
ms.keywords: IDirect3DBaseTexture9 interface [Direct3D 9],SetLOD method, IDirect3DBaseTexture9.SetLOD, IDirect3DBaseTexture9::SetLOD, SetLOD, SetLOD method [Direct3D 9], SetLOD method [Direct3D 9],IDirect3DBaseTexture9 interface, d3d9helper/IDirect3DBaseTexture9::SetLOD, direct3d9.idirect3dbasetexture9__setlod, e09d34c8-aef0-62f8-8160-11d659b8bb51
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DBaseTexture9::SetLOD
 - d3d9/IDirect3DBaseTexture9::SetLOD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DBaseTexture9.SetLOD
---

# IDirect3DBaseTexture9::SetLOD


## -description

Sets the most detailed level-of-detail for a managed texture.

## -parameters

### -param LODNew [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Most detailed level-of-detail value to set for the mipmap chain.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

A DWORD value, clamped to the maximum level-of-detail value (one less than the total number of levels). Subsequent calls to this method will return the clamped value, not the level-of-detail value that was previously set.

## -remarks

This method applies to the following interfaces, which inherit from <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9">IDirect3DBaseTexture9</a>.

<ul>
<li>
<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9">IDirect3DCubeTexture9</a>
</li>
<li>
<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dtexture9">IDirect3DTexture9</a>
</li>
<li>
<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9">IDirect3DVolumeTexture9</a>
</li>
<li>
<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dresource9">IDirect3DResource9</a>
</li>
</ul>
<b>SetLOD</b> is used for level-of-detail control of managed textures. This method returns 0 on nonmanaged textures.

<b>SetLOD</b> communicates to the Direct3D texture manager the most detailed mipmap in the chain that should be loaded into local video memory. For example, in a five-level mipmap chain, setting LODNew to 2 indicates that the texture manager should load only mipmap levels 2 through 4 into local video memory at any given time. 

More specifically, if the texture was created with the dimensions of 256x256, setting the most detailed level to 0 indicates that 256 x 256 is the largest mipmap available, setting the most detailed level to 1 indicates that 128 x 128 is the largest mipmap available, and so on, up to the most detailed mip level (the smallest texture size) for the chain.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9">IDirect3DBaseTexture9</a>
