---
UID: NF:d3d10.ID3D10Device.OMGetBlendState
title: ID3D10Device::OMGetBlendState (d3d10.h)
description: Get the blend state of the output-merger stage. (ID3D10Device.OMGetBlendState)
helpviewer_keywords: ["ID3D10Device interface [Direct3D 10]","OMGetBlendState method","ID3D10Device.OMGetBlendState","ID3D10Device::OMGetBlendState","OMGetBlendState","OMGetBlendState method [Direct3D 10]","OMGetBlendState method [Direct3D 10]","ID3D10Device interface","b8350c99-7325-98c2-8067-e749ec016907","d3d10/ID3D10Device::OMGetBlendState","direct3d10.id3d10device_omgetblendstate"]
old-location: direct3d10\id3d10device_omgetblendstate.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_omgetblendstate.htm
ms.date: 12/05/2018
ms.keywords: ID3D10Device interface [Direct3D 10],OMGetBlendState method, ID3D10Device.OMGetBlendState, ID3D10Device::OMGetBlendState, OMGetBlendState, OMGetBlendState method [Direct3D 10], OMGetBlendState method [Direct3D 10],ID3D10Device interface, b8350c99-7325-98c2-8067-e749ec016907, d3d10/ID3D10Device::OMGetBlendState, direct3d10.id3d10device_omgetblendstate
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
 - ID3D10Device::OMGetBlendState
 - d3d10/ID3D10Device::OMGetBlendState
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
 - ID3D10Device.OMGetBlendState
---

# ID3D10Device::OMGetBlendState


## -description

Get the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">blend state</a> of the output-merger stage.

## -parameters

### -param ppBlendState [out]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10blendstate">ID3D10BlendState</a>**</b>

Address of a pointer to a blend-state interface (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10blendstate">ID3D10BlendState</a>).

### -param BlendFactor [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

Array of blend factors, one for each RGBA component.

### -param pSampleMask [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

Pointer to a <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-omsetblendstate">sample mask</a>.

## -remarks

The reference count of the returned interface will be incremented by one when the blend state is retrieved. Applications must release returned pointer(s) when they are no longer needed, or else there will be a memory leak.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
