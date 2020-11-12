---
UID: NF:d3d12.ID3D12Device8.CreateCommittedResource2
title: ID3D12Device8::CreateCommittedResource2
description: Creates both a resource and an implicit heap (optionally for a protected session), such that the heap is big enough to contain the entire resource, and the resource is mapped to the heap.
helpviewer_keywords: ["ID3D12Device8 interface","CreateCommittedResource2 method","ID3D12Device8.CreateCommittedResource2","ID3D12Device8::CreateCommittedResource2","CreateCommittedResource2","CreateCommittedResource2 method","CreateCommittedResource2 method","ID3D12Device8 interface","direct3d12.id3d12device7_createcommittedresource2","d3d12/ID3D12Device8::CreateCommittedResource2"]
tech.root: direct3d12
ms.date: 09/16/2020
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: d3d12.dll
req.header: d3d12.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: d3d12.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.lib
 - d3d12.dll
api_name:
 - ID3D12Device8::CreateCommittedResource2
f1_keywords:
 - d3d12/ID3D12Device8::CreateCommittedResource2
dev_langs:
 - c++
---

## -description

Creates both a resource and an implicit heap (optionally for a protected session), such that the heap is big enough to contain the entire resource, and the resource is mapped to the heap. Also see [ID3D12Device::CreateCommittedResource](./nf-d3d12-id3d12device-createcommittedresource.md) for a code example.

## -parameters

### -param pHeapProperties

Type: _In_ **const [D3D12_HEAP_PROPERTIES](./ns-d3d12-d3d12_heap_properties.md)\***

A pointer to a **D3D12_HEAP_PROPERTIES** structure that provides properties for the resource's heap.

### -param HeapFlags

Type: **[D3D12_HEAP_FLAGS](./ne-d3d12-d3d12_heap_flags.md)**

Heap options, as a bitwise-OR'd combination of **D3D12_HEAP_FLAGS** enumeration constants.

### -param pDesc

_In_ const D3D12_RESOURCE_DESC1 *pDesc,
Type: **const [D3D12_RESOURCE_DESC1](./ns-d3d12-d3d12_resource_desc1.md)\***

A pointer to a **D3D12_RESOURCE_DESC1** structure that describes the resource, including a mip region.

### -param InitialResourceState

Type: **[D3D12_RESOURCE_STATES](./ne-d3d12-d3d12_resource_states.md)**

The initial state of the resource, as a bitwise-OR'd combination of **D3D12_RESOURCE_STATES** enumeration constants.

When you create a resource together with a [D3D12_HEAP_TYPE_UPLOAD](./ne-d3d12-d3d12_heap_type.md) heap, you must set *InitialResourceState* to [D3D12_RESOURCE_STATE_GENERIC_READ](./ne-d3d12-d3d12_resource_states.md).

When you create a resource together with a [D3D12_HEAP_TYPE_READBACK](./ne-d3d12-d3d12_heap_type.md) heap, you must set *InitialResourceState* to [D3D12_RESOURCE_STATE_COPY_DEST](./ne-d3d12-d3d12_resource_states.md).

### -param pOptimizedClearValue

Type: **const [D3D12_CLEAR_VALUE](./ns-d3d12-d3d12_clear_value.md)\***

Specifies a **D3D12_CLEAR_VALUE** structure that describes the default value for a clear color.

*pOptimizedClearValue* specifies a value for which clear operations are most optimal. When the created resource is a texture with either the [D3D12_RESOURCE_FLAG_ALLOW_RENDER_TARGET](./ne-d3d12-d3d12_resource_flags.md) or **D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL** flags, you should choose the value with which the clear operation will most commonly be called. You can call the clear operation with other values, but those operations won't be as efficient as when the value matches the one passed in to resource creation.

When you use [D3D12_RESOURCE_DIMENSION_BUFFER](./ne-d3d12-d3d12_resource_dimension.md), you must set *pOptimizedClearValue* to `nullptr`.

### -param pProtectedSession

Type: **[ID3D12ProtectedResourceSession](./nn-d3d12-id3d12protectedresourcesession.md)\***

An optional pointer to an object that represents a session for content protection. If provided, this session indicates that the resource should be protected. You can obtain an **ID3D12ProtectedResourceSession** by calling [ID3D12Device4::CreateProtectedResourceSession](./nf-d3d12-id3d12device4-createprotectedresourcesession.md).

### -param riidResource

Type: **REFIID**

A reference to the globally unique identifier (**GUID**) of the resource interface to return in *ppvResource*.

While *riidResource* is most commonly the **GUID** of [ID3D12Resource](./nn-d3d12-id3d12resource.md), it may be the **GUID** of any interface. If the resource object doesn't support the interface for this **GUID**, then creation fails with **E_NOINTERFACE**.

### -param ppvResource

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

## -see-also

* [Sampler feedback specification](https://microsoft.github.io/DirectX-Specs/d3d/SamplerFeedback.html)