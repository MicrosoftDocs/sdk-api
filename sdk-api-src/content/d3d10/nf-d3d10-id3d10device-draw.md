---
UID: NF:d3d10.ID3D10Device.Draw
title: ID3D10Device::Draw method
author: windows-driver-content
description: Draw non-indexed, non-instanced primitives.
old-location: direct3d10\id3d10device_draw.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_draw.htm
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: 32601c9d-0f76-a5ab-559a-a11064280174, Draw method [Direct3D 10], Draw method [Direct3D 10], ID3D10Device interface, Draw,ID3D10Device.Draw, ID3D10Device, ID3D10Device interface [Direct3D 10], Draw method, ID3D10Device::Draw, d3d10/ID3D10Device::Draw, direct3d10.id3d10device_draw
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
req.typenames: D3D10_USAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10.lib
-	D3D10.dll
api_name:
-	ID3D10Device.Draw
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::Draw method


## -description


Draw non-indexed, non-instanced primitives.


## -parameters




### -param VertexCount [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of vertices to draw.


### -param StartVertexLocation [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index of the first vertex, which is usually an offset in a vertex buffer; it could also be used as the first vertex id generated for a shader parameter marked with the <b>SV_TargetId</b> <a href="https://msdn.microsoft.com/6f5c504c-1940-4d1c-b594-a2132599376b">system-value semantic</a>.


## -returns



Returns nothing.




## -remarks



A <a href="https://msdn.microsoft.com/84c0ca29-2356-4b7f-98ee-ff1758edc540">draw API</a> submits work to the rendering pipeline.

The vertex data for a draw call normally comes from a vertex buffer that is bound to the pipeline. However, you could also provide the vertex data from a shader that has vertex data marked with the <b>SV_VertexId</b> <a href="https://msdn.microsoft.com/6f5c504c-1940-4d1c-b594-a2132599376b">system-value semantic</a>.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

