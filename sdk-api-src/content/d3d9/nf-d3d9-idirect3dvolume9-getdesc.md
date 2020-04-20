---
UID: NF:d3d9.IDirect3DVolume9.GetDesc
title: IDirect3DVolume9::GetDesc (d3d9.h)
description: Retrieves a description of the volume.helpviewer_keywords: ["6ce3365b-f9f8-dd10-e1a5-c17ea631f175","GetDesc","GetDesc method [Direct3D 9]","GetDesc method [Direct3D 9]","IDirect3DVolume9 interface","IDirect3DVolume9 interface [Direct3D 9]","GetDesc method","IDirect3DVolume9.GetDesc","IDirect3DVolume9::GetDesc","d3d9helper/IDirect3DVolume9::GetDesc","direct3d9.idirect3dvolume9__getdesc"]
old-location: direct3d9\idirect3dvolume9__getdesc.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvolume9__getdesc.htm
ms.date: 12/05/2018
ms.keywords: 6ce3365b-f9f8-dd10-e1a5-c17ea631f175, GetDesc, GetDesc method [Direct3D 9], GetDesc method [Direct3D 9],IDirect3DVolume9 interface, IDirect3DVolume9 interface [Direct3D 9],GetDesc method, IDirect3DVolume9.GetDesc, IDirect3DVolume9::GetDesc, d3d9helper/IDirect3DVolume9::GetDesc, direct3d9.idirect3dvolume9__getdesc
f1_keywords:
- d3d9/IDirect3DVolume9.GetDesc
dev_langs:
- c++
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
- IDirect3DVolume9.GetDesc
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DVolume9::GetDesc


## -description


Retrieves a description of the volume.


## -parameters




### -param pDesc [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/direct3d9/d3dvolume-desc">D3DVOLUME_DESC</a>*</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/direct3d9/d3dvolume-desc">D3DVOLUME_DESC</a> structure, describing the volume. 


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL is returned if the argument is invalid.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvolume9">IDirect3DVolume9</a>
 

 

