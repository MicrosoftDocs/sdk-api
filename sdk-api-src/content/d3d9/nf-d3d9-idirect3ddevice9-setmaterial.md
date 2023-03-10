---
UID: NF:d3d9.IDirect3DDevice9.SetMaterial
title: IDirect3DDevice9::SetMaterial (d3d9.h)
description: The IDirect3DDevice9::SetMaterial method (d3d9.h) sets the material properties for the device.
helpviewer_keywords: ["IDirect3DDevice9 interface [Direct3D 9]","SetMaterial method","IDirect3DDevice9.SetMaterial","IDirect3DDevice9::SetMaterial","SetMaterial","SetMaterial method [Direct3D 9]","SetMaterial method [Direct3D 9]","IDirect3DDevice9 interface","a65e098b-14ec-df07-e795-b22f5ac8fcbd","d3d9helper/IDirect3DDevice9::SetMaterial","direct3d9.idirect3ddevice9__setmaterial"]
old-location: direct3d9\idirect3ddevice9__setmaterial.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setmaterial.htm
ms.date: 08/11/2022
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],SetMaterial method, IDirect3DDevice9.SetMaterial, IDirect3DDevice9::SetMaterial, SetMaterial, SetMaterial method [Direct3D 9], SetMaterial method [Direct3D 9],IDirect3DDevice9 interface, a65e098b-14ec-df07-e795-b22f5ac8fcbd, d3d9helper/IDirect3DDevice9::SetMaterial, direct3d9.idirect3ddevice9__setmaterial
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DDevice9::SetMaterial
 - d3d9/IDirect3DDevice9::SetMaterial
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
 - IDirect3DDevice9.SetMaterial
---

# IDirect3DDevice9::SetMaterial


## -description

Sets the material properties for the device.

## -parameters

### -param pMaterial [in]

Type: <b>const <a href="/windows/desktop/direct3d9/d3dmaterial9">D3DMATERIAL9</a>*</b>

Pointer to a <a href="/windows/desktop/direct3d9/d3dmaterial9">D3DMATERIAL9</a> structure, describing the material properties to set.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL if the pMaterial parameter is invalid.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getmaterial">IDirect3DDevice9::GetMaterial</a>
