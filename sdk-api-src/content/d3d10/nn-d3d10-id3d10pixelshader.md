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


A pixel-shader interface manages an executable program (a pixel shader) that controls the <a href="https://msdn.microsoft.com/library/Bb205146(v=VS.85).aspx">pixel-shader stage</a>.


## -remarks



The pixel-shader interface has no methods; use HLSL to implement your shader functionality. All shaders in Direct3D 10 are implemented from a common set of features referred to as the <a href="https://msdn.microsoft.com/en-us/library/Bb509580(v=VS.85).aspx">common shader core</a>.

To create a pixel shader interface, call <a href="https://msdn.microsoft.com/en-us/library/Bb173551(v=VS.85).aspx">ID3D10Device::CreatePixelShader</a>. Before using a pixel shader you must bind it to the device by calling <a href="https://msdn.microsoft.com/en-us/library/Bb173605(v=VS.85).aspx">ID3D10Device::PSSetShader</a>.

This interface is defined in D3D10.h.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173529(v=VS.85).aspx">ID3D10DeviceChild</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb205158(v=VS.85).aspx">Shader Interfaces</a>
 

 

