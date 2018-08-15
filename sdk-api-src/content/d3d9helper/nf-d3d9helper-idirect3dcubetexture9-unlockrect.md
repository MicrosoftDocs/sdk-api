---
UID: NF:d3d9helper.IDirect3DCubeTexture9.UnlockRect
title: IDirect3DCubeTexture9::UnlockRect
author: windows-sdk-content
description: Unlocks a rectangle on a cube texture resource.
old-location: direct3d9\idirect3dcubetexture9__unlockrect.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dcubetexture9__unlockrect.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IDirect3DCubeTexture9 interface [Direct3D 9],UnlockRect method, IDirect3DCubeTexture9.UnlockRect, IDirect3DCubeTexture9::UnlockRect, UnlockRect, UnlockRect method [Direct3D 9], UnlockRect method [Direct3D 9],IDirect3DCubeTexture9 interface, d3d9helper/IDirect3DCubeTexture9::UnlockRect, direct3d9.idirect3dcubetexture9__unlockrect, f5fb42b3-5c6a-7e4c-83fd-575e49595447
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9helper.h
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
req.typenames: D3DVSHADERCAPS2_0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DCubeTexture9.UnlockRect
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DCubeTexture9::UnlockRect


## -description


Unlocks a rectangle on a cube texture resource.


## -parameters




### -param FaceType [in]

Type: <b><a href="https://msdn.microsoft.com/6d18b410-6f22-4202-86ae-6b3ef85e6f69">D3DCUBEMAP_FACES</a></b>

Member of the <a href="https://msdn.microsoft.com/6d18b410-6f22-4202-86ae-6b3ef85e6f69">D3DCUBEMAP_FACES</a> enumerated type, identifying a cube map face. 


### -param Level [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Specifies a level of a mipmapped cube texture. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be: D3DERR_INVALIDCALL.




## -see-also




<a href="https://msdn.microsoft.com/59e400ae-d2ec-425c-9adf-49cb5a24c808">IDirect3DCubeTexture9</a>



<a href="https://msdn.microsoft.com/377536bd-c55c-4ec8-a07c-5addd8e84c3a">IDirect3DCubeTexture9::AddDirtyRect</a>



<a href="https://msdn.microsoft.com/724317a3-1fc7-499d-94b7-759731337a00">IDirect3DCubeTexture9::LockRect</a>
 

 

