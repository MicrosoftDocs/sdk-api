---
UID: NN:d3d11.ID3D11VertexShader
title: ID3D11VertexShader (d3d11.h)
author: windows-sdk-content
description: A vertex-shader interface manages an executable program (a vertex shader) that controls the vertex-shader stage.
old-location: direct3d11\id3d11vertexshader.htm
tech.root: direct3d11
ms.assetid: 8300ec12-ecf5-49c2-9313-b542a7d971f3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D11VertexShader, ID3D11VertexShader interface [Direct3D 11], ID3D11VertexShader interface [Direct3D 11],described, b9c949e5-8c3e-0e31-c320-230e1c67dfaf, d3d11/ID3D11VertexShader, direct3d11.id3d11vertexshader
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
 - ID3D11VertexShader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VertexShader interface


## -description


A vertex-shader interface manages an executable program (a vertex shader) that controls the vertex-shader stage.


## -remarks



The vertex-shader interface has no methods; use HLSL to implement your shader functionality. All shaders are implemented from a common set of features referred to as the common-shader core..

To create a vertex shader interface, call <a href="https://msdn.microsoft.com/06e5105a-ff7e-430a-ab9a-2aefb161894c">ID3D11Device::CreateVertexShader</a>. Before using a vertex shader you must bind it to the device by calling <a href="https://msdn.microsoft.com/d6207779-7477-4e74-beb8-065949abce06">ID3D11DeviceContext::VSSetShader</a>.

This interface is defined in D3D11.h.




## -see-also




<a href="https://msdn.microsoft.com/bed17239-0358-4768-8655-9a1d92f25a2e">ID3D11DeviceChild</a>



<a href="https://msdn.microsoft.com/1791d2c9-3791-47fe-b887-a8117ecc798b">Shader Interfaces</a>
 

 

