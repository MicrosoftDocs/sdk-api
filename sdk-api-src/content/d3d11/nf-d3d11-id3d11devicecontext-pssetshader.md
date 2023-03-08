---
UID: NF:d3d11.ID3D11DeviceContext.PSSetShader
title: ID3D11DeviceContext::PSSetShader (d3d11.h)
description: Sets a pixel shader to the device. (ID3D11DeviceContext.PSSetShader)
helpviewer_keywords: ["4cf3d515-f3f8-76b0-407a-e411a6589c75","ID3D11DeviceContext interface [Direct3D 11]","PSSetShader method","ID3D11DeviceContext.PSSetShader","ID3D11DeviceContext::PSSetShader","PSSetShader","PSSetShader method [Direct3D 11]","PSSetShader method [Direct3D 11]","ID3D11DeviceContext interface","d3d11/ID3D11DeviceContext::PSSetShader","direct3d11.id3d11devicecontext_pssetshader"]
old-location: direct3d11\id3d11devicecontext_pssetshader.htm
tech.root: direct3d11
ms.assetid: 2ee5c946-10bd-40b0-90b2-015aff2377aa
ms.date: 12/05/2018
ms.keywords: 4cf3d515-f3f8-76b0-407a-e411a6589c75, ID3D11DeviceContext interface [Direct3D 11],PSSetShader method, ID3D11DeviceContext.PSSetShader, ID3D11DeviceContext::PSSetShader, PSSetShader, PSSetShader method [Direct3D 11], PSSetShader method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::PSSetShader, direct3d11.id3d11devicecontext_pssetshader
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
 - ID3D11DeviceContext::PSSetShader
 - d3d11/ID3D11DeviceContext::PSSetShader
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
 - ID3D11DeviceContext.PSSetShader
---

# ID3D11DeviceContext::PSSetShader


## -description

Sets a pixel shader to the device.

## -parameters

### -param pPixelShader [in, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11pixelshader">ID3D11PixelShader</a>*</b>

Pointer to a pixel shader (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11pixelshader">ID3D11PixelShader</a>). Passing in <b>NULL</b> disables the shader for this pipeline stage.

### -param ppClassInstances [in, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classinstance">ID3D11ClassInstance</a>*</b>

A pointer to an array of class-instance interfaces (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classinstance">ID3D11ClassInstance</a>). Each interface used by a shader must have a corresponding class instance or the shader will get disabled. Set ppClassInstances to <b>NULL</b> if the shader does not use any interfaces.

### -param NumClassInstances

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of class-instance interfaces in the array.

## -remarks

The method will hold a reference to the interfaces passed in.
          This differs from the device state behavior in Direct3D 10.
        

The maximum number of instances a shader can have is 256.

Set ppClassInstances to <b>NULL</b> if no interfaces are used in the shader. If it is not <b>NULL</b>, the number of class instances must match the number of interfaces used in the shader. Furthermore, each interface pointer must have a corresponding class instance or the assigned shader will be disabled.
        

<b>Windows Phone 8:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
