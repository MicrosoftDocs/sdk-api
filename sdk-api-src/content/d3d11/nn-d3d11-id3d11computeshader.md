---
UID: NN:d3d11.ID3D11ComputeShader
title: ID3D11ComputeShader (d3d11.h)
description: A compute-shader interface manages an executable program (a compute shader) that controls the compute-shader stage.
helpviewer_keywords: ["ID3D11ComputeShader","ID3D11ComputeShader interface [Direct3D 11]","ID3D11ComputeShader interface [Direct3D 11]","described","d3d11/ID3D11ComputeShader","dde07f60-78d4-2f2f-10da-d2a2973a909c","direct3d11.id3d11computeshader"]
old-location: direct3d11\id3d11computeshader.htm
tech.root: direct3d11
ms.assetid: 33a43253-ada2-4085-9401-e84562b37d59
ms.date: 12/05/2018
ms.keywords: ID3D11ComputeShader, ID3D11ComputeShader interface [Direct3D 11], ID3D11ComputeShader interface [Direct3D 11],described, d3d11/ID3D11ComputeShader, dde07f60-78d4-2f2f-10da-d2a2973a909c, direct3d11.id3d11computeshader
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
 - ID3D11ComputeShader
 - d3d11/ID3D11ComputeShader
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
 - ID3D11ComputeShader
---

# ID3D11ComputeShader interface


## -description

A compute-shader interface manages an executable program (a compute shader) that controls the compute-shader stage.

## -remarks

The compute-shader interface has no methods; use HLSL to implement your shader functionality. All shaders are implemented from a common set of features referred to as the common-shader core..

To create a compute-shader interface, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createcomputeshader">ID3D11Device::CreateComputeShader</a>. Before using a compute shader you must bind it to the device by calling <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-cssetshader">ID3D11DeviceContext::CSSetShader</a>.

This interface is defined in D3D11.h.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-shader-interfaces">Shader Interfaces</a>