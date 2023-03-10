---
UID: NN:d3d10.ID3D10VertexShader
title: ID3D10VertexShader (d3d10.h)
description: A vertex-shader interface manages an executable program (a vertex shader) that controls the vertex-shader stage. (ID3D10VertexShader)
helpviewer_keywords: ["1037a0d0-ff92-5834-5b3b-282125a9ccca","ID3D10VertexShader","ID3D10VertexShader interface [Direct3D 10]","ID3D10VertexShader interface [Direct3D 10]","described","d3d10/ID3D10VertexShader","direct3d10.id3d10vertexshader"]
old-location: direct3d10\id3d10vertexshader.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10vertexshader.htm
ms.date: 12/05/2018
ms.keywords: 1037a0d0-ff92-5834-5b3b-282125a9ccca, ID3D10VertexShader, ID3D10VertexShader interface [Direct3D 10], ID3D10VertexShader interface [Direct3D 10],described, d3d10/ID3D10VertexShader, direct3d10.id3d10vertexshader
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10VertexShader
 - d3d10/ID3D10VertexShader
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10VertexShader
---

# ID3D10VertexShader interface


## -description

A vertex-shader interface manages an executable program (a vertex shader) that controls the <a href="/previous-versions/bb205146(v=vs.85)">vertex-shader stage</a>.

## -remarks

The vertex-shader interface has no methods; use HLSL to implement your shader functionality. All shaders in Direct3D 10 are implemented from a common set of features referred to as the <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-common-core">common shader core</a>.

To create a vertex shader interface, call <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createvertexshader">ID3D10Device::CreateVertexShader</a>. Before using a vertex shader you must bind it to the device by calling <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetshader">ID3D10Device::VSSetShader</a>.

This interface is defined in D3D10.h.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10devicechild">ID3D10DeviceChild</a>



<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-interfaces">Shader Interfaces</a>
