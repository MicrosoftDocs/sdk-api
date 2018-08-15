---
UID: NF:d3d10.ID3D10Device.DrawInstanced
title: ID3D10Device::DrawInstanced
author: windows-sdk-content
description: Draw non-indexed, instanced primitives.
old-location: direct3d10\id3d10device_drawinstanced.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_drawinstanced.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 59daf614-be34-5946-a8e4-10a976e15345, DrawInstanced, DrawInstanced method [Direct3D 10], DrawInstanced method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],DrawInstanced method, ID3D10Device.DrawInstanced, ID3D10Device::DrawInstanced, d3d10/ID3D10Device::DrawInstanced, direct3d10.id3d10device_drawinstanced
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
 - ID3D10Device.DrawInstanced
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::DrawInstanced


## -description


Draw non-indexed, instanced primitives.


## -parameters




### -param VertexCountPerInstance [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of vertices to draw.


### -param InstanceCount [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of instances to draw.


### -param StartVertexLocation [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index of the first vertex.


### -param StartInstanceLocation [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index of the first instance.


## -returns



Returns nothing.




## -remarks



A <a href="https://msdn.microsoft.com/en-us/library/Bb205117(v=VS.85).aspx">draw API</a> submits work to the rendering pipeline.

Instancing may extend performance by reusing the same geometry to draw multiple objects in a scene. One example of instancing could be to draw the same object with different positions and colors. For an example of instancing, see the <a href="https://msdn.microsoft.com/library/Ee416415(v=VS.85).aspx">Instancing10 Sample</a>.

The vertex data for an instanced draw call normally comes from a vertex buffer that is bound to the pipeline. However, you could also provide the vertex data from a shader that has instanced data identified with a <a href="https://msdn.microsoft.com/en-us/library/Bb509647(v=VS.85).aspx">system-value semantic</a> (SV_InstanceID).




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

