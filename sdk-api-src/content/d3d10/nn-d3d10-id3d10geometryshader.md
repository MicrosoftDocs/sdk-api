---
UID: NN:d3d10.ID3D10GeometryShader
title: ID3D10GeometryShader
author: windows-driver-content
description: A geometry-shader interface manages an executable program (a geometry shader) that controls the geometry-shader stage.
old-location: direct3d10\id3d10geometryshader.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10geometryshader.htm
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: 0dcf2957-f913-22f8-e1fe-0085a1e9dce8, ID3D10GeometryShader, ID3D10GeometryShader interface [Direct3D 10], ID3D10GeometryShader interface [Direct3D 10], described, d3d10/ID3D10GeometryShader, direct3d10.id3d10geometryshader
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
-	ID3D10GeometryShader
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10GeometryShader interface


## -description


A geometry-shader interface manages an executable program (a geometry shader) that controls the <a href="direct3d10.d3d10_graphics_programming_guide_shader_stages">geometry-shader stage</a>.


## -remarks



The geometry-shader interface has no methods; use HLSL to implement your shader functionality. All shaders in Direct3D 10 are implemented from a common set of features referred to as the <a href="https://msdn.microsoft.com/f3cf2969-83a4-461f-8177-d336536194ba">common shader core</a>.

To create a geometry shader interface, call either <a href="https://msdn.microsoft.com/6202ed81-a599-497f-a271-940f5605fb84">ID3D10Device::CreateGeometryShader</a> or <a href="https://msdn.microsoft.com/f4e99b74-032b-4ae2-88d1-f0837cdbcbfb">ID3D10Device::CreateGeometryShaderWithStreamOutput</a>. Before using a geometry shader you must bind it to the device by calling <a href="https://msdn.microsoft.com/cd591f9d-dd17-48e3-b952-9f38c7572b93">ID3D10Device::GSSetShader</a>.

This interface is defined in D3D10.h.




## -see-also




<a href="https://msdn.microsoft.com/64eff938-e130-48be-a45f-43f6c885b588">ID3D10DeviceChild</a>



<a href="https://msdn.microsoft.com/d8770b45-a05c-4dd8-9fa7-08fb4330d734">Shader Interfaces</a>
 

 

