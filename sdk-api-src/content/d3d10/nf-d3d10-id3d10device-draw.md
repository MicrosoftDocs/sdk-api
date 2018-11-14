---
UID: NF:d3d10.ID3D10Device.Draw
title: ID3D10Device::Draw
author: windows-sdk-content
description: Draw non-indexed, non-instanced primitives.
old-location: direct3d10\id3d10device_draw.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_draw.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 32601c9d-0f76-a5ab-559a-a11064280174, Draw, Draw method [Direct3D 10], Draw method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],Draw method, ID3D10Device.Draw, ID3D10Device::Draw, d3d10/ID3D10Device::Draw, direct3d10.id3d10device_draw
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.Draw
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d10.h
: 
- ID3D10Device.Draw
: 
---

# ID3D10Device::Draw


## -description


Draw non-indexed, non-instanced primitives.


## -parameters




### -param VertexCount [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of vertices to draw.


### -param StartVertexLocation [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Index of the first vertex, which is usually an offset in a vertex buffer; it could also be used as the first vertex id generated for a shader parameter marked with the <b>SV_TargetId</b> <a href="https://msdn.microsoft.com/en-us/library/Bb509647(v=VS.85).aspx">system-value semantic</a>.


## -returns



Returns nothing.




## -remarks



A <a href="https://msdn.microsoft.com/en-us/library/Bb205117(v=VS.85).aspx">draw API</a> submits work to the rendering pipeline.

The vertex data for a draw call normally comes from a vertex buffer that is bound to the pipeline. However, you could also provide the vertex data from a shader that has vertex data marked with the <b>SV_VertexId</b> <a href="https://msdn.microsoft.com/en-us/library/Bb509647(v=VS.85).aspx">system-value semantic</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

