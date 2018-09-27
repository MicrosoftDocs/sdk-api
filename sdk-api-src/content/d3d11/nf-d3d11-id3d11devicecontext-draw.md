---
UID: NF:d3d11.ID3D11DeviceContext.Draw
title: ID3D11DeviceContext::Draw
author: windows-sdk-content
description: Draw non-indexed, non-instanced primitives.
old-location: direct3d11\id3d11devicecontext_draw.htm
tech.root: direct3d11
ms.assetid: 9c63067b-c7ac-412c-ad49-c35d4fba1d68
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: 531461d1-7b41-e75e-d7e7-78e6386f31f4, Draw, Draw method [Direct3D 11], Draw method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],Draw method, ID3D11DeviceContext.Draw, ID3D11DeviceContext::Draw, d3d11/ID3D11DeviceContext::Draw, direct3d11.id3d11devicecontext_draw
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.Draw
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DeviceContext::Draw


## -description


Draw non-indexed, non-instanced primitives.


## -parameters




### -param VertexCount [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of vertices to draw.


### -param StartVertexLocation [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Index of the first vertex, which is usually an offset in a vertex buffer.


## -returns



Returns nothing.




## -remarks



<b>Draw</b> submits work to the rendering pipeline.

The vertex data for a draw call normally comes from a vertex buffer that is bound to the pipeline.

Even without any vertex buffer bound to the pipeline, you can generate your own vertex data in your vertex shader by using the <a href="https://msdn.microsoft.com/en-us/library/Bb509647(v=VS.85).aspx">SV_VertexID</a> system-value semantic to determine the current vertex that the runtime is processing.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476385(v=VS.85).aspx">ID3D11DeviceContext</a>
 

 

