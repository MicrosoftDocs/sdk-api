---
UID: NF:d3d9helper.IDirect3DDevice9.GetPixelShader
title: IDirect3DDevice9::GetPixelShader (d3d9helper.h)
description: The IDirect3DDevice9::GetPixelShader method (d3d9.h) retrieves the currently set pixel shader.
helpviewer_keywords: ["77c70c81-d458-7302-5a4e-9899aad1f456","GetPixelShader","GetPixelShader method [Direct3D 9]","GetPixelShader method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","GetPixelShader method","IDirect3DDevice9.GetPixelShader","IDirect3DDevice9::GetPixelShader","d3d9helper/IDirect3DDevice9::GetPixelShader","direct3d9.idirect3ddevice9__getpixelshader"]
old-location: direct3d9\idirect3ddevice9__getpixelshader.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getpixelshader.htm
ms.date: 08/11/2022
ms.keywords: 77c70c81-d458-7302-5a4e-9899aad1f456, GetPixelShader, GetPixelShader method [Direct3D 9], GetPixelShader method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetPixelShader method, IDirect3DDevice9.GetPixelShader, IDirect3DDevice9::GetPixelShader, d3d9helper/IDirect3DDevice9::GetPixelShader, direct3d9.idirect3ddevice9__getpixelshader
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
 - IDirect3DDevice9::GetPixelShader
 - d3d9helper/IDirect3DDevice9::GetPixelShader
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
 - IDirect3DDevice9.GetPixelShader
---

# IDirect3DDevice9::GetPixelShader


## -description

Retrieves the currently set pixel shader.

## -parameters

### -param ppShader [out, retval]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9">IDirect3DPixelShader9</a>**</b>

Pointer to a pixel shader interface.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -remarks

This method will not work on a device that is created using D3DCREATE_PUREDEVICE.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader">IDirect3DDevice9::SetPixelShader</a>
