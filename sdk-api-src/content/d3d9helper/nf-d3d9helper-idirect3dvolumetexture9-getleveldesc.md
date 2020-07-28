---
UID: NF:d3d9helper.IDirect3DVolumeTexture9.GetLevelDesc
title: IDirect3DVolumeTexture9::GetLevelDesc (d3d9helper.h)
description: Retrieves a level description of a volume texture resource.
helpviewer_keywords: ["6c5724cb-a5d1-ccdb-bcca-67000d91dacf","GetLevelDesc","GetLevelDesc method [Direct3D 9]","GetLevelDesc method [Direct3D 9]","IDirect3DVolumeTexture9 interface","IDirect3DVolumeTexture9 interface [Direct3D 9]","GetLevelDesc method","IDirect3DVolumeTexture9.GetLevelDesc","IDirect3DVolumeTexture9::GetLevelDesc","d3d9helper/IDirect3DVolumeTexture9::GetLevelDesc","direct3d9.idirect3dvolumetexture9__getleveldesc"]
old-location: direct3d9\idirect3dvolumetexture9__getleveldesc.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvolumetexture9__getleveldesc.htm
ms.date: 12/05/2018
ms.keywords: 6c5724cb-a5d1-ccdb-bcca-67000d91dacf, GetLevelDesc, GetLevelDesc method [Direct3D 9], GetLevelDesc method [Direct3D 9],IDirect3DVolumeTexture9 interface, IDirect3DVolumeTexture9 interface [Direct3D 9],GetLevelDesc method, IDirect3DVolumeTexture9.GetLevelDesc, IDirect3DVolumeTexture9::GetLevelDesc, d3d9helper/IDirect3DVolumeTexture9::GetLevelDesc, direct3d9.idirect3dvolumetexture9__getleveldesc
f1_keywords:
- d3d9helper/IDirect3DVolumeTexture9.GetLevelDesc
dev_langs:
- c++
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
- IDirect3DVolumeTexture9.GetLevelDesc
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DVolumeTexture9::GetLevelDesc


## -description


Retrieves a level description of a volume texture resource.


## -parameters




### -param Level [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Identifies a level of the volume texture resource. This method returns a volume description for the level specified by this parameter. 


### -param pDesc [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/direct3d9/d3dvolume-desc">D3DVOLUME_DESC</a>*</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/direct3d9/d3dvolume-desc">D3DVOLUME_DESC</a> structure, describing the returned volume texture level. 


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL is returned if one or more of the arguments are invalid.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9">IDirect3DVolumeTexture9</a>
 

 

