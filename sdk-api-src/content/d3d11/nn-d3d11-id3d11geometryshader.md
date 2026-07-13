---
UID: NN:d3d11.ID3D11GeometryShader
title: ID3D11GeometryShader (d3d11.h)
description: A geometry-shader interface manages an executable program (a geometry shader) that controls the geometry-shader stage. (ID3D11GeometryShader)
helpviewer_keywords: ["71a86899-19ac-ddc3-70b4-f68cdd6422d0","ID3D11GeometryShader","ID3D11GeometryShader interface [Direct3D 11]","ID3D11GeometryShader interface [Direct3D 11]","described","d3d11/ID3D11GeometryShader","direct3d11.id3d11geometryshader"]
old-location: direct3d11\id3d11geometryshader.htm
tech.root: direct3d11
ms.assetid: c2b5863d-5773-4719-b1d0-2026f55fcef3
ms.date: 12/05/2018
ms.keywords: 71a86899-19ac-ddc3-70b4-f68cdd6422d0, ID3D11GeometryShader, ID3D11GeometryShader interface [Direct3D 11], ID3D11GeometryShader interface [Direct3D 11],described, d3d11/ID3D11GeometryShader, direct3d11.id3d11geometryshader
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
 - ID3D11GeometryShader
 - d3d11/ID3D11GeometryShader
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
 - ID3D11GeometryShader
---

# ID3D11GeometryShader interface


## -description

A geometry-shader interface manages an executable program (a geometry shader) that controls the geometry-shader stage.

## -remarks

The geometry-shader interface has no methods; use HLSL to implement your shader functionality. All shaders are implemented from a common set of features referred to as the common-shader core..

To create a geometry shader interface, call either <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-creategeometryshader">ID3D11Device::CreateGeometryShader</a> or <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput">ID3D11Device::CreateGeometryShaderWithStreamOutput</a>. Before using a geometry shader you must bind it to the device by calling <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-gssetshader">ID3D11DeviceContext::GSSetShader</a>.

This interface is defined in D3D11.h.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-shader-interfaces">Shader Interfaces</a>
