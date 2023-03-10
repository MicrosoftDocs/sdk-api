---
UID: NF:d3d9helper.IDirect3DDevice9.GetPixelShaderConstantB
title: IDirect3DDevice9::GetPixelShaderConstantB (d3d9helper.h)
description: The IDirect3DDevice9::GetPixelShaderConstantB method (d3d9.h) gets a Boolean shader constant.
helpviewer_keywords: ["GetPixelShaderConstantB","GetPixelShaderConstantB method [Direct3D 9]","GetPixelShaderConstantB method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","GetPixelShaderConstantB method","IDirect3DDevice9.GetPixelShaderConstantB","IDirect3DDevice9::GetPixelShaderConstantB","b5063da2-ebe9-220a-5bcc-e8d602dff035","d3d9helper/IDirect3DDevice9::GetPixelShaderConstantB","direct3d9.idirect3ddevice9__getpixelshaderconstantb"]
old-location: direct3d9\idirect3ddevice9__getpixelshaderconstantb.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getpixelshaderconstantb.htm
ms.date: 08/11/2022
ms.keywords: GetPixelShaderConstantB, GetPixelShaderConstantB method [Direct3D 9], GetPixelShaderConstantB method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetPixelShaderConstantB method, IDirect3DDevice9.GetPixelShaderConstantB, IDirect3DDevice9::GetPixelShaderConstantB, b5063da2-ebe9-220a-5bcc-e8d602dff035, d3d9helper/IDirect3DDevice9::GetPixelShaderConstantB, direct3d9.idirect3ddevice9__getpixelshaderconstantb
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
 - IDirect3DDevice9::GetPixelShaderConstantB
 - d3d9helper/IDirect3DDevice9::GetPixelShaderConstantB
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
 - IDirect3DDevice9.GetPixelShaderConstantB
---

# IDirect3DDevice9::GetPixelShaderConstantB


## -description

Gets a Boolean shader constant.

## -parameters

### -param StartRegister [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Register number that will contain the first constant value.

### -param pConstantData [in, out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

Pointer to an array of constants.

### -param BoolCount [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of Boolean values in the array of constants.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be
     D3DERR_INVALIDCALL.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb">IDirect3DDevice9::SetPixelShaderConstantB</a>
