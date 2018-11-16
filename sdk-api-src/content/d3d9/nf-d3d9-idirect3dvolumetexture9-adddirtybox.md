---
UID: NF:d3d9.IDirect3DVolumeTexture9.AddDirtyBox
title: IDirect3DVolumeTexture9::AddDirtyBox
author: windows-sdk-content
description: Adds a dirty region to a volume texture resource.
old-location: direct3d9\idirect3dvolumetexture9__adddirtybox.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvolumetexture9__adddirtybox.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
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
- apiref
: 
- COM
: 
- d3d9.h
: 
- IDirect3DVolumeTexture9.AddDirtyBox
: 
---

# IDirect3DVolumeTexture9::AddDirtyBox


## -description


Adds a dirty region to a volume texture resource.


## -parameters




### -param pDirtyBox [in]

Type: <b>const <a href="https://msdn.microsoft.com/415a96bc-1621-4691-b87a-98ca22f0bf07">D3DBOX</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/415a96bc-1621-4691-b87a-98ca22f0bf07">D3DBOX</a> structure, specifying the dirty region to add. Specifying <b>NULL</b> expands the dirty region to cover the entire volume texture. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



For performance reasons, dirty regions are only recorded for level zero of a texture. For sublevels, it is assumed that the corresponding (scaled) box is also dirty. Dirty regions are automatically recorded when <a href="https://msdn.microsoft.com/732f7711-a71b-4470-824e-4ea0b47e64f7">LockBox</a> is called without <a href="https://msdn.microsoft.com/46a611bd-a1ec-4967-b68d-72661d1b5cad">D3DLOCK_NO_DIRTY_UPDATE</a> or <a href="https://msdn.microsoft.com/46a611bd-a1ec-4967-b68d-72661d1b5cad">D3DLOCK_READONLY</a>.

Using <a href="https://msdn.microsoft.com/46a611bd-a1ec-4967-b68d-72661d1b5cad">D3DLOCK_NO_DIRTY_UPDATE</a> and explicitly specifying dirty regions can be used to increase the efficiency of <a href="https://msdn.microsoft.com/79be31d9-0dd2-416c-b58c-9b3b7777c65c">UpdateTexture</a>. Using this method, applications can optimize what subset of a resource is copied by specifying dirty boxes on the resource. However, the dirty regions may be expanded to optimize alignment.




## -see-also




<a href="https://msdn.microsoft.com/c92cabb8-61d1-4dcf-acf1-fddd3e007d47">IDirect3DVolumeTexture9</a>
 

 

