---
UID: NF:d3d9.IDirect3DBaseTexture9.GetLevelCount
title: IDirect3DBaseTexture9::GetLevelCount (d3d9.h)
description: Returns the number of texture levels in a multilevel texture.helpviewer_keywords: ["GetLevelCount","GetLevelCount method [Direct3D 9]","GetLevelCount method [Direct3D 9]","IDirect3DBaseTexture9 interface","IDirect3DBaseTexture9 interface [Direct3D 9]","GetLevelCount method","IDirect3DBaseTexture9.GetLevelCount","IDirect3DBaseTexture9::GetLevelCount","d1e2b647-f3f4-ac84-e24e-feeb8e0c6bf8","d3d9helper/IDirect3DBaseTexture9::GetLevelCount","direct3d9.idirect3dbasetexture9__getlevelcount"]
old-location: direct3d9\idirect3dbasetexture9__getlevelcount.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dbasetexture9__getlevelcount.htm
ms.date: 12/05/2018
ms.keywords: GetLevelCount, GetLevelCount method [Direct3D 9], GetLevelCount method [Direct3D 9],IDirect3DBaseTexture9 interface, IDirect3DBaseTexture9 interface [Direct3D 9],GetLevelCount method, IDirect3DBaseTexture9.GetLevelCount, IDirect3DBaseTexture9::GetLevelCount, d1e2b647-f3f4-ac84-e24e-feeb8e0c6bf8, d3d9helper/IDirect3DBaseTexture9::GetLevelCount, direct3d9.idirect3dbasetexture9__getlevelcount
f1_keywords:
- d3d9/IDirect3DBaseTexture9.GetLevelCount
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D3D9.lib
- D3D9.dll
api_name:
- IDirect3DBaseTexture9.GetLevelCount
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DBaseTexture9::GetLevelCount


## -description


Returns the number of texture levels in a multilevel texture.


## -parameters






## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

A <a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">DWORD</a> value that indicates the number of texture levels in a multilevel texture.




## -remarks



<div class="alert"><b>Warning</b>  If you create a texture with <a href="https://docs.microsoft.com/windows/desktop/direct3d9/d3dusage">D3DUSAGE_AUTOGENMIPMAP</a> to make that texture automatically generate sublevels, <b>GetLevelCount</b> always returns 1 for the number of levels.</div>
<div> </div>
This method applies to the following interfaces, which inherit from <a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9">IDirect3DBaseTexture9</a>.

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9">IDirect3DCubeTexture9</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dtexture9">IDirect3DTexture9</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9">IDirect3DVolumeTexture9</a>
</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9">IDirect3DBaseTexture9</a>
 

 

