---
UID: NN:d3d11.ID3D11PixelShader
title: ID3D11PixelShader (d3d11.h)
description: A pixel-shader interface manages an executable program (a pixel shader) that controls the pixel-shader stage. (ID3D11PixelShader)
helpviewer_keywords: ["49390d89-6546-de4c-d03d-c7914ecb86eb","ID3D11PixelShader","ID3D11PixelShader interface [Direct3D 11]","ID3D11PixelShader interface [Direct3D 11]","described","d3d11/ID3D11PixelShader","direct3d11.id3d11pixelshader"]
old-location: direct3d11\id3d11pixelshader.htm
tech.root: direct3d11
ms.assetid: d16e00a9-02f9-413f-b9f7-31446fb0a692
ms.date: 12/05/2018
ms.keywords: 49390d89-6546-de4c-d03d-c7914ecb86eb, ID3D11PixelShader, ID3D11PixelShader interface [Direct3D 11], ID3D11PixelShader interface [Direct3D 11],described, d3d11/ID3D11PixelShader, direct3d11.id3d11pixelshader
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - ID3D11PixelShader
 - d3d11/ID3D11PixelShader
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
 - ID3D11PixelShader
---

# ID3D11PixelShader interface


## -description

A pixel-shader interface manages an executable program (a pixel shader) that controls the pixel-shader stage.

## -remarks

The pixel-shader interface has no methods; use HLSL to implement your shader functionality. All shaders in are implemented from a common set of features referred to as the common-shader core..

To create a pixel shader interface, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader">ID3D11Device::CreatePixelShader</a>. Before using a pixel shader you must bind it to the device by calling <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshader">ID3D11DeviceContext::PSSetShader</a>.

This interface is defined in D3D11.h.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-shader-interfaces">Shader Interfaces</a>
