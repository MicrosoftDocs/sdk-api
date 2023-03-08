---
UID: NF:d3d9.IDirect3DDevice9.SetPixelShader
title: IDirect3DDevice9::SetPixelShader (d3d9.h)
description: The IDirect3DDevice9::SetPixelShader method (d3d9.h) sets the current pixel shader to a previously created pixel shader.
helpviewer_keywords: ["IDirect3DDevice9 interface [Direct3D 9]","SetPixelShader method","IDirect3DDevice9.SetPixelShader","IDirect3DDevice9::SetPixelShader","SetPixelShader","SetPixelShader method [Direct3D 9]","SetPixelShader method [Direct3D 9]","IDirect3DDevice9 interface","c65d883e-77d2-f541-2bd4-48dba090930c","d3d9helper/IDirect3DDevice9::SetPixelShader","direct3d9.idirect3ddevice9__setpixelshader"]
old-location: direct3d9\idirect3ddevice9__setpixelshader.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setpixelshader.htm
ms.date: 08/11/2022
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],SetPixelShader method, IDirect3DDevice9.SetPixelShader, IDirect3DDevice9::SetPixelShader, SetPixelShader, SetPixelShader method [Direct3D 9], SetPixelShader method [Direct3D 9],IDirect3DDevice9 interface, c65d883e-77d2-f541-2bd4-48dba090930c, d3d9helper/IDirect3DDevice9::SetPixelShader, direct3d9.idirect3ddevice9__setpixelshader
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
 - IDirect3DDevice9::SetPixelShader
 - d3d9/IDirect3DDevice9::SetPixelShader
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
 - IDirect3DDevice9.SetPixelShader
---

# IDirect3DDevice9::SetPixelShader


## -description

Sets the current pixel shader to a previously created pixel shader.

## -parameters

### -param pShader [in]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9">IDirect3DPixelShader9</a>*</b>

Pixel shader interface.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getpixelshader">IDirect3DDevice9::GetPixelShader</a>
