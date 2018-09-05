---
UID: NF:d3d9.IDirect3DBaseTexture9.SetLOD
title: IDirect3DBaseTexture9::SetLOD
author: windows-sdk-content
description: Sets the most detailed level-of-detail for a managed texture.
old-location: direct3d9\idirect3dbasetexture9__setlod.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dbasetexture9__setlod.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IDirect3DBaseTexture9 interface [Direct3D 9],SetLOD method, IDirect3DBaseTexture9.SetLOD, IDirect3DBaseTexture9::SetLOD, SetLOD, SetLOD method [Direct3D 9], SetLOD method [Direct3D 9],IDirect3DBaseTexture9 interface, d3d9helper/IDirect3DBaseTexture9::SetLOD, direct3d9.idirect3dbasetexture9__setlod, e09d34c8-aef0-62f8-8160-11d659b8bb51
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9.h
req.include-header: D3D9.h
req.redist: 
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
tech.root: 
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
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
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DBaseTexture9::SetLOD


## -description


Sets the most detailed level-of-detail for a managed texture. 


## -parameters




### -param LODNew [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Most detailed level-of-detail value to set for the mipmap chain. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

A DWORD value, clamped to the maximum level-of-detail value (one less than the total number of levels). Subsequent calls to this method will return the clamped value, not the level-of-detail value that was previously set.




## -remarks



This method applies to the following interfaces, which inherit from <a href="https://msdn.microsoft.com/d4d7f8b9-2e7b-4445-8380-2d321a46e064">IDirect3DBaseTexture9</a>.

<ul>
<li>
<a href="https://msdn.microsoft.com/59e400ae-d2ec-425c-9adf-49cb5a24c808">IDirect3DCubeTexture9</a>
</li>
<li>
<a href="https://msdn.microsoft.com/fcea1048-1d9b-409f-9b5a-cdf85c30c76e">IDirect3DTexture9</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c92cabb8-61d1-4dcf-acf1-fddd3e007d47">IDirect3DVolumeTexture9</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1fdb0bfe-6e36-49ca-b119-a2b3266037d2">IDirect3DResource9</a>
</li>
</ul>
<b>SetLOD</b> is used for level-of-detail control of managed textures. This method returns 0 on nonmanaged textures.

<b>SetLOD</b> communicates to the Direct3D texture manager the most detailed mipmap in the chain that should be loaded into local video memory. For example, in a five-level mipmap chain, setting LODNew to 2 indicates that the texture manager should load only mipmap levels 2 through 4 into local video memory at any given time. 

More specifically, if the texture was created with the dimensions of 256x256, setting the most detailed level to 0 indicates that 256 x 256 is the largest mipmap available, setting the most detailed level to 1 indicates that 128 x 128 is the largest mipmap available, and so on, up to the most detailed mip level (the smallest texture size) for the chain.




## -see-also




<a href="https://msdn.microsoft.com/d4d7f8b9-2e7b-4445-8380-2d321a46e064">IDirect3DBaseTexture9</a>
 

 

