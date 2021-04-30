---
UID: NN:d3d11.ID3D11HullShader
title: ID3D11HullShader (d3d11.h)
description: A hull-shader interface manages an executable program (a hull shader) that controls the hull-shader stage.
helpviewer_keywords: ["47a9bf26-6dd1-87f4-4259-36e6163908d8","ID3D11HullShader","ID3D11HullShader interface [Direct3D 11]","ID3D11HullShader interface [Direct3D 11]","described","d3d11/ID3D11HullShader","direct3d11.id3d11hullshader"]
old-location: direct3d11\id3d11hullshader.htm
tech.root: direct3d11
ms.assetid: 3459f533-e2ac-4b0e-bfdd-d9dae704f418
ms.date: 12/05/2018
ms.keywords: 47a9bf26-6dd1-87f4-4259-36e6163908d8, ID3D11HullShader, ID3D11HullShader interface [Direct3D 11], ID3D11HullShader interface [Direct3D 11],described, d3d11/ID3D11HullShader, direct3d11.id3d11hullshader
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
 - ID3D11HullShader
 - d3d11/ID3D11HullShader
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
 - ID3D11HullShader
---

# ID3D11HullShader interface


## -description

A hull-shader interface manages an executable program (a hull shader) that controls the hull-shader stage.

## -remarks

The hull-shader interface has no methods; use HLSL to implement your shader functionality. All shaders are implemented from a common set of features referred to as the common-shader core..

To create a hull-shader interface, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createhullshader">ID3D11Device::CreateHullShader</a>. Before using a hull shader you must bind it to the device by calling <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-hssetshader">ID3D11DeviceContext::HSSetShader</a>.

This interface is defined in D3D11.h.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-shader-interfaces">Shader Interfaces</a>