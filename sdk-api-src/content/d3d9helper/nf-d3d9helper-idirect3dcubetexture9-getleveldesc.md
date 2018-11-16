---
UID: NF:d3d9helper.IDirect3DCubeTexture9.GetLevelDesc
title: IDirect3DCubeTexture9::GetLevelDesc
author: windows-sdk-content
description: Retrieves a description of one face of the specified cube texture level.
old-location: direct3d9\idirect3dcubetexture9__getleveldesc.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dcubetexture9__getleveldesc.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetLevelDesc, GetLevelDesc method [Direct3D 9], GetLevelDesc method [Direct3D 9],IDirect3DCubeTexture9 interface, IDirect3DCubeTexture9 interface [Direct3D 9],GetLevelDesc method, IDirect3DCubeTexture9.GetLevelDesc, IDirect3DCubeTexture9::GetLevelDesc, d3d9helper/IDirect3DCubeTexture9::GetLevelDesc, direct3d9.idirect3dcubetexture9__getleveldesc, f3b033c9-6f8e-47a9-8c20-08c7e254bd9c
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
 - IDirect3DCubeTexture9.GetLevelDesc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d9helper.h
: 
- IDirect3DCubeTexture9.GetLevelDesc
: 
---

# IDirect3DCubeTexture9::GetLevelDesc


## -description


Retrieves a description of one face of the specified cube texture level.


## -parameters




### -param Level [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Specifies a level of a mipmapped cube texture.


### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172611(v=VS.85).aspx">D3DSURFACE_DESC</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb172611(v=VS.85).aspx">D3DSURFACE_DESC</a> structure, describing one face of the specified cube texture level.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be: D3DERR_INVALIDCALL.




## -remarks



The <a href="https://msdn.microsoft.com/en-us/library/Bb172611(v=VS.85).aspx">D3DSURFACE_DESC</a> structure contains Width and Height members, which describe the size of one face in the cube. To get the size of the entire cube, multiply six (the number of cube faces) by the product of Width and Height.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174329(v=VS.85).aspx">IDirect3DCubeTexture9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174330(v=VS.85).aspx">IDirect3DCubeTexture9::AddDirtyRect</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174334(v=VS.85).aspx">IDirect3DCubeTexture9::LockRect</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174335(v=VS.85).aspx">IDirect3DCubeTexture9::UnlockRect</a>
 

 

