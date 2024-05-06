---
UID: NF:d3d12.ID3D12GraphicsCommandList.ClearUnorderedAccessViewFloat
title: ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat (d3d12.h)
description: Sets all the elements in a unordered access view to the specified float values.
helpviewer_keywords: ["ClearUnorderedAccessViewFloat","ClearUnorderedAccessViewFloat method","ClearUnorderedAccessViewFloat method","ID3D12GraphicsCommandList interface","ID3D12GraphicsCommandList interface","ClearUnorderedAccessViewFloat method","ID3D12GraphicsCommandList.ClearUnorderedAccessViewFloat","ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat","d3d12/ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat","direct3d12.id3d12graphicscommandlist_clearunorderedaccessviewfloat"]
old-location: direct3d12\id3d12graphicscommandlist_clearunorderedaccessviewfloat.htm
tech.root: direct3d12
ms.assetid: 6A19F429-D7B2-4A71-8904-31BFA1FD10C6
ms.date: 12/05/2018
ms.keywords: ClearUnorderedAccessViewFloat, ClearUnorderedAccessViewFloat method, ClearUnorderedAccessViewFloat method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,ClearUnorderedAccessViewFloat method, ID3D12GraphicsCommandList.ClearUnorderedAccessViewFloat, ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat, d3d12/ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat, direct3d12.id3d12graphicscommandlist_clearunorderedaccessviewfloat
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
 - ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat
 - d3d12/ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat
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
 - ID3D12GraphicsCommandList.ClearUnorderedAccessViewFloat
---

## -description

Sets all of the elements in an unordered-access view (UAV) to the specified float values.

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
> This descriptor must not be in a shader-visible descriptor heap. This is to allow drivers that implement the clear as a fixed-function hardware operation (rather than as a dispatch) to efficiently read from the descriptor, as shader-visible heaps may be created in **WRITE_BACK** memory (similar to **D3D12_HEAP_TYPE_UPLOAD** heap types), and CPU reads from this type of memory are prohibitively slow.

### -param pResource

Type: [in] **[ID3D12Resource](./nn-d3d12-id3d12resource.md)\***

A pointer to the [ID3D12Resource](./nn-d3d12-id3d12resource.md) interface that represents the unordered-access-view (UAV) resource to clear.

### -param Values

Type: [in] **const FLOAT[4]**

A 4-component array that containing the values to fill the unordered-access-view resource with.

### -param NumRects

Type: [in] **UINT**

The number of rectangles in the array that the *pRects* parameter specifies.

### -param pRects

Type: [in] **const [D3D12_RECT](/windows/win32/direct3d12/d3d12-rect)\***

An array of **D3D12_RECT** structures for the rectangles in the resource view to clear. If **NULL**, **ClearUnorderedAccessViewFloat** clears the entire resource view.

## -remarks

### Runtime validation

For floating-point inputs, the runtime sets denormalized values to 0 (while preserving NANs).

If you want to clear the UAV to a specific bit pattern, consider using [ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint](./nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint.md).

Validation failure results in the call to [ID3D12GraphicsCommandList::Close](./nf-d3d12-id3d12graphicscommandlist-close.md) returning **E_INVALIDARG**.

### Debug layer

The debug layer issues errors if the input values are outside of a normalized range.

The debug layer issues an error if the subresources referenced by the view aren't in the appropriate state. For **ClearUnorderedAccessViewFloat**, the state must be [D3D12_RESOURCE_STATE_UNORDERED_ACCESS](./ne-d3d12-d3d12_resource_states.md).

## -see-also

[ID3D12GraphicsCommandList interface](./nn-d3d12-id3d12graphicscommandlist.md)
