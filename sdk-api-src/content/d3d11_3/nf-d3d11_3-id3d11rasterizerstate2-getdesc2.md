---
UID: NF:d3d11_3.ID3D11RasterizerState2.GetDesc2
title: ID3D11RasterizerState2::GetDesc2 (d3d11_3.h)
description: Gets the description for rasterizer state that you used to create the rasterizer-state object. (ID3D11RasterizerState2.GetDesc2)
helpviewer_keywords: ["GetDesc2","GetDesc2 method [Direct3D 11]","GetDesc2 method [Direct3D 11]","ID3D11RasterizerState2 interface","ID3D11RasterizerState2 interface [Direct3D 11]","GetDesc2 method","ID3D11RasterizerState2.GetDesc2","ID3D11RasterizerState2::GetDesc2","d3d11_3/ID3D11RasterizerState2::GetDesc2","direct3d11.id3d11rasterizerstate2_getdesc2"]
old-location: direct3d11\id3d11rasterizerstate2_getdesc2.htm
tech.root: direct3d11
ms.assetid: 23A3BCDF-9D3D-4984-BFA9-E598773DBC44
ms.date: 12/05/2018
ms.keywords: GetDesc2, GetDesc2 method [Direct3D 11], GetDesc2 method [Direct3D 11],ID3D11RasterizerState2 interface, ID3D11RasterizerState2 interface [Direct3D 11],GetDesc2 method, ID3D11RasterizerState2.GetDesc2, ID3D11RasterizerState2::GetDesc2, d3d11_3/ID3D11RasterizerState2::GetDesc2, direct3d11.id3d11rasterizerstate2_getdesc2
req.header: d3d11_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - ID3D11RasterizerState2::GetDesc2
 - d3d11_3/ID3D11RasterizerState2::GetDesc2
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
 - ID3D11RasterizerState2.GetDesc2
---

# ID3D11RasterizerState2::GetDesc2


## -description

Gets the description for rasterizer state that you used to create the rasterizer-state object.

## -parameters

### -param pDesc [out]

A pointer to a <a href="/windows/desktop/api/d3d11_3/ns-d3d11_3-cd3d11_rasterizer_desc2">D3D11_RASTERIZER_DESC2</a> structure that receives a description of the rasterizer state. This rasterizer state can specify forced sample count and conservative rasterization mode.

## -remarks

You use the description for rasterizer state in a call to the <a href="/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-createrasterizerstate2">ID3D11Device3::CreateRasterizerState2</a> method to create the rasterizer-state object.

## -see-also

<a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11rasterizerstate2">ID3D11RasterizerState2</a>
