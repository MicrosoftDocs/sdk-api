---
UID: NN:d3d11.ID3D11SamplerState
title: ID3D11SamplerState (d3d11.h)
description: The sampler-state interface holds a description for sampler state that you can bind to any shader stage of the pipeline for reference by texture sample operations.
helpviewer_keywords: ["10df1118-2f5f-fe2c-97bb-9adf4d72bc25","ID3D11SamplerState","ID3D11SamplerState interface [Direct3D 11]","ID3D11SamplerState interface [Direct3D 11]","described","d3d11/ID3D11SamplerState","direct3d11.id3d11samplerstate"]
old-location: direct3d11\id3d11samplerstate.htm
tech.root: direct3d11
ms.assetid: 8dc2facc-4f51-4064-aab4-028a06b9d7e6
ms.date: 12/05/2018
ms.keywords: 10df1118-2f5f-fe2c-97bb-9adf4d72bc25, ID3D11SamplerState, ID3D11SamplerState interface [Direct3D 11], ID3D11SamplerState interface [Direct3D 11],described, d3d11/ID3D11SamplerState, direct3d11.id3d11samplerstate
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
 - ID3D11SamplerState
 - d3d11/ID3D11SamplerState
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
 - ID3D11SamplerState
---

# ID3D11SamplerState interface


## -description

The sampler-state interface holds a description for sampler state that you can bind to any shader stage of the <a href="/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline">pipeline</a> for reference by texture sample operations.

## -inheritance

The <b>ID3D11SamplerState</b> interface inherits from <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>. <b>ID3D11SamplerState</b> also has these types of members:

## -remarks

To create a sampler-state object, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createsamplerstate">ID3D11Device::CreateSamplerState</a>.

To bind a sampler-state object to any <a href="/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline">pipeline</a> shader stage, call the following methods:

<ul>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetsamplers">ID3D11DeviceContext::VSSetSamplers</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-hssetsamplers">ID3D11DeviceContext::HSSetSamplers</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dssetsamplers">ID3D11DeviceContext::DSSetSamplers</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-gssetsamplers">ID3D11DeviceContext::GSSetSamplers</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetsamplers">ID3D11DeviceContext::PSSetSamplers</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-cssetsamplers">ID3D11DeviceContext::CSSetSamplers</a>
</li>
</ul>
You can bind the same sampler-state object to multiple shader stages simultaneously.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-interfaces">Core Interfaces</a>



<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>
