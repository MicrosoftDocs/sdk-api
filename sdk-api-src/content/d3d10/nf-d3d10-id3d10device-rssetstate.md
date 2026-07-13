---
UID: NF:d3d10.ID3D10Device.RSSetState
title: ID3D10Device::RSSetState (d3d10.h)
description: Set the rasterizer state for the rasterizer stage of the pipeline. (ID3D10Device.RSSetState)
helpviewer_keywords: ["ID3D10Device interface [Direct3D 10]","RSSetState method","ID3D10Device.RSSetState","ID3D10Device::RSSetState","RSSetState","RSSetState method [Direct3D 10]","RSSetState method [Direct3D 10]","ID3D10Device interface","a9a649fb-abd5-0934-b091-8a577434dfdc","d3d10/ID3D10Device::RSSetState","direct3d10.id3d10device_rssetstate"]
old-location: direct3d10\id3d10device_rssetstate.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_rssetstate.htm
ms.date: 12/05/2018
ms.keywords: ID3D10Device interface [Direct3D 10],RSSetState method, ID3D10Device.RSSetState, ID3D10Device::RSSetState, RSSetState, RSSetState method [Direct3D 10], RSSetState method [Direct3D 10],ID3D10Device interface, a9a649fb-abd5-0934-b091-8a577434dfdc, d3d10/ID3D10Device::RSSetState, direct3d10.id3d10device_rssetstate
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
 - ID3D10Device::RSSetState
 - d3d10/ID3D10Device::RSSetState
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
 - ID3D10Device.RSSetState
---

# ID3D10Device::RSSetState


## -description

Set the <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_rasterizer_desc">rasterizer state</a> for the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage">rasterizer stage</a> of the pipeline.

## -parameters

### -param pRasterizerState [in]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10rasterizerstate">ID3D10RasterizerState</a>*</b>

Pointer to a rasterizer-state interface (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10rasterizerstate">ID3D10RasterizerState</a>) to bind to the pipeline.

## -remarks

To create a rasterizer state interface, call <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createrasterizerstate">ID3D10Device::CreateRasterizerState</a>. For more details on setting up the rasterizer state, see <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage-getting-started">Set Rasterizer State</a>.

The method will not hold a reference to the interfaces passed in. For that reason, applications should be careful not to release an interface currently in use by the device.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
