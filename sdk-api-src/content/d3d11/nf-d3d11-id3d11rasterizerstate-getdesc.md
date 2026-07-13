---
UID: NF:d3d11.ID3D11RasterizerState.GetDesc
title: ID3D11RasterizerState::GetDesc (d3d11.h)
description: Gets the description for rasterizer state that you used to create the rasterizer-state object. (ID3D11RasterizerState.GetDesc)
helpviewer_keywords: ["GetDesc","GetDesc method [Direct3D 11]","GetDesc method [Direct3D 11]","ID3D11RasterizerState interface","ID3D11RasterizerState interface [Direct3D 11]","GetDesc method","ID3D11RasterizerState.GetDesc","ID3D11RasterizerState::GetDesc","ce48f8a7-2b79-44f8-93db-80cad9b1ca3b","d3d11/ID3D11RasterizerState::GetDesc","direct3d11.id3d11rasterizerstate_getdesc"]
old-location: direct3d11\id3d11rasterizerstate_getdesc.htm
tech.root: direct3d11
ms.assetid: cc6bbdd2-af9c-45be-a13a-5f9105f08c99
ms.date: 12/05/2018
ms.keywords: GetDesc, GetDesc method [Direct3D 11], GetDesc method [Direct3D 11],ID3D11RasterizerState interface, ID3D11RasterizerState interface [Direct3D 11],GetDesc method, ID3D11RasterizerState.GetDesc, ID3D11RasterizerState::GetDesc, ce48f8a7-2b79-44f8-93db-80cad9b1ca3b, d3d11/ID3D11RasterizerState::GetDesc, direct3d11.id3d11rasterizerstate_getdesc
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
 - ID3D11RasterizerState::GetDesc
 - d3d11/ID3D11RasterizerState::GetDesc
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
 - ID3D11RasterizerState.GetDesc
---

# ID3D11RasterizerState::GetDesc


## -description

Gets the description for rasterizer state that you used to create the rasterizer-state object.

## -parameters

### -param pDesc [out]

Type: <b><a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_rasterizer_desc">D3D11_RASTERIZER_DESC</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_rasterizer_desc">D3D11_RASTERIZER_DESC</a> structure that receives a description of the rasterizer state.

## -remarks

You use the description for rasterizer state in a call to the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createrasterizerstate">ID3D11Device::CreateRasterizerState</a> method to create the rasterizer-state object.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11rasterizerstate">ID3D11RasterizerState</a>
