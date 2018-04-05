---
UID: NN:d3d10.ID3D10VertexShader
title: ID3D10VertexShader
author: windows-driver-content
description: A vertex-shader interface manages an executable program (a vertex shader) that controls the vertex-shader stage.
old-location: direct3d10\id3d10vertexshader.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10vertexshader.htm
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: 1037a0d0-ff92-5834-5b3b-282125a9ccca, ID3D10VertexShader, ID3D10VertexShader interface [Direct3D 10], ID3D10VertexShader interface [Direct3D 10], described, d3d10/ID3D10VertexShader, direct3d10.id3d10vertexshader
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
req.typenames: D3D10_USAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10.lib
-	D3D10.dll
api_name:
-	ID3D10VertexShader
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10VertexShader interface


## -description


A vertex-shader interface manages an executable program (a vertex shader) that controls the <a href="direct3d10.d3d10_graphics_programming_guide_shader_stages">vertex-shader stage</a>.


## -remarks



The vertex-shader interface has no methods; use HLSL to implement your shader functionality. All shaders in Direct3D 10 are implemented from a common set of features referred to as the <a href="https://msdn.microsoft.com/f3cf2969-83a4-461f-8177-d336536194ba">common shader core</a>.

To create a vertex shader interface, call <a href="https://msdn.microsoft.com/a7449878-b0a7-44b6-acbc-172449523098">ID3D10Device::CreateVertexShader</a>. Before using a vertex shader you must bind it to the device by calling <a href="https://msdn.microsoft.com/9ebc673d-d3e0-4678-8c6e-b11fb75e1ed1">ID3D10Device::VSSetShader</a>.

This interface is defined in D3D10.h.




## -see-also




<a href="https://msdn.microsoft.com/64eff938-e130-48be-a45f-43f6c885b588">ID3D10DeviceChild</a>



<a href="https://msdn.microsoft.com/d8770b45-a05c-4dd8-9fa7-08fb4330d734">Shader Interfaces</a>
 

 

