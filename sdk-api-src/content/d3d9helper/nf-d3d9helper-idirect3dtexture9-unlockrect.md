---
UID: NF:d3d9helper.IDirect3DTexture9.UnlockRect
title: IDirect3DTexture9::UnlockRect
author: windows-sdk-content
description: Unlocks a rectangle on a texture resource.
old-location: direct3d9\idirect3dtexture9__unlockrect.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dtexture9__unlockrect.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IDirect3DTexture9 interface [Direct3D 9],UnlockRect method, IDirect3DTexture9.UnlockRect, IDirect3DTexture9::UnlockRect, UnlockRect, UnlockRect method [Direct3D 9], UnlockRect method [Direct3D 9],IDirect3DTexture9 interface, d3d9helper/IDirect3DTexture9::UnlockRect, dc06fd43-b5ef-87a2-a68e-2779288b756b, direct3d9.idirect3dtexture9__unlockrect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IDirect3DTexture9.UnlockRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DTexture9::UnlockRect


## -description


Unlocks a rectangle on a texture resource.


## -parameters




### -param Level [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Specifies the level of the texture resource to unlock. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205909(v=VS.85).aspx">IDirect3DTexture9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb205913(v=VS.85).aspx">IDirect3DTexture9::LockRect</a>
 

 

