---
UID: NF:d3d12.ID3D12GraphicsCommandList.ClearUnorderedAccessViewUint
title: ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint (d3d12.h)
description: Sets all the elements in a unordered-access view (UAV) to the specified integer values.helpviewer_keywords: ["ClearUnorderedAccessViewUint","ClearUnorderedAccessViewUint method","ClearUnorderedAccessViewUint method","ID3D12GraphicsCommandList interface","ID3D12GraphicsCommandList interface","ClearUnorderedAccessViewUint method","ID3D12GraphicsCommandList.ClearUnorderedAccessViewUint","ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint","d3d12/ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint","direct3d12.id3d12graphicscommandlist_clearunorderedaccessviewuint"]
old-location: direct3d12\id3d12graphicscommandlist_clearunorderedaccessviewuint.htm
tech.root: direct3d12
ms.assetid: A048BF0C-9141-4DDF-91F9-B53464033A44
ms.date: 12/05/2018
ms.keywords: ClearUnorderedAccessViewUint, ClearUnorderedAccessViewUint method, ClearUnorderedAccessViewUint method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,ClearUnorderedAccessViewUint method, ID3D12GraphicsCommandList.ClearUnorderedAccessViewUint, ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint, d3d12/ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint, direct3d12.id3d12graphicscommandlist_clearunorderedaccessviewuint
f1_keywords:
- d3d12/ID3D12GraphicsCommandList.ClearUnorderedAccessViewUint
dev_langs:
- c++
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
- ID3D12GraphicsCommandList.ClearUnorderedAccessViewUint
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Sets all the elements in a unordered-access view (UAV) to the specified integer values.

## -parameters

### -param ViewGPUHandleInCurrentHeap [in]

Type: <b><a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle">D3D12_GPU_DESCRIPTOR_HANDLE</a></b>

A <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle">D3D12_GPU_DESCRIPTOR_HANDLE</a> that references an initialized descriptor for the unordered-access view that is to be cleared. This descriptor must be in a shader-visible descriptor heap, which must be set on the command list via [SetDescriptorHeaps](nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps.md).

### -param ViewCPUHandle [in]

Type: <b><a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle">D3D12_CPU_DESCRIPTOR_HANDLE</a></b>

A <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle">D3D12_CPU_DESCRIPTOR_HANDLE</a> that references an initialized descriptor for the unordered-access view (UAV) that is to be cleared.

> [!IMPORTANT]
> This descriptor must not be in a shader-visible descriptor heap.

### -param pResource [in]

Type: <b>ID3D12Resource\*</b>

A pointer to the <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a> interface that represents the unordered-access view resource to clear.
          
### -param Values [in]

Type: <b>const UINT[4]</b>

A four-component array containing the values to fill the unordered-access view resource with.

### -param NumRects [in]

Type: <b>UINT</b>

The number of rectangles in the array that the <i>pRects</i> parameter specifies.

### -param pRects [in]

Type: <b>const D3D12_RECT*</b>

An array of <b>D3D12_RECT</b> structures for the rectangles in the resource view to clear. If <b>NULL</b>, then <b>ClearUnorderedAccessViewUint</b> clears the entire resource view.
          
## -remarks

<h3><a id="Runtime_validation"></a><a id="runtime_validation"></a><a id="RUNTIME_VALIDATION"></a>Runtime validation</h3>
Validation failure will result in the call to <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close">ID3D12GraphicsCommandList::Close</a> returning <b>E_INVALIDARG</b>.

<h3><a id="Debug_layer"></a><a id="debug_layer"></a><a id="DEBUG_LAYER"></a>Debug layer</h3>
The debug layer will issue errors if the input values are outside of a normalized range.

The debug layer will issue an error if the subresources referenced by the view are not in the appropriate state. For <b>ClearUnorderedAccessViewUint</b>, the state must be <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATE_UNORDERED_ACCESS</a>.

## -see-also

[ID3D12GraphicsCommandList](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)
