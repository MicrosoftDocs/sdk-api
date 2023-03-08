---
UID: NF:d3d9.IDirect3DPixelShader9.GetFunction
title: IDirect3DPixelShader9::GetFunction (d3d9.h)
description: The IDirect3DPixelShader9::GetFunction method (d3d9helper.h) gets a pointer to the shader data.
helpviewer_keywords: ["3fd5e480-51b4-f6cc-c9eb-1fa92415018a","GetFunction","GetFunction method [Direct3D 9]","GetFunction method [Direct3D 9]","IDirect3DPixelShader9 interface","IDirect3DPixelShader9 interface [Direct3D 9]","GetFunction method","IDirect3DPixelShader9.GetFunction","IDirect3DPixelShader9::GetFunction","d3d9helper/IDirect3DPixelShader9::GetFunction","direct3d9.idirect3dpixelshader9__getfunction"]
old-location: direct3d9\idirect3dpixelshader9__getfunction.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dpixelshader9__getfunction.htm
ms.date: 08/11/2022
ms.keywords: 3fd5e480-51b4-f6cc-c9eb-1fa92415018a, GetFunction, GetFunction method [Direct3D 9], GetFunction method [Direct3D 9],IDirect3DPixelShader9 interface, IDirect3DPixelShader9 interface [Direct3D 9],GetFunction method, IDirect3DPixelShader9.GetFunction, IDirect3DPixelShader9::GetFunction, d3d9helper/IDirect3DPixelShader9::GetFunction, direct3d9.idirect3dpixelshader9__getfunction
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
 - IDirect3DPixelShader9::GetFunction
 - d3d9/IDirect3DPixelShader9::GetFunction
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
 - IDirect3DPixelShader9.GetFunction
---

# IDirect3DPixelShader9::GetFunction


## -description

Gets a pointer to the shader data.

## -parameters

### -param unnamedParam1 [in, out]

Type: <b>void*</b>

Pointer to a buffer that contains the shader data. The application needs to allocate enough room for this.

### -param pSizeOfData [in, out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

Size of the data, in bytes. To get the buffer size that is needed to retrieve the data, set pData = <b>NULL</b> when calling GetFunction. Then call GetFunction with the returned size, to get the buffer data.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be:
     D3DERR_INVALIDCALL.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9">IDirect3DPixelShader9</a>
