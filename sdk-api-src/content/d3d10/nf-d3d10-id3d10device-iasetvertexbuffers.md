---
UID: NF:d3d10.ID3D10Device.IASetVertexBuffers
title: ID3D10Device::IASetVertexBuffers (d3d10.h)
author: windows-sdk-content
description: Bind an array of vertex buffers to the input-assembler stage.
old-location: direct3d10\id3d10device_iasetvertexbuffers.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_iasetvertexbuffers.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IASetVertexBuffers, IASetVertexBuffers method [Direct3D 10], IASetVertexBuffers method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],IASetVertexBuffers method, ID3D10Device.IASetVertexBuffers, ID3D10Device::IASetVertexBuffers, d3d10/ID3D10Device::IASetVertexBuffers, db68f354-a2bd-412e-0600-c324eb254808, direct3d10.id3d10device_iasetvertexbuffers
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
 - ID3D10Device.IASetVertexBuffers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Device::IASetVertexBuffers


## -description


Bind an array of <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">vertex buffers</a> to the <a href="https://msdn.microsoft.com/en-us/library/Bb205116(v=VS.85).aspx">input-assembler</a> stage.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The first <a href="https://msdn.microsoft.com/en-us/library/Bb205117(v=VS.85).aspx">input slot</a> for binding. The first vertex buffer is explicitly bound to the start slot; this causes each additional vertex buffer in the array to be implicitly bound to each subsequent input slot. A maximum of 16 or 32 input slots (ranges from 0 to either D3D10_IA_VERTEX_INPUT_RESOURCE_SLOT_COUNT - 1 or D3D10_1_IA_VERTEX_INPUT_RESOURCE_SLOT_COUNT - 1) are available; the <a href="https://msdn.microsoft.com/5ad0525c-249f-452d-950b-df8fa2addde2">maximum number of input slots depends on the feature level</a>.


### -param NumBuffers [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of vertex buffers in the array. The number of buffers (plus the starting slot) cannot exceed the total number of IA-stage input slots.


### -param ppVertexBuffers [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173510(v=VS.85).aspx">ID3D10Buffer</a>*</b>

A pointer to an array of vertex buffers (see <a href="https://msdn.microsoft.com/en-us/library/Bb173510(v=VS.85).aspx">ID3D10Buffer</a>). The vertex buffers must have been created with the <a href="https://msdn.microsoft.com/en-us/library/Bb204891(v=VS.85).aspx">D3D10_BIND_VERTEX_BUFFER</a> flag.


### -param pStrides [in]

Type: <b>const <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Pointer to an array of stride values; one stride value for each buffer in the vertex-buffer array. Each stride is the size (in bytes) of the elements that are to be used from that vertex buffer.


### -param pOffsets [in]

Type: <b>const <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Pointer to an array of offset values; one offset value for each buffer in the vertex-buffer array. Each offset is the number of bytes between the first element of a vertex buffer and the first element that will be used.


## -returns



Returns nothing.




## -remarks



For information about creating vertex buffers, see <a href="https://msdn.microsoft.com/en-us/library/Bb205130(v=VS.85).aspx">Create a Vertex Buffer</a>.

Calling this method using a buffer that is currently bound for writing (i.e. bound to the <a href="https://msdn.microsoft.com/en-us/library/Bb205121(v=VS.85).aspx">stream output</a> pipeline stage) will effectively bind <b>NULL</b> instead because a buffer cannot be bound as both an input and an output at the same time.

The <a href="https://msdn.microsoft.com/en-us/library/Bb205068(v=VS.85).aspx">Debug Layer</a> will generate a warning whenever a resource is prevented from being bound simultaneously as an input and an output, but this will not prevent invalid data from being used by the runtime.

The method will not hold a reference to the interfaces passed in. For that reason, applications should be careful not to release an interface currently in use by the device.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

