---
UID: NN:d3d10.ID3D10GeometryShader
title: ID3D10GeometryShader (d3d10.h)
description: A geometry-shader interface manages an executable program (a geometry shader) that controls the geometry-shader stage. (ID3D10GeometryShader)
helpviewer_keywords: ["0dcf2957-f913-22f8-e1fe-0085a1e9dce8","ID3D10GeometryShader","ID3D10GeometryShader interface [Direct3D 10]","ID3D10GeometryShader interface [Direct3D 10]","described","d3d10/ID3D10GeometryShader","direct3d10.id3d10geometryshader"]
old-location: direct3d10\id3d10geometryshader.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10geometryshader.htm
ms.date: 12/05/2018
ms.keywords: 0dcf2957-f913-22f8-e1fe-0085a1e9dce8, ID3D10GeometryShader, ID3D10GeometryShader interface [Direct3D 10], ID3D10GeometryShader interface [Direct3D 10],described, d3d10/ID3D10GeometryShader, direct3d10.id3d10geometryshader
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
 - ID3D10GeometryShader
 - d3d10/ID3D10GeometryShader
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
 - ID3D10GeometryShader
---

# ID3D10GeometryShader interface


## -description

A geometry-shader interface manages an executable program (a geometry shader) that controls the <a href="/previous-versions/bb205146(v=vs.85)">geometry-shader stage</a>.

## -remarks

The geometry-shader interface has no methods; use HLSL to implement your shader functionality. All shaders in Direct3D 10 are implemented from a common set of features referred to as the <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-common-core">common shader core</a>.

To create a geometry shader interface, call either <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-creategeometryshader">ID3D10Device::CreateGeometryShader</a> or <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-creategeometryshaderwithstreamoutput">ID3D10Device::CreateGeometryShaderWithStreamOutput</a>. Before using a geometry shader you must bind it to the device by calling <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetshader">ID3D10Device::GSSetShader</a>.

This interface is defined in D3D10.h.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10devicechild">ID3D10DeviceChild</a>



<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-interfaces">Shader Interfaces</a>
