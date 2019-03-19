---
UID: NN:d3d11.ID3D11PixelShader
title: ID3D11PixelShader (d3d11.h)
author: windows-sdk-content
description: A pixel-shader interface manages an executable program (a pixel shader) that controls the pixel-shader stage.
old-location: direct3d11\id3d11pixelshader.htm
tech.root: direct3d11
ms.assetid: d16e00a9-02f9-413f-b9f7-31446fb0a692
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 49390d89-6546-de4c-d03d-c7914ecb86eb, ID3D11PixelShader, ID3D11PixelShader interface [Direct3D 11], ID3D11PixelShader interface [Direct3D 11],described, d3d11/ID3D11PixelShader, direct3d11.id3d11pixelshader
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11PixelShader interface


## -description


A pixel-shader interface manages an executable program (a pixel shader) that controls the pixel-shader stage.


## -remarks



The pixel-shader interface has no methods; use HLSL to implement your shader functionality. All shaders in are implemented from a common set of features referred to as the common-shader core..

To create a pixel shader interface, call <a href="https://msdn.microsoft.com/f013a648-fd11-417b-8f87-36a4be901715">ID3D11Device::CreatePixelShader</a>. Before using a pixel shader you must bind it to the device by calling <a href="https://msdn.microsoft.com/2ee5c946-10bd-40b0-90b2-015aff2377aa">ID3D11DeviceContext::PSSetShader</a>.

This interface is defined in D3D11.h.




## -see-also




<a href="https://msdn.microsoft.com/bed17239-0358-4768-8655-9a1d92f25a2e">ID3D11DeviceChild</a>



<a href="https://msdn.microsoft.com/1791d2c9-3791-47fe-b887-a8117ecc798b">Shader Interfaces</a>
 

 

