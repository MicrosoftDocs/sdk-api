---
UID: NF:d3d12.ID3D12Device4.CreateHeap1
title: ID3D12Device4::CreateHeap1
description: Creates a heap (optionally for a protected session) that can be used with placed resources and reserved resources.
helpviewer_keywords: ["ID3D12Device4 interface","CreateHeap1 method","ID3D12Device4.CreateHeap1","ID3D12Device4::CreateHeap1","CreateHeap1","CreateHeap1 method","CreateHeap1 method","ID3D12Device4 interface","direct3d12.id3d12device4_createheap1","d3d12/ID3D12Device4::CreateHeap1"]
tech.root: direct3d12
ms.date: 10/14/2019
ms.keywords: ID3D12Device4 interface,CreateHeap1 method, ID3D12Device4.CreateHeap1, ID3D12Device4::CreateHeap1, CreateHeap1, CreateHeap1 method, CreateHeap1 method,ID3D12Device4 interface, direct3d12.id3d12device4_createheap1, d3d12/ID3D12Device4::CreateHeap1
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
 - ID3D12Device4::CreateHeap1
 - d3d12/ID3D12Device4::CreateHeap1
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
 - ID3D12Device4::CreateHeap1
---

## -description

Creates a heap (optionally for a protected session) that can be used with placed resources and reserved resources. Also see [ID3D12Device::CreateHeap](./nf-d3d12-id3d12device-createheap.md).

## -parameters

### -param pDesc [in]

Type: **const [D3D12_HEAP_DESC](./ns-d3d12-d3d12_heap_desc.md)\***

A pointer to a constant **D3D12_HEAP_DESC** structure that describes the heap.

### -param pProtectedSession [in, optional]

Type: **[ID3D12ProtectedResourceSession](./nn-d3d12-id3d12protectedresourcesession.md)\***

An optional pointer to an object that represents a session for content protection. If provided, this session indicates that the heap should be protected. You can obtain an **ID3D12ProtectedResourceSession** by calling [ID3D12Device4::CreateProtectedResourceSession](./nf-d3d12-id3d12device4-createprotectedresourcesession.md).

A heap with a protected session can't be created with the [D3D12_HEAP_FLAG_SHARED_CROSS_ADAPTER](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags) flag.

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

**CreateHeap1** creates a heap that can be used with placed resources and reserved resources.

Before releasing the final reference on the heap, your application must ensure that the GPU will no longer read or write to this heap.

A placed resource object holds a reference on the heap it is created on; but a reserved resource doesn't hold a reference for each mapping made to a heap.

## -see-also
