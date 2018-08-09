---
UID: NF:d3d10.ID3D10Device.IASetVertexBuffers
title: ID3D10Device::IASetVertexBuffers
author: windows-sdk-content
description: Bind an array of vertex buffers to the input-assembler stage.
old-location: direct3d10\id3d10device_iasetvertexbuffers.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_iasetvertexbuffers.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IASetVertexBuffers, IASetVertexBuffers method [Direct3D 10], IASetVertexBuffers method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],IASetVertexBuffers method, ID3D10Device.IASetVertexBuffers, ID3D10Device::IASetVertexBuffers, d3d10/ID3D10Device::IASetVertexBuffers, db68f354-a2bd-412e-0600-c324eb254808, direct3d10.id3d10device_iasetvertexbuffers
ms.prod: windows
ms.technology: windows-sdk
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
 - ID3D10Device.IASetVertexBuffers
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::IASetVertexBuffers


## -description


Bind an array of <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">vertex buffers</a> to the <a href="https://msdn.microsoft.com/71141a5e-2d79-4b02-8370-c0cbc8618908">input-assembler</a> stage.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The first <a href="https://msdn.microsoft.com/84c0ca29-2356-4b7f-98ee-ff1758edc540">input slot</a> for binding. The first vertex buffer is explicitly bound to the start slot; this causes each additional vertex buffer in the array to be implicitly bound to each subsequent input slot. A maximum of 16 or 32 input slots (ranges from 0 to either D3D10_IA_VERTEX_INPUT_RESOURCE_SLOT_COUNT - 1 or D3D10_1_IA_VERTEX_INPUT_RESOURCE_SLOT_COUNT - 1) are available; the <a href="https://msdn.microsoft.com/5ad0525c-249f-452d-950b-df8fa2addde2">maximum number of input slots depends on the feature level</a>.


### -param NumBuffers [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of vertex buffers in the array. The number of buffers (plus the starting slot) cannot exceed the total number of IA-stage input slots.


### -param ppVertexBuffers [in]

Type: <b><a href="https://msdn.microsoft.com/a81e0dfc-9be4-4ba6-a388-9c9bb97a0fa9">ID3D10Buffer</a>*</b>

A pointer to an array of vertex buffers (see <a href="https://msdn.microsoft.com/a81e0dfc-9be4-4ba6-a388-9c9bb97a0fa9">ID3D10Buffer</a>). The vertex buffers must have been created with the <a href="https://msdn.microsoft.com/3bbefc3b-ad05-499b-bbec-f370bf08a7f4">D3D10_BIND_VERTEX_BUFFER</a> flag.


### -param pStrides [in]

Type: <b>const <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Pointer to an array of stride values; one stride value for each buffer in the vertex-buffer array. Each stride is the size (in bytes) of the elements that are to be used from that vertex buffer.


### -param pOffsets [in]

Type: <b>const <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Pointer to an array of offset values; one offset value for each buffer in the vertex-buffer array. Each offset is the number of bytes between the first element of a vertex buffer and the first element that will be used.


## -returns



Returns nothing.




## -remarks



For information about creating vertex buffers, see <a href="https://msdn.microsoft.com/9787b153-9301-4a0f-bd6f-21cc6f7fc650">Create a Vertex Buffer</a>.

Calling this method using a buffer that is currently bound for writing (i.e. bound to the <a href="https://msdn.microsoft.com/f902dc93-9612-481b-a6bd-073e924a4c79">stream output</a> pipeline stage) will effectively bind <b>NULL</b> instead because a buffer cannot be bound as both an input and an output at the same time.

The <a href="https://msdn.microsoft.com/19c81383-6ac7-49ea-98a3-bf761a32ab40">Debug Layer</a> will generate a warning whenever a resource is prevented from being bound simultaneously as an input and an output, but this will not prevent invalid data from being used by the runtime.

The method will not hold a reference to the interfaces passed in. For that reason, applications should be careful not to release an interface currently in use by the device.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

