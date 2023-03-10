---
UID: NF:d3d12.ID3D12Device.CreateCommittedResource
title: ID3D12Device::CreateCommittedResource (d3d12.h)
description: Creates both a resource and an implicit heap, such that the heap is big enough to contain the entire resource, and the resource is mapped to the heap.
helpviewer_keywords: ["CreateCommittedResource","CreateCommittedResource method","CreateCommittedResource method","ID3D12Device interface","ID3D12Device interface","CreateCommittedResource method","ID3D12Device.CreateCommittedResource","ID3D12Device::CreateCommittedResource","d3d12/ID3D12Device::CreateCommittedResource","direct3d12.id3d12device_createcommittedresource"]
old-location: direct3d12\id3d12device_createcommittedresource.htm
tech.root: direct3d12
ms.assetid: FF9E8F11-F2C5-4A96-8E25-140870D15DA9
ms.date: 12/05/2018
ms.keywords: CreateCommittedResource, CreateCommittedResource method, CreateCommittedResource method,ID3D12Device interface, ID3D12Device interface,CreateCommittedResource method, ID3D12Device.CreateCommittedResource, ID3D12Device::CreateCommittedResource, d3d12/ID3D12Device::CreateCommittedResource, direct3d12.id3d12device_createcommittedresource
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12Device::CreateCommittedResource
 - d3d12/ID3D12Device::CreateCommittedResource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Device.CreateCommittedResource
---

## -description

Creates both a resource and an implicit heap, such that the heap is big enough to contain the entire resource, and the resource is mapped to the heap.

## -parameters

### -param pHeapProperties [in]

Type: **const [D3D12_HEAP_PROPERTIES](./ns-d3d12-d3d12_heap_properties.md)\***

A pointer to a **D3D12_HEAP_PROPERTIES** structure that provides properties for the resource's heap.

### -param HeapFlags [in]

Type: **[D3D12_HEAP_FLAGS](./ne-d3d12-d3d12_heap_flags.md)**

Heap options, as a bitwise-OR'd combination of **D3D12_HEAP_FLAGS** enumeration constants.

### -param pDesc [in]

Type: **const [D3D12_RESOURCE_DESC](./ns-d3d12-d3d12_resource_desc.md)\***

A pointer to a **D3D12_RESOURCE_DESC** structure that describes the resource.

### -param InitialResourceState [in]

Type: **[D3D12_RESOURCE_STATES](./ne-d3d12-d3d12_resource_states.md)**

The initial state of the resource, as a bitwise-OR'd combination of **D3D12_RESOURCE_STATES** enumeration constants.

When you create a resource together with a [D3D12_HEAP_TYPE_UPLOAD](./ne-d3d12-d3d12_heap_type.md) heap, you must set *InitialResourceState* to [D3D12_RESOURCE_STATE_GENERIC_READ](./ne-d3d12-d3d12_resource_states.md).

When you create a resource together with a [D3D12_HEAP_TYPE_READBACK](./ne-d3d12-d3d12_heap_type.md) heap, you must set *InitialResourceState* to [D3D12_RESOURCE_STATE_COPY_DEST](./ne-d3d12-d3d12_resource_states.md).

### -param pOptimizedClearValue [in, optional]

Type: **const [D3D12_CLEAR_VALUE](./ns-d3d12-d3d12_clear_value.md)\***

Specifies a **D3D12_CLEAR_VALUE** structure that describes the default value for a clear color.

*pOptimizedClearValue* specifies a value for which clear operations are most optimal. When the created resource is a texture with either the [D3D12_RESOURCE_FLAG_ALLOW_RENDER_TARGET](./ne-d3d12-d3d12_resource_flags.md) or **D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL** flags, you should choose the value with which the clear operation will most commonly be called. You can call the clear operation with other values, but those operations won't be as efficient as when the value matches the one passed in to resource creation.

When you use [D3D12_RESOURCE_DIMENSION_BUFFER](./ne-d3d12-d3d12_resource_dimension.md), you must set *pOptimizedClearValue* to `nullptr`.

### -param riidResource [in]

Type: **REFIID**

A reference to the globally unique identifier (**GUID**) of the resource interface to return in *ppvResource*.

While *riidResource* is most commonly the **GUID** of [ID3D12Resource](./nn-d3d12-id3d12resource.md), it may be the **GUID** of any interface. If the resource object doesn't support the interface for this **GUID**, then creation fails with **E_NOINTERFACE**.

### -param ppvResource [out, optional]

Type: **void\*\***

An optional pointer to a memory block that receives the requested interface pointer to the created resource object.

*ppvResource* can be `nullptr`, to enable capability testing. When *ppvResource* is `nullptr`, no object is created, and **S_FALSE** is returned when *pDesc* is valid.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

|Return value|Description|
|-|-|
|E_OUTOFMEMORY|There is insufficient memory to create the resource.|

See [Direct3D 12 return codes](/windows/win32/direct3d12/d3d12-graphics-reference-returnvalues) for other possible return values.

## -remarks

This method creates both a resource and a heap, such that the heap is big enough to contain the entire resource, and the resource is mapped to the heap. The created heap is known as an implicit heap, because the heap object can't be obtained by the application. Before releasing the final reference on the resource, your application must ensure that the GPU will no longer read nor write to this resource.

The implicit heap is made resident for GPU access before the method returns control to your application. Also see [Residency](/windows/win32/direct3d12/residency).

The resource GPU VA mapping can't be changed. See [ID3D12CommandQueue::UpdateTileMappings](./nf-d3d12-id3d12commandqueue-updatetilemappings.md) and [Volume tiled resources](/windows/win32/direct3d12/volume-tiled-resources).

This method may be called by multiple threads concurrently.

## Examples

The <a href="/windows/win32/direct3d12/working-samples">D3D12Bundles</a> sample uses <b>ID3D12Device::CreateCommittedResource</b> as follows:

Create a vertex buffer.

```cpp
auto heapProperties = CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT);
auto resourceDesc = CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize);
ThrowIfFailed(m_device->CreateCommittedResource(
    &heapProperties,
    D3D12_HEAP_FLAG_NONE,
    &resourceDesc,
    D3D12_RESOURCE_STATE_COPY_DEST,
    nullptr,
    IID_PPV_ARGS(&m_vertexBuffer)));
```

See [Example code in the Direct3D 12 reference](/windows/win32/direct3d12/notes-on-example-code).

## -see-also

<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource">CreatePlacedResource</a>

<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource">CreateReservedResource</a>

<a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags">D3D12_HEAP_FLAGS</a>

<a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>