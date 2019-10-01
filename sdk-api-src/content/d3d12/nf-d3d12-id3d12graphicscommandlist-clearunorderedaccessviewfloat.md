---
UID: NF:d3d12.ID3D12GraphicsCommandList.ClearUnorderedAccessViewFloat
title: ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat (d3d12.h)
author: windows-sdk-content
description: Sets all the elements in a unordered access view to the specified float values.
old-location: direct3d12\id3d12graphicscommandlist_clearunorderedaccessviewfloat.htm
tech.root: direct3d12
ms.assetid: 6A19F429-D7B2-4A71-8904-31BFA1FD10C6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ClearUnorderedAccessViewFloat, ClearUnorderedAccessViewFloat method, ClearUnorderedAccessViewFloat method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,ClearUnorderedAccessViewFloat method, ID3D12GraphicsCommandList.ClearUnorderedAccessViewFloat, ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat, d3d12/ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat, direct3d12.id3d12graphicscommandlist_clearunorderedaccessviewfloat
ms.topic: method
f1_keywords: 
 - "d3d12/ID3D12GraphicsCommandList.ClearUnorderedAccessViewFloat"
req.header: d3d12.h
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12GraphicsCommandList.ClearUnorderedAccessViewFloat
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat


## -description


Sets all the elements in a unordered access view to the specified float values.


## -parameters




### -param ViewGPUHandleInCurrentHeap [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle">D3D12_GPU_DESCRIPTOR_HANDLE</a></b>

Describes the GPU descriptor handle that represents the start of the heap for the unordered-access view to clear.
          


### -param ViewCPUHandle [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle">D3D12_CPU_DESCRIPTOR_HANDLE</a></b>

Describes the CPU descriptor handle that represents the start of the heap for the render target to clear.
          


### -param pResource [in]

Type: <b>ID3D12Resource*</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a> interface that represents the unordered-access-view resource to clear.
          


### -param Values [in]

Type: <b>const FLOAT[4]</b>

A 4-component array that containing the values to fill the unordered-access-view resource with.
          


### -param NumRects [in]

Type: <b>UINT</b>

The number of rectangles in the array that the <i>pRects</i> parameter specifies.
          


### -param pRects [in]

Type: <b>const D3D12_RECT*</b>

An array of <b>D3D12_RECT</b> structures for the rectangles in the resource view to clear. If <b>NULL</b>, <b>ClearUnorderedAccessViewFloat</b> clears the entire resource view.
          


## -returns



This method does not return a value.
          




## -remarks



<h3><a id="Runtime_validation"></a><a id="runtime_validation"></a><a id="RUNTIME_VALIDATION"></a>Runtime validation</h3>
For floating-point inputs, the runtime will set denormalized values to 0 (while preserving NANs).
          

Validation failure will result in the call to <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close">Close</a> returning <b>E_INVALIDARG</b>.
          

<h3><a id="Debug_layer"></a><a id="debug_layer"></a><a id="DEBUG_LAYER"></a>Debug layer</h3>
The debug layer will issue errors if the input values are outside of a normalized range.
          

The debug layer will issue an error if the subresources referenced by the view are not in the appropriate state. For <b>ClearUnorderedAccessViewFloat</b>, the state must be <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATE_UNORDERED_ACCESS</a>.
          




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>
 

 

