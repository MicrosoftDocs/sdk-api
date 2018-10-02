---
UID: NF:d3d11.ID3D11DeviceContext.DrawIndexedInstanced
title: ID3D11DeviceContext::DrawIndexedInstanced
author: windows-sdk-content
description: Draw indexed, instanced primitives.
old-location: direct3d11\id3d11devicecontext_drawindexedinstanced.htm
tech.root: direct3d11
ms.assetid: c7a4821a-324c-47e4-b89f-603d2afcfb51
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 8742ce56-5b31-7869-ab62-cb36d33cc5ca, DrawIndexedInstanced, DrawIndexedInstanced method [Direct3D 11], DrawIndexedInstanced method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],DrawIndexedInstanced method, ID3D11DeviceContext.DrawIndexedInstanced, ID3D11DeviceContext::DrawIndexedInstanced, d3d11/ID3D11DeviceContext::DrawIndexedInstanced, direct3d11.id3d11devicecontext_drawindexedinstanced
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
 - ID3D11DeviceContext.DrawIndexedInstanced
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DeviceContext::DrawIndexedInstanced


## -description


Draw indexed, instanced primitives.


## -parameters




### -param IndexCountPerInstance [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of indices read from the index buffer for each instance.


### -param InstanceCount [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of instances to draw.


### -param StartIndexLocation [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The location of the first index read by the GPU from the index buffer.


### -param BaseVertexLocation [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

A value added to each index before reading a vertex from the vertex buffer.


### -param StartInstanceLocation [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A value added to each index before reading per-instance data from a vertex buffer.


## -returns



Returns nothing.




## -remarks



A draw API submits work to the rendering pipeline.

Instancing may extend performance by reusing the same geometry to draw multiple objects in a scene. One example of instancing could be 
      to draw the same object with different positions and colors. Instancing requires multiple vertex buffers: at least one for per-vertex data 
      and a second buffer for per-instance data.




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

