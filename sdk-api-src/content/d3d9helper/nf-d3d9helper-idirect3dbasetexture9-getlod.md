---
UID: NF:d3d9helper.IDirect3DBaseTexture9.GetLOD
title: IDirect3DBaseTexture9::GetLOD (d3d9helper.h)
description: The IDirect3DBaseTexture9::GetLOD (d3d9helper.h) method returns a value clamped to the maximum level-of-detail set for a managed texture.
helpviewer_keywords: ["GetLOD","GetLOD method [Direct3D 9]","GetLOD method [Direct3D 9]","IDirect3DBaseTexture9 interface","IDirect3DBaseTexture9 interface [Direct3D 9]","GetLOD method","IDirect3DBaseTexture9.GetLOD","IDirect3DBaseTexture9::GetLOD","a04e1586-ff6d-b7ed-c4b5-175ecbe9e41c","d3d9helper/IDirect3DBaseTexture9::GetLOD","direct3d9.idirect3dbasetexture9__getlod"]
old-location: direct3d9\idirect3dbasetexture9__getlod.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dbasetexture9__getlod.htm
ms.date: 08/11/2022
ms.keywords: GetLOD, GetLOD method [Direct3D 9], GetLOD method [Direct3D 9],IDirect3DBaseTexture9 interface, IDirect3DBaseTexture9 interface [Direct3D 9],GetLOD method, IDirect3DBaseTexture9.GetLOD, IDirect3DBaseTexture9::GetLOD, a04e1586-ff6d-b7ed-c4b5-175ecbe9e41c, d3d9helper/IDirect3DBaseTexture9::GetLOD, direct3d9.idirect3dbasetexture9__getlod
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DBaseTexture9::GetLOD
 - d3d9helper/IDirect3DBaseTexture9::GetLOD
dev_langs:
 - c++
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
---

# IDirect3DBaseTexture9::GetLOD


## -description

Returns a value clamped to the maximum level-of-detail set for a managed texture (this method is not supported for an unmanaged texture).



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

A DWORD value, clamped to the maximum level-of-detail value (one less than the total number of levels). Calling <b>GetLOD</b> on an unmanaged texture is not supported and will result in a <a href="/windows/desktop/direct3d9/d3derr">D3DERR</a> error code being returned.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9">IDirect3DBaseTexture9</a>
