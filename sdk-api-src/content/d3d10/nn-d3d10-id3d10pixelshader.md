---
UID: NN:d3d10.ID3D10PixelShader
title: ID3D10PixelShader
author: windows-sdk-content
description: A pixel-shader interface manages an executable program (a pixel shader) that controls the pixel-shader stage.
old-location: direct3d10\id3d10pixelshader.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10pixelshader.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D10PixelShader, ID3D10PixelShader interface [Direct3D 10], ID3D10PixelShader interface [Direct3D 10],described, af8a1f54-5d9a-91f5-ed3f-377a9ad029d2, d3d10/ID3D10PixelShader, direct3d10.id3d10pixelshader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - ID3D10PixelShader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10PixelShader interface


## -description


A pixel-shader interface manages an executable program (a pixel shader) that controls the <a href="direct3d10.d3d10_graphics_programming_guide_shader_stages">pixel-shader stage</a>.


## -remarks



The pixel-shader interface has no methods; use HLSL to implement your shader functionality. All shaders in Direct3D 10 are implemented from a common set of features referred to as the <a href="https://msdn.microsoft.com/f3cf2969-83a4-461f-8177-d336536194ba">common shader core</a>.

To create a pixel shader interface, call <a href="https://msdn.microsoft.com/85dfc580-1231-413d-8cc1-6bfd9e0eec68">ID3D10Device::CreatePixelShader</a>. Before using a pixel shader you must bind it to the device by calling <a href="https://msdn.microsoft.com/8e7cf7fb-e2c0-4524-a909-5592decd9a66">ID3D10Device::PSSetShader</a>.

This interface is defined in D3D10.h.




## -see-also




<a href="https://msdn.microsoft.com/64eff938-e130-48be-a45f-43f6c885b588">ID3D10DeviceChild</a>



<a href="https://msdn.microsoft.com/d8770b45-a05c-4dd8-9fa7-08fb4330d734">Shader Interfaces</a>
 

 

