---
UID: NF:d3d9helper.IDirect3DDevice9.SetPixelShaderConstantF
title: IDirect3DDevice9::SetPixelShaderConstantF (d3d9helper.h)
description: The IDirect3DDevice9::SetPixelShaderConstantF method (d3d9helper.h) sets a floating-point shader constant.
helpviewer_keywords: ["4fc94dcb-1d4f-d3e3-578a-ca1fec85dd86","IDirect3DDevice9 interface [Direct3D 9]","SetPixelShaderConstantF method","IDirect3DDevice9.SetPixelShaderConstantF","IDirect3DDevice9::SetPixelShaderConstantF","SetPixelShaderConstantF","SetPixelShaderConstantF method [Direct3D 9]","SetPixelShaderConstantF method [Direct3D 9]","IDirect3DDevice9 interface","d3d9helper/IDirect3DDevice9::SetPixelShaderConstantF","direct3d9.idirect3ddevice9__setpixelshaderconstantf"]
old-location: direct3d9\idirect3ddevice9__setpixelshaderconstantf.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setpixelshaderconstantf.htm
ms.date: 08/11/2022
ms.keywords: 4fc94dcb-1d4f-d3e3-578a-ca1fec85dd86, IDirect3DDevice9 interface [Direct3D 9],SetPixelShaderConstantF method, IDirect3DDevice9.SetPixelShaderConstantF, IDirect3DDevice9::SetPixelShaderConstantF, SetPixelShaderConstantF, SetPixelShaderConstantF method [Direct3D 9], SetPixelShaderConstantF method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetPixelShaderConstantF, direct3d9.idirect3ddevice9__setpixelshaderconstantf
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
 - IDirect3DDevice9::SetPixelShaderConstantF
 - d3d9helper/IDirect3DDevice9::SetPixelShaderConstantF
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
 - IDirect3DDevice9.SetPixelShaderConstantF
---

# IDirect3DDevice9::SetPixelShaderConstantF


## -description

Sets a floating-point shader constant.

## -parameters

### -param StartRegister [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Register number that will contain the first constant value.

### -param pConstantData [in]

Type: <b>const float*</b>

Pointer to an array of constants.

### -param Vector4fCount [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of four float vectors in the array of constants.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be
     D3DERR_INVALIDCALL.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getpixelshaderconstantf">IDirect3DDevice9::GetPixelShaderConstantF</a>
