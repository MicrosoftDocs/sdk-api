---
UID: NF:d3d10.ID3D10Device.OMGetDepthStencilState
title: ID3D10Device::OMGetDepthStencilState (d3d10.h)
description: Gets the depth-stencil state of the output-merger stage. (ID3D10Device.OMGetDepthStencilState)
helpviewer_keywords: ["5fead180-40d5-ddfe-7065-11f773e4032e","ID3D10Device interface [Direct3D 10]","OMGetDepthStencilState method","ID3D10Device.OMGetDepthStencilState","ID3D10Device::OMGetDepthStencilState","OMGetDepthStencilState","OMGetDepthStencilState method [Direct3D 10]","OMGetDepthStencilState method [Direct3D 10]","ID3D10Device interface","d3d10/ID3D10Device::OMGetDepthStencilState","direct3d10.id3d10device_omgetdepthstencilstate"]
old-location: direct3d10\id3d10device_omgetdepthstencilstate.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_omgetdepthstencilstate.htm
ms.date: 12/05/2018
ms.keywords: 5fead180-40d5-ddfe-7065-11f773e4032e, ID3D10Device interface [Direct3D 10],OMGetDepthStencilState method, ID3D10Device.OMGetDepthStencilState, ID3D10Device::OMGetDepthStencilState, OMGetDepthStencilState, OMGetDepthStencilState method [Direct3D 10], OMGetDepthStencilState method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::OMGetDepthStencilState, direct3d10.id3d10device_omgetdepthstencilstate
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
 - ID3D10Device::OMGetDepthStencilState
 - d3d10/ID3D10Device::OMGetDepthStencilState
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
 - ID3D10Device.OMGetDepthStencilState
---

# ID3D10Device::OMGetDepthStencilState


## -description

Gets the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">depth-stencil</a> state of the output-merger stage.

## -parameters

### -param ppDepthStencilState [out]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10depthstencilstate">ID3D10DepthStencilState</a>**</b>

Address of a pointer to a depth-stencil state interface (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10depthstencilstate">ID3D10DepthStencilState</a>) to be filled with information from the device.

### -param pStencilRef [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

Pointer to the stencil reference value used in the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">depth-stencil</a> test.

## -remarks

Any returned interfaces will have their reference count incremented by one. Applications should call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> on the returned interfaces when they are no longer needed to avoid memory leaks.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
