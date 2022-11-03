---
UID: NF:d3d12.ID3D12Device10.CreateCommittedResource3
title: ID3D12Device10::CreateCommittedResource3
description: Creates a committed resource with an initial layout rather than an initial state.
helpviewer_keywords:
 - CreateCommittedResource3
tech.root: direct3d12
ms.date: 10/31/2022
req.construct-type: function
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
f1_keywords:
 - ID3D12Device10::CreateCommittedResource3
 - d3d12/ID3D12Device10::CreateCommittedResource3
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.h
api_name:
 - ID3D12Device10::CreateCommittedResource3
---

## -description

Creates a committed resource with an initial layout rather than an initial state.

Requires the DirectX 12 Agility SDK 1.7 or later.

## -parameters

### -param pHeapProperties

Type: \_In\_ **const [D3D12_HEAP_PROPERTIES](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_properties)\***

A pointer to a **D3D12_HEAP_PROPERTIES** structure that provides properties for the resource's heap.

### -param HeapFlags

Type: **[D3D12_HEAP_FLAGS](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags)**

Heap options, as a bitwise-OR'd combination of **D3D12_HEAP_FLAGS** enumeration constants.

### -param pDesc

Type: **const [D3D12_RESOURCE_DESC1](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc1)\***

A pointer to a **D3D12_RESOURCE_DESC1** structure that describes the resource, including a mip region.

### -param InitialLayout

The initial layout of the texture resource; **D3D12_BARRIER_LAYOUT::D3D12_BARRIER_LAYOUT_UNDEFINED** for buffers.

### -param pOptimizedClearValue

Type: **const [D3D12_CLEAR_VALUE](/windows/win32/api/d3d12/ns-d3d12-d3d12_clear_value)\***

Specifies a **D3D12_CLEAR_VALUE** structure that describes the default value for a clear color.

*pOptimizedClearValue* specifies a value for which clear operations are most optimal. When the created resource is a texture with either the [D3D12_RESOURCE_FLAG_ALLOW_RENDER_TARGET](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_flags) or **D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL** flags, you should choose the value with which the clear operation will most commonly be called. You can call the clear operation with other values, but those operations won't be as efficient as when the value matches the one passed in to resource creation.

When you use [D3D12_RESOURCE_DIMENSION_BUFFER](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension), you must set *pOptimizedClearValue* to `nullptr`.

### -param pProtectedSession

Type: **[ID3D12ProtectedResourceSession](/windows/win32/api/d3d12/nn-d3d12-id3d12protectedresourcesession)\***

An optional pointer to an object that represents a session for content protection. If provided, this session indicates that the resource should be protected. You can obtain an **ID3D12ProtectedResourceSession** by calling [ID3D12Device4::CreateProtectedResourceSession](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-createprotectedresourcesession).

### -param NumCastableFormats

The number of elements in *pCastableFormats*.

### -param pCastableFormats

A contiguous array of [DXGI_FORMAT](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) structures that this resource can be cast to.

### -param riidResource

Type: **REFIID**

A reference to the globally unique identifier (**GUID**) of the resource interface to return in *ppvResource*.

While *riidResource* is most commonly the **GUID** of [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource), it may be the **GUID** of any interface. If the resource object doesn't support the interface for this **GUID**, then creation fails with **E_NOINTERFACE**.

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

## -see-also

<a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device10">ID3D12Device10</a>
