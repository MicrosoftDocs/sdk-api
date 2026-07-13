---
UID: NF:d3d10.ID3D10Device.DrawIndexed
title: ID3D10Device::DrawIndexed (d3d10.h)
description: Draw indexed, non-instanced primitives. (ID3D10Device.DrawIndexed)
helpviewer_keywords: ["9c08e40b-b454-48b6-c9b7-35fc68d81999","DrawIndexed","DrawIndexed method [Direct3D 10]","DrawIndexed method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","DrawIndexed method","ID3D10Device.DrawIndexed","ID3D10Device::DrawIndexed","d3d10/ID3D10Device::DrawIndexed","direct3d10.id3d10device_drawindexed"]
old-location: direct3d10\id3d10device_drawindexed.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_drawindexed.htm
ms.date: 12/05/2018
ms.keywords: 9c08e40b-b454-48b6-c9b7-35fc68d81999, DrawIndexed, DrawIndexed method [Direct3D 10], DrawIndexed method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],DrawIndexed method, ID3D10Device.DrawIndexed, ID3D10Device::DrawIndexed, d3d10/ID3D10Device::DrawIndexed, direct3d10.id3d10device_drawindexed
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
 - ID3D10Device::DrawIndexed
 - d3d10/ID3D10Device::DrawIndexed
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
 - ID3D10Device.DrawIndexed
---

# ID3D10Device::DrawIndexed


## -description

Draw indexed, non-instanced primitives.

## -parameters

### -param IndexCount [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of indices to draw.

### -param StartIndexLocation [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index of the first index to use when accessing the vertex buffer; begin at <i>StartIndexLocation</i> to index vertices from the vertex buffer.

### -param BaseVertexLocation [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

Offset from the start of the vertex buffer to the first vertex.

## -remarks

A <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-getting-started">draw API</a> submits work to the rendering pipeline.

If the sum of both indices is negative, the result of the function call is undefined.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
