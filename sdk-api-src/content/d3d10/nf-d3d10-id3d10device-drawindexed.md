---
UID: NF:d3d10.ID3D10Device.DrawIndexed
title: ID3D10Device::DrawIndexed
author: windows-sdk-content
description: Draw indexed, non-instanced primitives.
old-location: direct3d10\id3d10device_drawindexed.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_drawindexed.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 9c08e40b-b454-48b6-c9b7-35fc68d81999, DrawIndexed, DrawIndexed method [Direct3D 10], DrawIndexed method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],DrawIndexed method, ID3D10Device.DrawIndexed, ID3D10Device::DrawIndexed, d3d10/ID3D10Device::DrawIndexed, direct3d10.id3d10device_drawindexed
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D3D10_USAGE
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
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::DrawIndexed


## -description


Draw indexed, non-instanced primitives.


## -parameters




### -param IndexCount [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of indices to draw.


### -param StartIndexLocation [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index of the first index to use when accesssing the vertex buffer; begin at <i>StartIndexLocation</i> to index vertices from the vertex buffer.


### -param BaseVertexLocation [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

Offset from the start of the vertex buffer to the first vertex.


## -returns



Returns nothing.




## -remarks



A <a href="https://msdn.microsoft.com/en-us/library/Bb205117(v=VS.85).aspx">draw API</a> submits work to the rendering pipeline.

If the sum of both indices is negative, the result of the function call is undefined.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

