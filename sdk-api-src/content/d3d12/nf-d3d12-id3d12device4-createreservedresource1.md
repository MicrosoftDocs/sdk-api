---
UID: NF:d3d12.ID3D12Device4.CreateReservedResource1
title: ID3D12Device4::CreateReservedResource1
description: Creates a resource (optionally for a protected session) that is reserved, and not yet mapped to any pages in a heap.
helpviewer_keywords: ["ID3D12Device4 interface","CreateReservedResource1 method","ID3D12Device4.CreateReservedResource1","ID3D12Device4::CreateReservedResource1","CreateReservedResource1","CreateReservedResource1 method","CreateReservedResource1 method","ID3D12Device4 interface","direct3d12.id3d12device4_createreservedresource1","d3d12/ID3D12Device4::CreateReservedResource1"]
tech.root: direct3d12
ms.date: 10/15/2019
ms.keywords: ID3D12Device4 interface,CreateReservedResource1 method, ID3D12Device4.CreateReservedResource1, ID3D12Device4::CreateReservedResource1, CreateReservedResource1, CreateReservedResource1 method, CreateReservedResource1 method,ID3D12Device4 interface, direct3d12.id3d12device4_createreservedresource1, d3d12/ID3D12Device4::CreateReservedResource1
req.construct-type: function
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: d3d12.lib
req.dll: d3d12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - ID3D12Device4::CreateReservedResource1
 - d3d12/ID3D12Device4::CreateReservedResource1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.lib
 - d3d12.dll
api_name:
 - ID3D12Device4::CreateReservedResource1
---

## -description

Creates a resource (optionally for a protected session) that is reserved, and not yet mapped to any pages in a heap. Also see [ID3D12Device::CreateReservedResource](./nf-d3d12-id3d12device-createreservedresource.md).

> [!NOTE]
> Only tiles from heaps created with the same protected resource session can be mapped into a protected reserved resource.

## -parameters

### -param pDesc [in]

Type: **const [D3D12_RESOURCE_DESC](./ns-d3d12-d3d12_resource_desc.md)\***

A pointer to a **D3D12_RESOURCE_DESC** structure that describes the resource.

### -param InitialState [in]

Type: **[D3D12_RESOURCE_STATES](./ne-d3d12-d3d12_resource_states.md)**

The initial state of the resource, as a bitwise-OR'd combination of **D3D12_RESOURCE_STATES** enumeration constants.

### -param pOptimizedClearValue [in, optional]

Type: **const [D3D12_CLEAR_VALUE](./ns-d3d12-d3d12_clear_value.md)\***

Specifies a **D3D12_CLEAR_VALUE** structure that describes the default value for a clear color.

*pOptimizedClearValue* specifies a value for which clear operations are most optimal. When the created resource is a texture with either the [D3D12_RESOURCE_FLAG_ALLOW_RENDER_TARGET](./ne-d3d12-d3d12_resource_flags.md) or **D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL** flags, you should choose the value with which the clear operation will most commonly be called. You can call the clear operation with other values, but those operations won't be as efficient as when the value matches the one passed in to resource creation.

When you use [D3D12_RESOURCE_DIMENSION_BUFFER](./ne-d3d12-d3d12_resource_dimension.md), you must set *pOptimizedClearValue* to `nullptr`.

### -param pProtectedSession [in, optional]

Type: **[ID3D12ProtectedResourceSession](./nn-d3d12-id3d12protectedresourcesession.md)\***

An optional pointer to an object that represents a session for content protection. If provided, this session indicates that the resource should be protected. You can obtain an **ID3D12ProtectedResourceSession** by calling [ID3D12Device4::CreateProtectedResourceSession](./nf-d3d12-id3d12device4-createprotectedresourcesession.md).

### -param riid [in]

Type: **REFIID**

A reference to the globally unique identifier (**GUID**) of the resource interface to return in *ppvResource*. See **Remarks**.

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

**CreateReservedResource** is equivalent to [D3D11_RESOURCE_MISC_TILED](../d3d11/ne-d3d11-d3d11_resource_misc_flag.md) in Direct3D 11. It creates a resource with virtual memory only, no backing store.

You need to map the resource to physical memory (that is, to a heap) using <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings">CopyTileMappings</a> and <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings">UpdateTileMappings</a>.

These resource types can only be created when the adapter supports tiled resource tier 1 or greater. The tiled resource tier defines the behavior of accessing a resource that is not mapped to a heap.

## -see-also

<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device4-createcommittedresource1">CreateCommittedResource1</a>

<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource">CreatePlacedResource</a>

<a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device4">ID3D12Device4</a>
