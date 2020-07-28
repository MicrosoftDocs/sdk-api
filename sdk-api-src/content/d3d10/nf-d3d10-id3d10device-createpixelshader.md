---
UID: NF:d3d10.ID3D10Device.CreatePixelShader
title: ID3D10Device::CreatePixelShader (d3d10.h)
description: Create a pixel shader.
helpviewer_keywords: ["CreatePixelShader","CreatePixelShader method [Direct3D 10]","CreatePixelShader method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","CreatePixelShader method","ID3D10Device.CreatePixelShader","ID3D10Device::CreatePixelShader","d3d10/ID3D10Device::CreatePixelShader","direct3d10.id3d10device_createpixelshader","eaddd998-99a2-ab8d-51dd-98d72c93e291"]
old-location: direct3d10\id3d10device_createpixelshader.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_createpixelshader.htm
ms.date: 12/05/2018
ms.keywords: CreatePixelShader, CreatePixelShader method [Direct3D 10], CreatePixelShader method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CreatePixelShader method, ID3D10Device.CreatePixelShader, ID3D10Device::CreatePixelShader, d3d10/ID3D10Device::CreatePixelShader, direct3d10.id3d10device_createpixelshader, eaddd998-99a2-ab8d-51dd-98d72c93e291
f1_keywords:
- d3d10/ID3D10Device.CreatePixelShader
dev_langs:
- c++
req.header: d3d10.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D3D10.lib
- D3D10.dll
api_name:
- ID3D10Device.CreatePixelShader
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10Device::CreatePixelShader


## -description


Create a pixel shader.


## -parameters




### -param pShaderBytecode [in]

Type: <b>const void*</b>

A pointer to the compiled shader. To get this pointer see <a href="https://docs.microsoft.com/windows/desktop/direct3dhlsl/dx-graphics-hlsl-using-shaders-10">Getting a Pointer to a Compiled Shader</a>.


### -param BytecodeLength [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

Size of the compiled pixel shader.


### -param ppPixelShader [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10pixelshader">ID3D10PixelShader</a>**</b>

Address of a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10pixelshader">ID3D10PixelShader Interface</a>. If this is <b>NULL</b>, all other parameters will be validated, and if all parameters pass validation this API will return S_FALSE instead of S_OK.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.




## -remarks



After creating the pixel shader, you can set it to the device using <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetshader">ID3D10Device::PSSetShader</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
 

 

