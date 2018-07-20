---
UID: NF:d3d9.IDirect3DCubeTexture9.AddDirtyRect
title: IDirect3DCubeTexture9::AddDirtyRect
author: windows-sdk-content
description: Adds a dirty region to a cube texture resource.
old-location: direct3d9\idirect3dcubetexture9__adddirtyrect.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dcubetexture9__adddirtyrect.htm
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: AddDirtyRect, AddDirtyRect method [Direct3D 9], AddDirtyRect method [Direct3D 9],IDirect3DCubeTexture9 interface, IDirect3DCubeTexture9 interface [Direct3D 9],AddDirtyRect method, IDirect3DCubeTexture9.AddDirtyRect, IDirect3DCubeTexture9::AddDirtyRect, b0dc98c8-8a1a-85fb-09ae-35df9bd8edc0, d3d9helper/IDirect3DCubeTexture9::AddDirtyRect, direct3d9.idirect3dcubetexture9__adddirtyrect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IDirect3DCubeTexture9.AddDirtyRect
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DCubeTexture9::AddDirtyRect


## -description


Adds a dirty region to a cube texture resource.


## -parameters




### -param FaceType [in]

Type: <b><a href="https://msdn.microsoft.com/library/Bb172528(v=VS.85).aspx">D3DCUBEMAP_FACES</a></b>

Member of the <a href="https://msdn.microsoft.com/library/Bb172528(v=VS.85).aspx">D3DCUBEMAP_FACES</a> enumerated type, identifying the cube map face. 


### -param pDirtyRect [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure, specifying the dirty region. Specifying <b>NULL</b> expands the dirty region to cover the entire cube texture. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be: D3DERR_INVALIDCALL.




## -remarks



For performance reasons, dirty regions are only recorded for level zero of a texture. For sublevels, it is assumed that the corresponding (scaled) rectangle or box is also dirty. Dirty regions are automatically recorded when <a href="https://msdn.microsoft.com/library/Bb174334(v=VS.85).aspx">IDirect3DCubeTexture9::LockRect</a> is called without <a href="https://msdn.microsoft.com/library/Bb172568(v=VS.85).aspx">D3DLOCK_NO_DIRTY_UPDATE</a> or <a href="https://msdn.microsoft.com/library/Bb172568(v=VS.85).aspx">D3DLOCK_READONLY</a>. The destination surface of <a href="https://msdn.microsoft.com/library/Bb205857(v=VS.85).aspx">IDirect3DDevice9::UpdateSurface</a> is also marked dirty automatically.

Using <a href="https://msdn.microsoft.com/library/Bb172568(v=VS.85).aspx">D3DLOCK_NO_DIRTY_UPDATE</a> and explicitly specifying dirty regions can be used to increase the efficiency of <a href="https://msdn.microsoft.com/library/Bb205858(v=VS.85).aspx">IDirect3DDevice9::UpdateTexture</a>. Using this method, applications can optimize what subset of a resource is copied by specifying dirty regions on the resource. However, the dirty regions may be expanded to optimize alignment.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb174329(v=VS.85).aspx">IDirect3DCubeTexture9</a>



<a href="https://msdn.microsoft.com/library/Bb174332(v=VS.85).aspx">IDirect3DCubeTexture9::GetLevelDesc</a>



<a href="https://msdn.microsoft.com/library/Bb174334(v=VS.85).aspx">IDirect3DCubeTexture9::LockRect</a>



<a href="https://msdn.microsoft.com/library/Bb174335(v=VS.85).aspx">IDirect3DCubeTexture9::UnlockRect</a>
 

 

