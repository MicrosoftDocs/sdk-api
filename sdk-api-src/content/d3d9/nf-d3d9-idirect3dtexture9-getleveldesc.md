---
UID: NF:d3d9.IDirect3DTexture9.GetLevelDesc
title: IDirect3DTexture9::GetLevelDesc
author: windows-sdk-content
description: Retrieves a level description of a texture resource.
old-location: direct3d9\idirect3dtexture9__getleveldesc.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dtexture9__getleveldesc.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: 56fc4d84-d125-0b2e-6670-ecb45faa49cd, GetLevelDesc, GetLevelDesc method [Direct3D 9], GetLevelDesc method [Direct3D 9],IDirect3DTexture9 interface, IDirect3DTexture9 interface [Direct3D 9],GetLevelDesc method, IDirect3DTexture9.GetLevelDesc, IDirect3DTexture9::GetLevelDesc, d3d9helper/IDirect3DTexture9::GetLevelDesc, direct3d9.idirect3dtexture9__getleveldesc
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
 - IDirect3DTexture9.GetLevelDesc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DTexture9::GetLevelDesc


## -description


Retrieves a level description of a texture resource.


## -parameters




### -param Level [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Identifies a level of the texture resource. This method returns a surface description for the level specified by this parameter. 


### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172611(v=VS.85).aspx">D3DSURFACE_DESC</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb172611(v=VS.85).aspx">D3DSURFACE_DESC</a> structure, describing the returned level. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL is returned if one of the arguments is invalid.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205909(v=VS.85).aspx">IDirect3DTexture9</a>
 

 

