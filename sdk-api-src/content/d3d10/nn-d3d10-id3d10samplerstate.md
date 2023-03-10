---
UID: NN:d3d10.ID3D10SamplerState
title: ID3D10SamplerState (d3d10.h)
description: A sampler-state interface accesses sampler state for a texture.
helpviewer_keywords: ["2116312d-356e-9f01-4cdf-78e47d9a4ae8","ID3D10SamplerState","ID3D10SamplerState interface [Direct3D 10]","ID3D10SamplerState interface [Direct3D 10]","described","d3d10/ID3D10SamplerState","direct3d10.id3d10samplerstate"]
old-location: direct3d10\id3d10samplerstate.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10samplerstate.htm
ms.date: 12/05/2018
ms.keywords: 2116312d-356e-9f01-4cdf-78e47d9a4ae8, ID3D10SamplerState, ID3D10SamplerState interface [Direct3D 10], ID3D10SamplerState interface [Direct3D 10],described, d3d10/ID3D10SamplerState, direct3d10.id3d10samplerstate
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
 - ID3D10SamplerState
 - d3d10/ID3D10SamplerState
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
 - ID3D10SamplerState
---

# ID3D10SamplerState interface


## -description

A sampler-state interface accesses sampler state for a <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-type">texture</a>.

## -inheritance

The <b>ID3D10SamplerState</b> interface inherits from <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10devicechild">ID3D10DeviceChild</a>. <b>ID3D10SamplerState</b> also has these types of members:

## -remarks

Create a sampler-state object by calling <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createsamplerstate">ID3D10Device::CreateSamplerState</a>.

To initialize sampler state, bind the sampler-state object to the pipeline by calling <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetsamplers">ID3D10Device::VSSetSamplers</a>, <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetsamplers">ID3D10Device::GSSetSamplers</a>, or <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetsamplers">ID3D10Device::PSSetSamplers</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-interfaces">Core Interfaces</a>



<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core">Core Reference</a>



<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10devicechild">ID3D10DeviceChild</a>
