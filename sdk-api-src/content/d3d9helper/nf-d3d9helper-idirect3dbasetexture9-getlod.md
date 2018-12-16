---
UID: NF:d3d9helper.IDirect3DBaseTexture9.GetLOD
title: IDirect3DBaseTexture9::GetLOD
author: windows-sdk-content
description: Returns a value clamped to the maximum level-of-detail set for a managed texture (this method is not supported for an unmanaged texture).
old-location: direct3d9\idirect3dbasetexture9__getlod.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dbasetexture9__getlod.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetLOD, GetLOD method [Direct3D 9], GetLOD method [Direct3D 9],IDirect3DBaseTexture9 interface, IDirect3DBaseTexture9 interface [Direct3D 9],GetLOD method, IDirect3DBaseTexture9.GetLOD, IDirect3DBaseTexture9::GetLOD, a04e1586-ff6d-b7ed-c4b5-175ecbe9e41c, d3d9helper/IDirect3DBaseTexture9::GetLOD, direct3d9.idirect3dbasetexture9__getlod
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
 - IDirect3DBaseTexture9.GetLOD
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DBaseTexture9::GetLOD


## -description


Returns a value clamped to the maximum level-of-detail set for a managed texture (this method is not supported for an unmanaged texture).


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

A DWORD value, clamped to the maximum level-of-detail value (one less than the total number of levels). Calling <b>GetLOD</b> on an unmanaged texture is not supported and will result in a <a href="https://msdn.microsoft.com/en-us/library/Bb172554(v=VS.85).aspx">D3DERR</a> error code being returned.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174322(v=VS.85).aspx">IDirect3DBaseTexture9</a>
 

 

