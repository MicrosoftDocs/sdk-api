---
UID: NF:d3d9.IDirect3DDevice9.GetMaterial
title: IDirect3DDevice9::GetMaterial (d3d9.h)
description: The IDirect3DDevice9::GetMaterial method (d3d9.h) retrieves the current material properties for the device.
helpviewer_keywords: ["47d4ab4d-62cb-0012-9d9d-20e1cadba8c4","GetMaterial","GetMaterial method [Direct3D 9]","GetMaterial method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","GetMaterial method","IDirect3DDevice9.GetMaterial","IDirect3DDevice9::GetMaterial","d3d9helper/IDirect3DDevice9::GetMaterial","direct3d9.idirect3ddevice9__getmaterial"]
old-location: direct3d9\idirect3ddevice9__getmaterial.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getmaterial.htm
ms.date: 08/10/2022
ms.keywords: 47d4ab4d-62cb-0012-9d9d-20e1cadba8c4, GetMaterial, GetMaterial method [Direct3D 9], GetMaterial method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetMaterial method, IDirect3DDevice9.GetMaterial, IDirect3DDevice9::GetMaterial, d3d9helper/IDirect3DDevice9::GetMaterial, direct3d9.idirect3ddevice9__getmaterial
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
 - IDirect3DDevice9::GetMaterial
 - d3d9/IDirect3DDevice9::GetMaterial
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
 - IDirect3DDevice9.GetMaterial
---

# IDirect3DDevice9::GetMaterial


## -description

Retrieves the current material properties for the device.

## -parameters

### -param pMaterial [out]

Type: <b><a href="/windows/desktop/direct3d9/d3dmaterial9">D3DMATERIAL9</a>*</b>

Pointer to a <a href="/windows/desktop/direct3d9/d3dmaterial9">D3DMATERIAL9</a> structure to fill with the currently set material properties.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL if the pMaterial parameter is invalid.

## -remarks

This method will not return device state for a device that is created using D3DCREATE_PUREDEVICE. If you want to use this method, you must create your device with any of the other values in <a href="/windows/desktop/direct3d9/d3dcreate">D3DCREATE</a>.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial">IDirect3DDevice9::SetMaterial</a>
