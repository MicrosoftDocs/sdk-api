---
UID: NF:d3d11.ID3D11DeviceContext.IASetVertexBuffers
title: ID3D11DeviceContext::IASetVertexBuffers
author: windows-sdk-content
description: Bind an array of vertex buffers to the input-assembler stage.
old-location: direct3d11\id3d11devicecontext_iasetvertexbuffers.htm
tech.root: direct3d11
ms.assetid: e9a9a69c-7df7-4784-98f5-9ad63f6cd407
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IASetVertexBuffers, IASetVertexBuffers method [Direct3D 11], IASetVertexBuffers method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],IASetVertexBuffers method, ID3D11DeviceContext.IASetVertexBuffers, ID3D11DeviceContext::IASetVertexBuffers, d3b78697-f1d6-7517-a7bb-93d9f91ac800, d3d11/ID3D11DeviceContext::IASetVertexBuffers, direct3d11.id3d11devicecontext_iasetvertexbuffers
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
 - ID3D11DeviceContext.IASetVertexBuffers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d11.h
: 
- ID3D11DeviceContext.IASetVertexBuffers
: 
---

# ID3D11DeviceContext::IASetVertexBuffers


## -description


Bind an array of vertex buffers to the <a href="https://msdn.microsoft.com/71141a5e-2d79-4b02-8370-c0cbc8618908">input-assembler stage</a>.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The first input slot for binding. The first vertex buffer is explicitly bound to the start slot; this causes each additional vertex buffer in the array to be implicitly bound to each subsequent input slot. The maximum of 16 or 32 input slots (ranges from 0 to D3D11_IA_VERTEX_INPUT_RESOURCE_SLOT_COUNT - 1) are available; the <a href="https://msdn.microsoft.com/5ad0525c-249f-452d-950b-df8fa2addde2">maximum number of input slots depends on the feature level</a>.
          


### -param NumBuffers [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of vertex buffers in the array. The number of buffers (plus the starting slot) can't exceed the total number of IA-stage input slots (ranges from 0 to D3D11_IA_VERTEX_INPUT_RESOURCE_SLOT_COUNT - StartSlot).


### -param ppVertexBuffers [in, optional]

Type: <b><a href="https://msdn.microsoft.com/7224de57-75cb-4d68-9d70-f5dd2f92b1fd">ID3D11Buffer</a>*</b>

A pointer to an array of vertex buffers (see <a href="https://msdn.microsoft.com/7224de57-75cb-4d68-9d70-f5dd2f92b1fd">ID3D11Buffer</a>). The vertex buffers must have been created with the <a href="https://msdn.microsoft.com/4ffa1714-bd85-4d5a-930d-20526f46e4b9">D3D11_BIND_VERTEX_BUFFER</a> flag.
          


### -param pStrides [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Pointer to an array of stride values; one stride value for each buffer in the vertex-buffer array. Each stride is the size (in bytes) of the elements that are to be used from that vertex buffer.


### -param pOffsets [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Pointer to an array of offset values; one offset value for each buffer in the vertex-buffer array. Each offset is the number of bytes between the first element of a vertex buffer and the first element that will be used.


## -returns



This method does not return a value.




## -remarks



For info about creating vertex buffers, see <a href="https://msdn.microsoft.com/584a39d1-7629-429a-b451-64b1432cb48f">How to: Create a Vertex Buffer</a>.
        

Calling this method using a buffer that is currently bound for writing (that is, bound to the stream output pipeline stage) will effectively bind <b>NULL</b> instead because a buffer can't be bound as both an input and an output at the same time.
        

The debug layer will generate a warning whenever a resource is prevented from being bound simultaneously as an input and an output, but this will not prevent invalid data from being used by the runtime.

The method will hold a reference to the interfaces passed in.
          This differs from the device state behavior in Direct3D 10.
        

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

