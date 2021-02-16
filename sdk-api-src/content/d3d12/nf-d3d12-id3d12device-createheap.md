---
UID: NF:d3d12.ID3D12Device.CreateHeap
title: ID3D12Device::CreateHeap
description: Creates a heap that can be used with placed resources and reserved resources.
helpviewer_keywords: ["CreateHeap","CreateHeap method","CreateHeap method","ID3D12Device interface","ID3D12Device interface","CreateHeap method","ID3D12Device.CreateHeap","ID3D12Device::CreateHeap","d3d12/ID3D12Device::CreateHeap","direct3d12.id3d12device_createheap"]
old-location: direct3d12\id3d12device_createheap.htm
tech.root: direct3d12
ms.assetid: DB5DF4B2-4673-4B8D-BDED-9F672A41E7F6
ms.date: 12/05/2018
ms.keywords: CreateHeap, CreateHeap method, CreateHeap method,ID3D12Device interface, ID3D12Device interface,CreateHeap method, ID3D12Device.CreateHeap, ID3D12Device::CreateHeap, d3d12/ID3D12Device::CreateHeap, direct3d12.id3d12device_createheap
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
 - ID3D12Device::CreateHeap
 - d3d12/ID3D12Device::CreateHeap
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
 - ID3D12Device.CreateHeap
---

## -description

Creates a heap that can be used with placed resources and reserved resources.

## -parameters

### -param pDesc [in]

Type: **const [D3D12_HEAP_DESC](./ns-d3d12-d3d12_heap_desc.md)\***

A pointer to a constant **D3D12_HEAP_DESC** structure that describes the heap.

### -param riid [in]

Type: **REFIID**

A reference to the globally unique identifier (**GUID**) of the heap interface to return in *ppvHeap*.

While *riidResource* is most commonly the **GUID** of [ID3D12Heap](./nn-d3d12-id3d12heap.md), it may be the **GUID** of any interface. If the resource object doesn't support the interface for this **GUID**, then creation fails with **E_NOINTERFACE**.

### -param ppvHeap [out, optional]

Type: **void\*\***

An optional pointer to a memory block that receives the requested interface pointer to the created heap object.

*ppvHeap* can be `nullptr`, to enable capability testing. When *ppvHeap* is `nullptr`, no object is created, and **S_FALSE** is returned when *pDesc* is valid.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

|Return value|Description|
|-|-|
|E_OUTOFMEMORY|There is insufficient memory to create the heap.|

See [Direct3D 12 return codes](/windows/win32/direct3d12/d3d12-graphics-reference-returnvalues) for other possible return values.

## -remarks

**CreateHeap** creates a heap that can be used with placed resources and reserved resources.

Before releasing the final reference on the heap, your application must ensure that the GPU will no longer read or write to this heap.

A placed resource object holds a reference on the heap it is created on; but a reserved resource doesn't hold a reference for each mapping made to a heap.

## -see-also

[ID3D12Device](./nn-d3d12-id3d12device.md)

[Shared heaps](/windows/win32/direct3d12/shared-heaps)