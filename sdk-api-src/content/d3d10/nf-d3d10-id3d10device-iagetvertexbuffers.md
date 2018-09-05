---
UID: NF:d3d10.ID3D10Device.IAGetVertexBuffers
title: ID3D10Device::IAGetVertexBuffers
author: windows-sdk-content
description: Get the vertex buffers bound to the input-assembler stage.
old-location: direct3d10\id3d10device_iagetvertexbuffers.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_iagetvertexbuffers.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: 8b5abcbf-002c-c104-ad3f-1b179ff1df50, IAGetVertexBuffers, IAGetVertexBuffers method [Direct3D 10], IAGetVertexBuffers method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],IAGetVertexBuffers method, ID3D10Device.IAGetVertexBuffers, ID3D10Device::IAGetVertexBuffers, d3d10/ID3D10Device::IAGetVertexBuffers, direct3d10.id3d10device_iagetvertexbuffers
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
 - ID3D10Device.IAGetVertexBuffers
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::IAGetVertexBuffers


## -description


Get the <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">vertex buffers</a> bound to the <a href="https://msdn.microsoft.com/71141a5e-2d79-4b02-8370-c0cbc8618908">input-assembler</a> stage.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The <a href="https://msdn.microsoft.com/84c0ca29-2356-4b7f-98ee-ff1758edc540">input slot</a> of the first vertex buffer to get. The first vertex buffer is explicitly bound to the start slot; this causes each additional vertex buffer in the array to be implicitly bound to each subsequent input slot. A maximum of 16 or 32 input slots (ranges from 0 to either D3D10_IA_VERTEX_INPUT_RESOURCE_SLOT_COUNT - 1 or D3D10_1_IA_VERTEX_INPUT_RESOURCE_SLOT_COUNT - 1) are available; the <a href="https://msdn.microsoft.com/5ad0525c-249f-452d-950b-df8fa2addde2">maximum number of input slots depends on the feature level</a>.


### -param NumBuffers [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of vertex buffers to get starting at the offset. The number of buffers (plus the starting slot) cannot exceed the total number of IA-stage input slots.


### -param ppVertexBuffers [out]

Type: <b><a href="https://msdn.microsoft.com/a81e0dfc-9be4-4ba6-a388-9c9bb97a0fa9">ID3D10Buffer</a>**</b>

A pointer to an array of vertex buffers returned by the method (see <a href="https://msdn.microsoft.com/a81e0dfc-9be4-4ba6-a388-9c9bb97a0fa9">ID3D10Buffer</a>).


### -param pStrides [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Pointer to an array of stride values returned by the method; one stride value for each buffer in the vertex-buffer array. Each stride value is the size (in bytes) of the elements that are to be used from that vertex buffer.


### -param pOffsets [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Pointer to an array of offset values returned by the method; one offset value for each buffer in the vertex-buffer array. Each offset is the number of bytes between the first element of a vertex buffer and the first element that will be used.


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call <a href="http://msdn.microsoft.com/en-us/library/ms682317(VS.85).aspx">IUnknown::Release</a> on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

