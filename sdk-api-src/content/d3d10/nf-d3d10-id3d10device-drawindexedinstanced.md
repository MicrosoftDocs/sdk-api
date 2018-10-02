---
UID: NF:d3d10.ID3D10Device.DrawIndexedInstanced
title: ID3D10Device::DrawIndexedInstanced
author: windows-sdk-content
description: Draw indexed, instanced primitives.
old-location: direct3d10\id3d10device_drawindexedinstanced.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_drawindexedinstanced.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 38658e6f-340e-68e9-eb0a-101f9c8f0c5e, DrawIndexedInstanced, DrawIndexedInstanced method [Direct3D 10], DrawIndexedInstanced method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],DrawIndexedInstanced method, ID3D10Device.DrawIndexedInstanced, ID3D10Device::DrawIndexedInstanced, d3d10/ID3D10Device::DrawIndexedInstanced, direct3d10.id3d10device_drawindexedinstanced
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
 - ID3D10Device.DrawIndexedInstanced
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Device::DrawIndexedInstanced


## -description


Draw indexed, instanced primitives.


## -parameters




### -param IndexCountPerInstance [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Size of the index buffer used in each instance.


### -param InstanceCount [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of instances to draw.


### -param StartIndexLocation [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index of the first index.


### -param BaseVertexLocation [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

Index of the first vertex. The index is signed, which allows a negative index. If the negative index plus the index value from the index buffer are less than 0, the result is undefined.


### -param StartInstanceLocation [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index of the first instance.


## -returns



Returns nothing.




## -remarks



A <a href="https://msdn.microsoft.com/84c0ca29-2356-4b7f-98ee-ff1758edc540">draw API</a> submits work to the rendering pipeline.

Instancing may extend performance by reusing the same geometry to draw multiple objects in a scene. One example of instancing could be to draw the same object with different positions and colors. Indexing requires multiple vertex buffers: at least one for per-vertex data and a second buffer for per-instance data. For an example of instancing, see the <a href="dd22e271-7ace-fcb6-3da2-ba838c59db6e">Instancing10 Sample</a>.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

