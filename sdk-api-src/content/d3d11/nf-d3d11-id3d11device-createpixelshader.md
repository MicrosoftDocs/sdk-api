---
UID: NF:d3d11.ID3D11Device.CreatePixelShader
title: ID3D11Device::CreatePixelShader (d3d11.h)
description: Create a pixel shader. (ID3D11Device.CreatePixelShader)
helpviewer_keywords: ["60e28609-f849-5247-ceff-56bd9925d775","CreatePixelShader","CreatePixelShader method [Direct3D 11]","CreatePixelShader method [Direct3D 11]","ID3D11Device interface","ID3D11Device interface [Direct3D 11]","CreatePixelShader method","ID3D11Device.CreatePixelShader","ID3D11Device::CreatePixelShader","d3d11/ID3D11Device::CreatePixelShader","direct3d11.id3d11device_createpixelshader"]
old-location: direct3d11\id3d11device_createpixelshader.htm
tech.root: direct3d11
ms.assetid: f013a648-fd11-417b-8f87-36a4be901715
ms.date: 12/05/2018
ms.keywords: 60e28609-f849-5247-ceff-56bd9925d775, CreatePixelShader, CreatePixelShader method [Direct3D 11], CreatePixelShader method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreatePixelShader method, ID3D11Device.CreatePixelShader, ID3D11Device::CreatePixelShader, d3d11/ID3D11Device::CreatePixelShader, direct3d11.id3d11device_createpixelshader
req.header: d3d11.h
req.include-header: 
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11Device::CreatePixelShader
 - d3d11/ID3D11Device::CreatePixelShader
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Device.CreatePixelShader
---

# ID3D11Device::CreatePixelShader


## -description

Create a pixel shader.

## -parameters

### -param pShaderBytecode [in]

Type: <b>const void*</b>

A pointer to the compiled shader.

### -param BytecodeLength [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

Size of the compiled pixel shader.

### -param pClassLinkage [in, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classlinkage">ID3D11ClassLinkage</a>*</b>

A pointer to a class linkage interface (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classlinkage">ID3D11ClassLinkage</a>); the value can be <b>NULL</b>.

### -param ppPixelShader [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11pixelshader">ID3D11PixelShader</a>**</b>

Address of a pointer to a <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11pixelshader">ID3D11PixelShader</a> interface. If this is <b>NULL</b>, all other parameters will be validated, and if all parameters pass validation this API will return S_FALSE instead of S_OK.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

After creating the pixel shader, you can set it to the device using <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshader">ID3D11DeviceContext::PSSetShader</a>.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>
