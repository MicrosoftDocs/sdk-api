---
UID: NN:d3d10.ID3D10GeometryShader
title: ID3D10GeometryShader (d3d10.h)
author: windows-sdk-content
description: A geometry-shader interface manages an executable program (a geometry shader) that controls the geometry-shader stage.
old-location: direct3d10\id3d10geometryshader.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10geometryshader.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 0dcf2957-f913-22f8-e1fe-0085a1e9dce8, ID3D10GeometryShader, ID3D10GeometryShader interface [Direct3D 10], ID3D10GeometryShader interface [Direct3D 10],described, d3d10/ID3D10GeometryShader, direct3d10.id3d10geometryshader
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
 - ID3D10GeometryShader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10GeometryShader interface


## -description


A geometry-shader interface manages an executable program (a geometry shader) that controls the <a href="https://msdn.microsoft.com/library/Bb205146(v=VS.85).aspx">geometry-shader stage</a>.


## -remarks



The geometry-shader interface has no methods; use HLSL to implement your shader functionality. All shaders in Direct3D 10 are implemented from a common set of features referred to as the <a href="https://msdn.microsoft.com/en-us/library/Bb509580(v=VS.85).aspx">common shader core</a>.

To create a geometry shader interface, call either <a href="https://msdn.microsoft.com/en-us/library/Bb173548(v=VS.85).aspx">ID3D10Device::CreateGeometryShader</a> or <a href="https://msdn.microsoft.com/en-us/library/Bb173549(v=VS.85).aspx">ID3D10Device::CreateGeometryShaderWithStreamOutput</a>. Before using a geometry shader you must bind it to the device by calling <a href="https://msdn.microsoft.com/en-us/library/Bb173582(v=VS.85).aspx">ID3D10Device::GSSetShader</a>.

This interface is defined in D3D10.h.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173529(v=VS.85).aspx">ID3D10DeviceChild</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb205158(v=VS.85).aspx">Shader Interfaces</a>
 

 

