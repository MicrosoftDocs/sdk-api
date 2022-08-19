---
UID: NF:d3d9helper.IDirect3DDevice9.CreatePixelShader
title: IDirect3DDevice9::CreatePixelShader (d3d9helper.h)
description: The IDirect3DDevice9::CreatePixelShader method (d3d9.h) creates a pixel shader.  
helpviewer_keywords: ["CreatePixelShader","CreatePixelShader method [Direct3D 9]","CreatePixelShader method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","CreatePixelShader method","IDirect3DDevice9.CreatePixelShader","IDirect3DDevice9::CreatePixelShader","d3d9helper/IDirect3DDevice9::CreatePixelShader","dbb7453e-679d-3725-52e6-92748cf274cc","direct3d9.idirect3ddevice9__createpixelshader"]
old-location: direct3d9\idirect3ddevice9__createpixelshader.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__createpixelshader.htm
ms.date: 08/11/2022
ms.keywords: CreatePixelShader, CreatePixelShader method [Direct3D 9], CreatePixelShader method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],CreatePixelShader method, IDirect3DDevice9.CreatePixelShader, IDirect3DDevice9::CreatePixelShader, d3d9helper/IDirect3DDevice9::CreatePixelShader, dbb7453e-679d-3725-52e6-92748cf274cc, direct3d9.idirect3ddevice9__createpixelshader
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
 - IDirect3DDevice9::CreatePixelShader
 - d3d9helper/IDirect3DDevice9::CreatePixelShader
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
 - IDirect3DDevice9.CreatePixelShader
---

# IDirect3DDevice9::CreatePixelShader


## -description

Creates a pixel shader.

## -parameters

### -param pFunction [in]

Type: <b>const <a href="/windows/desktop/WinProg/windows-data-types">DWORD</a>*</b>

Pointer to the pixel shader function token array, specifying the blending operations. This value cannot be <b>NULL</b>.

### -param ppShader [out, retval]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9">IDirect3DPixelShader9</a>**</b>

Pointer to the returned pixel shader interface. See <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9">IDirect3DPixelShader9</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL, D3DERR_OUTOFVIDEOMEMORY, 
E_OUTOFMEMORY.

## -see-also

<a href="/windows/desktop/direct3d9/d3dxassembleshader">D3DXAssembleShader</a>



<a href="/windows/desktop/direct3d9/d3dxassembleshaderfromfile">D3DXAssembleShaderFromFile</a>



<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>
