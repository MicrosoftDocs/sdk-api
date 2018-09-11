---
UID: NF:d3d9.IDirect3DVolumeTexture9.AddDirtyBox
title: IDirect3DVolumeTexture9::AddDirtyBox
author: windows-sdk-content
description: Adds a dirty region to a volume texture resource.
old-location: direct3d9\idirect3dvolumetexture9__adddirtybox.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvolumetexture9__adddirtybox.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: 30c24ae6-fb69-6d6d-b5db-8af47fa9f97c, AddDirtyBox, AddDirtyBox method [Direct3D 9], AddDirtyBox method [Direct3D 9],IDirect3DVolumeTexture9 interface, IDirect3DVolumeTexture9 interface [Direct3D 9],AddDirtyBox method, IDirect3DVolumeTexture9.AddDirtyBox, IDirect3DVolumeTexture9::AddDirtyBox, d3d9helper/IDirect3DVolumeTexture9::AddDirtyBox, direct3d9.idirect3dvolumetexture9__adddirtybox
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDirect3DVolumeTexture9.AddDirtyBox
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DVolumeTexture9::AddDirtyBox


## -description


Adds a dirty region to a volume texture resource.


## -parameters




### -param pDirtyBox [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Bb172510(v=VS.85).aspx">D3DBOX</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb172510(v=VS.85).aspx">D3DBOX</a> structure, specifying the dirty region to add. Specifying <b>NULL</b> expands the dirty region to cover the entire volume texture. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



For performance reasons, dirty regions are only recorded for level zero of a texture. For sublevels, it is assumed that the corresponding (scaled) box is also dirty. Dirty regions are automatically recorded when <a href="https://msdn.microsoft.com/en-us/library/Bb205945(v=VS.85).aspx">LockBox</a> is called without <a href="https://msdn.microsoft.com/en-us/library/Bb172568(v=VS.85).aspx">D3DLOCK_NO_DIRTY_UPDATE</a> or <a href="https://msdn.microsoft.com/en-us/library/Bb172568(v=VS.85).aspx">D3DLOCK_READONLY</a>.

Using <a href="https://msdn.microsoft.com/en-us/library/Bb172568(v=VS.85).aspx">D3DLOCK_NO_DIRTY_UPDATE</a> and explicitly specifying dirty regions can be used to increase the efficiency of <a href="https://msdn.microsoft.com/en-us/library/Bb205858(v=VS.85).aspx">UpdateTexture</a>. Using this method, applications can optimize what subset of a resource is copied by specifying dirty boxes on the resource. However, the dirty regions may be expanded to optimize alignment.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205941(v=VS.85).aspx">IDirect3DVolumeTexture9</a>
 

 

