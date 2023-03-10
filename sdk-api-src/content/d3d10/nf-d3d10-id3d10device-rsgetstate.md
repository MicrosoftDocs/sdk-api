---
UID: NF:d3d10.ID3D10Device.RSGetState
title: ID3D10Device::RSGetState (d3d10.h)
description: Get the rasterizer state from the rasterizer stage of the pipeline. (ID3D10Device.RSGetState)
helpviewer_keywords: ["ID3D10Device interface [Direct3D 10]","RSGetState method","ID3D10Device.RSGetState","ID3D10Device::RSGetState","RSGetState","RSGetState method [Direct3D 10]","RSGetState method [Direct3D 10]","ID3D10Device interface","d3d10/ID3D10Device::RSGetState","direct3d10.id3d10device_rsgetstate","e6855c5c-5337-9573-7375-39d3e0d3e83c"]
old-location: direct3d10\id3d10device_rsgetstate.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_rsgetstate.htm
ms.date: 12/05/2018
ms.keywords: ID3D10Device interface [Direct3D 10],RSGetState method, ID3D10Device.RSGetState, ID3D10Device::RSGetState, RSGetState, RSGetState method [Direct3D 10], RSGetState method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::RSGetState, direct3d10.id3d10device_rsgetstate, e6855c5c-5337-9573-7375-39d3e0d3e83c
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
 - ID3D10Device::RSGetState
 - d3d10/ID3D10Device::RSGetState
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
 - ID3D10Device.RSGetState
---

# ID3D10Device::RSGetState


## -description

Get the <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_rasterizer_desc">rasterizer state</a> from the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage">rasterizer stage</a> of the pipeline.

## -parameters

### -param ppRasterizerState [out]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10rasterizerstate">ID3D10RasterizerState</a>**</b>

Address of a pointer to a rasterizer-state interface (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10rasterizerstate">ID3D10RasterizerState</a>) to fill with information from the device.

## -remarks

Any returned interfaces will have their reference count incremented by one. Applications should call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> on the returned interfaces when they are no longer needed to avoid memory leaks.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
