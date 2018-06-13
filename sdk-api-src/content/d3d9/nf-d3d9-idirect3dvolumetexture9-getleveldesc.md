---
UID: NF:d3d9.IDirect3DVolumeTexture9.GetLevelDesc
title: IDirect3DVolumeTexture9::GetLevelDesc
author: windows-sdk-content
description: Retrieves a level description of a volume texture resource.
old-location: direct3d9\idirect3dvolumetexture9__getleveldesc.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvolumetexture9__getleveldesc.htm
ms.author: windowssdkdev
ms.date: 04/10/2018
ms.keywords: 6c5724cb-a5d1-ccdb-bcca-67000d91dacf, GetLevelDesc, GetLevelDesc method [Direct3D 9], GetLevelDesc method [Direct3D 9],IDirect3DVolumeTexture9 interface, IDirect3DVolumeTexture9 interface [Direct3D 9],GetLevelDesc method, IDirect3DVolumeTexture9.GetLevelDesc, IDirect3DVolumeTexture9::GetLevelDesc, d3d9helper/IDirect3DVolumeTexture9::GetLevelDesc, direct3d9.idirect3dvolumetexture9__getleveldesc
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
 - IDirect3DVolumeTexture9.GetLevelDesc
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DVolumeTexture9::GetLevelDesc


## -description


Retrieves a level description of a volume texture resource.


## -parameters




### -param Level [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Identifies a level of the volume texture resource. This method returns a volume description for the level specified by this parameter. 


### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/c0224f4e-3d32-4bdd-b56c-4e8aa291bb27">D3DVOLUME_DESC</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/c0224f4e-3d32-4bdd-b56c-4e8aa291bb27">D3DVOLUME_DESC</a> structure, describing the returned volume texture level. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL is returned if one or more of the arguments are invalid.




## -see-also




<a href="https://msdn.microsoft.com/c92cabb8-61d1-4dcf-acf1-fddd3e007d47">IDirect3DVolumeTexture9</a>
 

 

