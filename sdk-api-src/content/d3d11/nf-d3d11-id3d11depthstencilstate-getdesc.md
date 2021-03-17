---
UID: NF:d3d11.ID3D11DepthStencilState.GetDesc
title: ID3D11DepthStencilState::GetDesc (d3d11.h)
description: Gets the description for depth-stencil state that you used to create the depth-stencil-state object.
helpviewer_keywords: ["GetDesc","GetDesc method [Direct3D 11]","GetDesc method [Direct3D 11]","ID3D11DepthStencilState interface","ID3D11DepthStencilState interface [Direct3D 11]","GetDesc method","ID3D11DepthStencilState.GetDesc","ID3D11DepthStencilState::GetDesc","b5b2c6e1-1315-e15e-9d66-a15b16d828aa","d3d11/ID3D11DepthStencilState::GetDesc","direct3d11.id3d11depthstencilstate_getdesc"]
old-location: direct3d11\id3d11depthstencilstate_getdesc.htm
tech.root: direct3d11
ms.assetid: f83ee1cf-b435-4c10-afb6-916307c420f9
ms.date: 12/05/2018
ms.keywords: GetDesc, GetDesc method [Direct3D 11], GetDesc method [Direct3D 11],ID3D11DepthStencilState interface, ID3D11DepthStencilState interface [Direct3D 11],GetDesc method, ID3D11DepthStencilState.GetDesc, ID3D11DepthStencilState::GetDesc, b5b2c6e1-1315-e15e-9d66-a15b16d828aa, d3d11/ID3D11DepthStencilState::GetDesc, direct3d11.id3d11depthstencilstate_getdesc
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
 - ID3D11DepthStencilState::GetDesc
 - d3d11/ID3D11DepthStencilState::GetDesc
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
 - ID3D11DepthStencilState.GetDesc
---

# ID3D11DepthStencilState::GetDesc


## -description

Gets the description for depth-stencil state that you used to create the depth-stencil-state object.

## -parameters

### -param pDesc [out]

Type: <b><a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_depth_stencil_desc">D3D11_DEPTH_STENCIL_DESC</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_depth_stencil_desc">D3D11_DEPTH_STENCIL_DESC</a> structure that receives a description of the depth-stencil state.

## -remarks

You use the description for depth-stencil state in a call to the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createdepthstencilstate">ID3D11Device::CreateDepthStencilState</a> method to create the depth-stencil-state object.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilstate">ID3D11DepthStencilState</a>