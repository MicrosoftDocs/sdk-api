---
UID: NF:d3d10.ID3D10Device.ClearState
title: ID3D10Device::ClearState (d3d10.h)
description: Restore all default device settings; return the device to the state it was in when it was created.
helpviewer_keywords: ["779d4054-49b3-9f94-f49a-3f3d097a65aa","ClearState","ClearState method [Direct3D 10]","ClearState method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","ClearState method","ID3D10Device.ClearState","ID3D10Device::ClearState","d3d10/ID3D10Device::ClearState","direct3d10.id3d10device_clearstate"]
old-location: direct3d10\id3d10device_clearstate.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_clearstate.htm
ms.date: 12/05/2018
ms.keywords: 779d4054-49b3-9f94-f49a-3f3d097a65aa, ClearState, ClearState method [Direct3D 10], ClearState method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],ClearState method, ID3D10Device.ClearState, ID3D10Device::ClearState, d3d10/ID3D10Device::ClearState, direct3d10.id3d10device_clearstate
req.header: d3d10.h
req.include-header: D3d10core
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Device::ClearState
 - d3d10/ID3D10Device::ClearState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d10.h
api_name:
 - ID3D10Device.ClearState
---

# ID3D10Device::ClearState


## -description

Restore all default device settings; return the device to the state it was in when it was created. This will set all set all input/output resource slots, shaders, input layouts, predications, scissor rectangles, depth-stencil state, rasterizer state, blend state, sampler state, and viewports to <b>NULL</b>. The primitive topology will be set to UNDEFINED.



## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
