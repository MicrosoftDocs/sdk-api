---
UID: NF:d3d12.ID3D12Device8.CreatePlacedResource1
title: ID3D12Device8::CreatePlacedResource1
description: Creates a resource that is placed in a specific heap. Placed resources are the lightest weight resource objects available, and are the fastest to create and destroy.
helpviewer_keywords: ["ID3D12Device8 interface","CreatePlacedResource1 method","ID3D12Device8.CreatePlacedResource1","ID3D12Device8::CreatePlacedResource1","CreatePlacedResource1","CreatePlacedResource1 method","CreatePlacedResource1 method","ID3D12Device8 interface","direct3d12.id3d12device7_createplacedresource1","d3d12/ID3D12Device8::CreatePlacedResource1"]
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
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
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
 - ID3D12Device8::CreatePlacedResource1
f1_keywords:
 - d3d12/ID3D12Device8::CreatePlacedResource1
dev_langs:
 - c++
---

## -description

Creates a resource that is placed in a specific heap. Placed resources are the lightest weight resource objects available, and are the fastest to create and destroy.

Your application can re-use video memory by overlapping multiple Direct3D placed and reserved resources on heap regions. The simple memory re-use model (described in [Remarks](#remarks)) exists to clarify which overlapping resource is valid at any given time. To maximize graphics tool support, with the simple model data-inheritance isn't supported; and finer-grained tile and sub-resource invalidation isn't supported. Only full overlapping resource invalidation occurs.

## -parameters

### -param pHeap

Type: [in] **<a href="/windows/win32/api/d3d12/nn-d3d12-id3d12heap">ID3D12Heap</a>***

A pointer to the **ID3D12Heap** interface that represents the heap in which the resource is placed.

### -param HeapOffset

Type: **<a href="/windows/win32/WinProg/windows-data-types">UINT64</a>**

The offset, in bytes, to the resource. The *HeapOffset* must be a multiple of the resource's alignment, and *HeapOffset* plus the resource size must be smaller than or equal to the heap size. <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo(uint_uint_constd3d12_resource_desc)">**GetResourceAllocationInfo**</a> must be used to understand the sizes of texture resources.

### -param pDesc

Type: [in] **const <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc1">D3D12_RESOURCE_DESC1</a>***

A pointer to a **D3D12_RESOURCE_DESC1** structure that describes the resource, including a mip region.

### -param InitialState

Type: **<a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATES</a>**

The initial state of the resource, as a bitwise-OR'd combination of **D3D12_RESOURCE_STATES** enumeration constants.

When a resource is created together with a **D3D12_HEAP_TYPE_UPLOAD** heap, *InitialState* must be **D3D12_RESOURCE_STATE_GENERIC_READ**. When a resource is created together with a **D3D12_HEAP_TYPE_READBACK** heap, *InitialState* must be **D3D12_RESOURCE_STATE_COPY_DEST**.

### -param pOptimizedClearValue

Type: [in, optional] **const <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_clear_value">D3D12_CLEAR_VALUE</a>***

Specifies a **D3D12_CLEAR_VALUE** that describes the default value for a clear color.

*pOptimizedClearValue* specifies a value for which clear operations are most optimal. When the created resource is a texture with either the **D3D12_RESOURCE_FLAG_ALLOW_RENDER_TARGET** or **D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL** flags, your application should choose the value that the clear operation will most commonly be called with.

Clear operations can be called with other values, but those operations will not be as efficient as when the value matches the one passed into resource creation.

*pOptimizedClearValue* must be NULL when used with **D3D12_RESOURCE_DIMENSION_BUFFER**.

### -param riid

Type: **REFIID**

The globally unique identifier (**GUID**) for the resource interface. This is an input parameter.

The **REFIID**, or **GUID**, of the interface to the resource can be obtained by using the `__uuidof` macro. For example, `__uuidof(ID3D12Resource)` gets the **GUID** of the interface to a resource. Although **riid** is, most commonly, the GUID for <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12resource">**ID3D12Resource**</a>, it may be any **GUID** for any interface. If the resource object doesn't support the interface for this **GUID**, then creation fails with **E_NOINTERFACE**.

### -param ppvResource

Type: [out, optional] **void****

A pointer to a memory block that receives a pointer to the resource. *ppvResource* can be NULL, to enable capability testing. When *ppvResource* is NULL, no object will be created and S_FALSE will be returned when *pResourceDesc* and other parameters are valid.

## -returns

Type: **<a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a>**

This method returns **E_OUTOFMEMORY** if there is insufficient memory to create the resource. See <a href="/windows/win32/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a> for other possible return values.

## -remarks

See [ID3D12Device::CreatePlacedResource](./nf-d3d12-id3d12device-createplacedresource.md).

## -see-also

* <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource">CreateCommittedResource</a>

* <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource">CreateReservedResource</a>

* <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>

* <a href="/windows/win32/direct3d12/shared-heaps">Shared heaps</a>

* [Sampler feedback specification](https://microsoft.github.io/DirectX-Specs/d3d/SamplerFeedback.html)
