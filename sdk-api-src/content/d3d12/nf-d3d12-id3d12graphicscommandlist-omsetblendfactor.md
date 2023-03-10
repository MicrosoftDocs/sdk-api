---
UID: NF:d3d12.ID3D12GraphicsCommandList.OMSetBlendFactor
title: ID3D12GraphicsCommandList::OMSetBlendFactor (d3d12.h)
description: Sets the blend factor that modulate values for a pixel shader, render target, or both.
helpviewer_keywords: ["ID3D12GraphicsCommandList interface","OMSetBlendFactor method","ID3D12GraphicsCommandList.OMSetBlendFactor","ID3D12GraphicsCommandList::OMSetBlendFactor","OMSetBlendFactor","OMSetBlendFactor method","OMSetBlendFactor method","ID3D12GraphicsCommandList interface","d3d12/ID3D12GraphicsCommandList::OMSetBlendFactor","direct3d12.id3d12graphicscommandlist_omsetblendfactor"]
old-location: direct3d12\id3d12graphicscommandlist_omsetblendfactor.htm
tech.root: direct3d12
ms.assetid: 344FD8B5-7225-4BEC-9D1F-C9CEDFE8C60F
ms.date: 12/05/2018
ms.keywords: ID3D12GraphicsCommandList interface,OMSetBlendFactor method, ID3D12GraphicsCommandList.OMSetBlendFactor, ID3D12GraphicsCommandList::OMSetBlendFactor, OMSetBlendFactor, OMSetBlendFactor method, OMSetBlendFactor method,ID3D12GraphicsCommandList interface, d3d12/ID3D12GraphicsCommandList::OMSetBlendFactor, direct3d12.id3d12graphicscommandlist_omsetblendfactor
req.header: d3d12.h
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12GraphicsCommandList::OMSetBlendFactor
 - d3d12/ID3D12GraphicsCommandList::OMSetBlendFactor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12GraphicsCommandList.OMSetBlendFactor
---

# ID3D12GraphicsCommandList::OMSetBlendFactor


## -description

Sets the blend factor that modulate values for a pixel shader, render target, or both.

## -parameters

### -param BlendFactor [in, optional]

Type: <b>const FLOAT[4]</b>

Array of blend factors, one for each RGBA component.

## -remarks

If you created the blend-state object with [D3D12_BLEND_BLEND_FACTOR](./ne-d3d12-d3d12_blend.md) or **D3D12_BLEND_INV_BLEND_FACTOR**, then the blending stage uses the non-NULL array of blend factors. Otherwise,the blending stage doesn't use the non-NULL array of blend factors; the runtime stores the blend factors.

If you pass NULL, then the runtime uses or stores a blend factor equal to `{ 1, 1, 1, 1 }`.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>