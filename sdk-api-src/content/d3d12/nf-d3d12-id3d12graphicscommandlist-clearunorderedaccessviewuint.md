---
UID: NF:d3d12.ID3D12GraphicsCommandList.ClearUnorderedAccessViewUint
title: ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint (d3d12.h)
description: Sets all the elements in a unordered-access view (UAV) to the specified integer values.
helpviewer_keywords: ["ClearUnorderedAccessViewUint","ClearUnorderedAccessViewUint method","ClearUnorderedAccessViewUint method","ID3D12GraphicsCommandList interface","ID3D12GraphicsCommandList interface","ClearUnorderedAccessViewUint method","ID3D12GraphicsCommandList.ClearUnorderedAccessViewUint","ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint","d3d12/ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint","direct3d12.id3d12graphicscommandlist_clearunorderedaccessviewuint"]
old-location: direct3d12\id3d12graphicscommandlist_clearunorderedaccessviewuint.htm
tech.root: direct3d12
ms.assetid: A048BF0C-9141-4DDF-91F9-B53464033A44
ms.date: 12/05/2018
ms.keywords: ClearUnorderedAccessViewUint, ClearUnorderedAccessViewUint method, ClearUnorderedAccessViewUint method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,ClearUnorderedAccessViewUint method, ID3D12GraphicsCommandList.ClearUnorderedAccessViewUint, ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint, d3d12/ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint, direct3d12.id3d12graphicscommandlist_clearunorderedaccessviewuint
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint
 - d3d12/ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12GraphicsCommandList.ClearUnorderedAccessViewUint
---

## -description

Sets all the elements in a unordered-access view (UAV) to the specified integer values.

> [!IMPORTANT]
> This behaves like a compute operation in that it isn't ordered with respect to surrounding work such as **Dispatch** calls. To ensure ordering, barrier calls must be issued before and/or after the **ClearUnorderedAccessViewXxx** call as needed. It might appear on some drivers that such barriers aren't necessary. But implicit barriers are not a spec guarantee; so they can't be relied upon. This is in contrast to **ClearDepthStencilView** and **ClearRenderTargetView** which (like **DrawXxx** commands), respect command list ordering.

## -parameters

### -param ViewGPUHandleInCurrentHeap

Type: [in] **[D3D12_GPU_DESCRIPTOR_HANDLE](./ns-d3d12-d3d12_gpu_descriptor_handle.md)**

A [D3D12_GPU_DESCRIPTOR_HANDLE](./ns-d3d12-d3d12_gpu_descriptor_handle.md) that references an initialized descriptor for the unordered-access view (UAV) that is to be cleared. This descriptor must be in a shader-visible descriptor heap, which must be set on the command list via [SetDescriptorHeaps](nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps.md).

### -param ViewCPUHandle

Type: [in] **[D3D12_CPU_DESCRIPTOR_HANDLE](./ns-d3d12-d3d12_cpu_descriptor_handle.md)**

A [D3D12_CPU_DESCRIPTOR_HANDLE](./ns-d3d12-d3d12_cpu_descriptor_handle.md) in a non-shader visible descriptor heap that references an initialized descriptor for the unordered-access view (UAV) that is to be cleared.

> [!IMPORTANT]
> This descriptor must not be in a shader-visible descriptor heap. This is to allow drivers that implement the clear as a fixed-function hardware operation (rather than as a dispatch) to efficiently read from the descriptor, as shader-visible heaps may be created in **WRITE_COMBINE** memory (similar to **D3D12_HEAP_TYPE_UPLOAD** heap types), and CPU reads from this type of memory are prohibitively slow.

### -param pResource

Type: [in] **[ID3D12Resource](./nn-d3d12-id3d12resource.md)\***

A pointer to the [ID3D12Resource](./nn-d3d12-id3d12resource.md) interface that represents the unordered-access-view (UAV) resource to clear.

### -param Values

Type: [in] **const UINT[4]**

A 4-component array that containing the values to fill the unordered-access-view resource with.

### -param NumRects

Type: [in] **UINT**

The number of rectangles in the array that the *pRects* parameter specifies.

### -param pRects

Type: [in] **const [D3D12_RECT](/windows/win32/direct3d12/d3d12-rect)\***

An array of **D3D12_RECT** structures for the rectangles in the resource view to clear. If **NULL**, **ClearUnorderedAccessViewUint** clears the entire resource view.

## -remarks

### Runtime validation

Validation failure results in the call to [ID3D12GraphicsCommandList::Close](./nf-d3d12-id3d12graphicscommandlist-close.md) returning **E_INVALIDARG**.

### Debug layer

The debug layer issues errors if the input values are outside of a normalized range.

The debug layer issues an error if the subresources referenced by the view aren't in the appropriate state. For **ClearUnorderedAccessViewUint**, the state must be [D3D12_RESOURCE_STATE_UNORDERED_ACCESS](./ne-d3d12-d3d12_resource_states.md).

## -see-also

[ID3D12GraphicsCommandList interface](./nn-d3d12-id3d12graphicscommandlist.md)
