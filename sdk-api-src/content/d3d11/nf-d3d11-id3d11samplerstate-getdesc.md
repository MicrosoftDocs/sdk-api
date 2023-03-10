---
UID: NF:d3d11.ID3D11SamplerState.GetDesc
title: ID3D11SamplerState::GetDesc (d3d11.h)
description: Gets the description for sampler state that you used to create the sampler-state object.
helpviewer_keywords: ["3558faeb-2890-903a-fe84-4afdeb705f2b","GetDesc","GetDesc method [Direct3D 11]","GetDesc method [Direct3D 11]","ID3D11SamplerState interface","ID3D11SamplerState interface [Direct3D 11]","GetDesc method","ID3D11SamplerState.GetDesc","ID3D11SamplerState::GetDesc","d3d11/ID3D11SamplerState::GetDesc","direct3d11.id3d11samplerstate_getdesc"]
old-location: direct3d11\id3d11samplerstate_getdesc.htm
tech.root: direct3d11
ms.assetid: cca7f0f1-44b7-4f49-9149-acb12d745890
ms.date: 12/05/2018
ms.keywords: 3558faeb-2890-903a-fe84-4afdeb705f2b, GetDesc, GetDesc method [Direct3D 11], GetDesc method [Direct3D 11],ID3D11SamplerState interface, ID3D11SamplerState interface [Direct3D 11],GetDesc method, ID3D11SamplerState.GetDesc, ID3D11SamplerState::GetDesc, d3d11/ID3D11SamplerState::GetDesc, direct3d11.id3d11samplerstate_getdesc
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11SamplerState::GetDesc
 - d3d11/ID3D11SamplerState::GetDesc
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
 - ID3D11SamplerState.GetDesc
---

# ID3D11SamplerState::GetDesc


## -description

Gets the description for sampler state that you used to create the sampler-state object.

## -parameters

### -param pDesc [out]

Type: <b><a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_sampler_desc">D3D11_SAMPLER_DESC</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_sampler_desc">D3D11_SAMPLER_DESC</a> structure that receives a description of the sampler state.

## -remarks

You use the description for sampler state in a call to the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createsamplerstate">ID3D11Device::CreateSamplerState</a> method to create the sampler-state object.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11samplerstate">ID3D11SamplerState</a>