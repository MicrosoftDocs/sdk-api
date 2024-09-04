---
UID: NF:d3d12.ID3D12Device.CreatePlacedResource
title: ID3D12Device::CreatePlacedResource (d3d12.h)
description: Creates a resource that is placed in a specific heap. Placed resources are the lightest weight resource objects available, and are the fastest to create and destroy.
helpviewer_keywords: ["CreatePlacedResource","CreatePlacedResource method","CreatePlacedResource method","ID3D12Device interface","ID3D12Device interface","CreatePlacedResource method","ID3D12Device.CreatePlacedResource","ID3D12Device::CreatePlacedResource","d3d12/ID3D12Device::CreatePlacedResource","direct3d12.id3d12device_createplacedresource"]
old-location: direct3d12\id3d12device_createplacedresource.htm
tech.root: direct3d12
ms.assetid: 4581A82D-D2B6-4CAE-A336-07B8CF90A0BA
ms.date: 12/05/2018
ms.keywords: CreatePlacedResource, CreatePlacedResource method, CreatePlacedResource method,ID3D12Device interface, ID3D12Device interface,CreatePlacedResource method, ID3D12Device.CreatePlacedResource, ID3D12Device::CreatePlacedResource, d3d12/ID3D12Device::CreatePlacedResource, direct3d12.id3d12device_createplacedresource
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
 - ID3D12Device::CreatePlacedResource
 - d3d12/ID3D12Device::CreatePlacedResource
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
 - ID3D12Device.CreatePlacedResource
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

Type: [in] **const <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc">D3D12_RESOURCE_DESC</a>***

A pointer to a **D3D12_RESOURCE_DESC** structure that describes the resource.

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

**CreatePlacedResource** is similar to fully mapping a reserved resource to an offset within a heap; but the virtual address space associated with a heap may be reused as well.

Placed resources are lighter weight to create and destroy than committed resources are. This is because no heap is created nor destroyed during those operations. In addition, placed resources enable an even lighter weight technique to reuse memory than resource creation and destruction&mdash;that is, reuse through aliasing, and aliasing barriers. Multiple placed resources may simultaneously overlap each other on the same heap, but only a single overlapping resource can be used at a time.

There are two placed resource usage semantics&mdash;a simple model, and an advanced model. We recommend that you choose the simple model (it maximizes graphics tool support across the diverse ecosystem of GPUs), unless and until you find that you need the advanced model for your app.

### Simple model

In this model, you can consider a placed resource to be in one of two states: active, or inactive. It's invalid for the GPU to either read or write from an inactive resource. Placed resources are created in the inactive state.

To activate a resource with an aliasing barrier on a command list, your application must pass the resource in <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier">**D3D12_RESOURCE_ALIASING_BARRIER::pResourceAfter**</a>. **pResourceBefore** can be left NULL during an activation. All resources that share physical memory with the activated resource now become inactive, which includes overlapping placed and reserved resources.

Aliasing barriers should be grouped up and submitted together, in order to maximize efficiency.

After activation, resources with either the render target or depth stencil flags must be further initialized. See the notes on the required resource initialization below.

#### Notes on the required resource initialization

Certain resource types still require initialization. Resources with either the render target or depth stencil flags must be initialized with either a clear operation or a collection of full subresource copies. If an aliasing barrier was used to denote the transition between two aliased resources, the initialization must occur after the aliasing barrier. This initialization is still required whenever a resource would've been activated in the simple model.

Placed and reserved resources with either the render target or depth stencil flags must be initialized with one of the following operations before other operations are supported.

- A *Clear* operation; for example <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview">ClearRenderTargetView</a> or <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview">ClearDepthStencilView</a>.
- A <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource">DiscardResource</a> operation.
- A *Copy* operation; for example <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion">CopyBufferRegion</a>, <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion">CopyTextureRegion</a>, or <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource">CopyResource</a>.

Applications should prefer the most explicit operation that results in the least amount of texels modified. Consider the following examples.

- Using a depth buffer to solve pixel visibility typically requires each depth texel start out at 1.0 or 0. Therefore, a *Clear* operation should be the most efficient option for aliased depth buffer initialization.
- An application may use an aliased render target as a destination for tone mapping. Since the application will render over every pixel during the tone mapping, <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource">DiscardResource</a> should be the most efficient option for initialization.

### Advanced model

In this model, you can ignore the active/inactive state abstraction. Instead, you must honor these lower-level rules.

- An aliasing barrier must be between two different GPU resource accesses of the same physical memory, as long as those accesses are within the same <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists">ExecuteCommandLists</a> call.
- The first rendering operation to certain types of aliased resource must still be an initialization, just like the simple model.

Initialization operations must occur either on an entire subresource, or on a 64KB granularity. An entire subresource initialization is supported for all resource types. A 64KB initialization granularity, aligned at a 64KB offset, is supported for buffers and textures with either the 64KB_UNDEFINED_SWIZZLE or 64KB_STANDARD_SWIZZLE texture layout (refer to <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_texture_layout">D3D12_TEXTURE_LAYOUT</a>).

### Notes on the aliasing barrier

The aliasing barrier may set NULL for both *pResourceAfter* and *pResourceBefore*. The memory coherence definition of <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists">**ExecuteCommandLists**</a> and an aliasing barrier are the same, such that two aliased accesses to the same physical memory need no aliasing barrier when the accesses are in two different **ExecuteCommandLists** invocations. 

For D3D12 advanced usage models, the synchronization definition of <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists">**ExecuteCommandLists**</a> is equivalent to an aliasing barrier. Therefore, applications may either insert an aliasing barrier between reusing physical memory, or ensure the two aliased usages of physical memory occurs in two separate calls to **ExecuteCommandLists**.

The amount of inactivation varies based on resource properties. Textures with undefined memory layouts are the worst case, as the entire texture must be inactivated atomically. For two overlapping resources with defined layouts, inactivation can result in only the overlapping aligned regions of a resource. Data inheritance can even be well-defined. For more details, see <a href="/windows/win32/direct3d12/memory-aliasing-and-data-inheritance">Memory aliasing and data inheritance</a>.

## -see-also

<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource">CreateCommittedResource</a>

<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource">CreateReservedResource</a>

<a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>

<a href="/windows/win32/direct3d12/shared-heaps">Shared Heaps</a>

