---
UID: NF:d3d11.ID3D11BlendState.GetDesc
title: ID3D11BlendState::GetDesc (d3d11.h)
description: Gets the description for blending state that you used to create the blend-state object. (ID3D11BlendState.GetDesc)
helpviewer_keywords: ["1228cbef-e4a2-9952-d96f-5f2e44ceaee0","GetDesc","GetDesc method [Direct3D 11]","GetDesc method [Direct3D 11]","ID3D11BlendState interface","ID3D11BlendState interface [Direct3D 11]","GetDesc method","ID3D11BlendState.GetDesc","ID3D11BlendState::GetDesc","d3d11/ID3D11BlendState::GetDesc","direct3d11.id3d11blendstate_getdesc"]
old-location: direct3d11\id3d11blendstate_getdesc.htm
tech.root: direct3d11
ms.assetid: f7330e53-78cd-42f9-9fc9-f61fce011b06
ms.date: 12/05/2018
ms.keywords: 1228cbef-e4a2-9952-d96f-5f2e44ceaee0, GetDesc, GetDesc method [Direct3D 11], GetDesc method [Direct3D 11],ID3D11BlendState interface, ID3D11BlendState interface [Direct3D 11],GetDesc method, ID3D11BlendState.GetDesc, ID3D11BlendState::GetDesc, d3d11/ID3D11BlendState::GetDesc, direct3d11.id3d11blendstate_getdesc
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
 - ID3D11BlendState::GetDesc
 - d3d11/ID3D11BlendState::GetDesc
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
 - ID3D11BlendState.GetDesc
---

# ID3D11BlendState::GetDesc


## -description

Gets the description for blending state that you used to create the blend-state object.

## -parameters

### -param pDesc [out]

Type: <b><a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_blend_desc">D3D11_BLEND_DESC</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_blend_desc">D3D11_BLEND_DESC</a> structure that receives a description of the blend state.

## -remarks

You use the description for blending state in a call to the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createblendstate">ID3D11Device::CreateBlendState</a> method to create the blend-state object.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11blendstate">ID3D11BlendState</a>
