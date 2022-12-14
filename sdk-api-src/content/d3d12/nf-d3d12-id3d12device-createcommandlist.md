---
UID: NF:d3d12.ID3D12Device.CreateCommandList
title: ID3D12Device::CreateCommandList
description: Creates a command list.
helpviewer_keywords: ["CreateCommandList","CreateCommandList method","CreateCommandList method","ID3D12Device interface","ID3D12Device interface","CreateCommandList method","ID3D12Device.CreateCommandList","ID3D12Device::CreateCommandList","d3d12/ID3D12Device::CreateCommandList","direct3d12.id3d12device_createcommandlist"]
old-location: direct3d12\id3d12device_createcommandlist.htm
tech.root: direct3d12
ms.assetid: 4C615D7D-6DBC-4EDA-8D72-271EC53047BF
ms.date: 12/05/2018
ms.keywords: CreateCommandList, CreateCommandList method, CreateCommandList method,ID3D12Device interface, ID3D12Device interface,CreateCommandList method, ID3D12Device.CreateCommandList, ID3D12Device::CreateCommandList, d3d12/ID3D12Device::CreateCommandList, direct3d12.id3d12device_createcommandlist
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
 - ID3D12Device::CreateCommandList
 - d3d12/ID3D12Device::CreateCommandList
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
 - ID3D12Device.CreateCommandList
---

## -description

Creates a command list.

## -parameters

### -param nodeMask [in]

Type: **[UINT](/windows/win32/WinProg/windows-data-types)**

For single-GPU operation, set this to zero. If there are multiple GPU nodes, then set a bit to identify the node (the device's physical adapter) for which to create the command list. Each bit in the mask corresponds to a single node. Only one bit must be set. Also see [Multi-adapter systems](/windows/win32/direct3d12/multi-engine).

### -param type [in]

Type: **[D3D12_COMMAND_LIST_TYPE](./ne-d3d12-d3d12_command_list_type.md)**

Specifies the type of command list to create.

### -param pCommandAllocator [in]

Type: **[ID3D12CommandAllocator](./nn-d3d12-id3d12commandallocator.md)\***

A pointer to the command allocator object from which the device creates command lists.

### -param pInitialState [in, optional]

Type: **[ID3D12PipelineState](./nn-d3d12-id3d12pipelinestate.md)\***

An optional pointer to the pipeline state object that contains the initial pipeline state for the command list. If it is `nullptr`, then the runtime sets a dummy initial pipeline state, so that drivers don't have to deal with undefined state. The overhead for this is low, particularly for a command list, for which the overall cost of recording the command list likely dwarfs the cost of a single initial state setting. So there's little cost in not setting the initial pipeline state parameter, if doing so is inconvenient.

For bundles, on the other hand, it might make more sense to try to set the initial state parameter (since bundles are likely smaller overall, and can be reused frequently).

### -param riid [in]

Type: **REFIID**

A reference to the globally unique identifier (**GUID**) of the command list interface to return in *ppCommandList*.

### -param ppCommandList [out]

Type: **void\*\***

A pointer to a memory block that receives a pointer to the [ID3D12CommandList](./nn-d3d12-id3d12commandlist.md) or [ID3D12GraphicsCommandList](./nn-d3d12-id3d12graphicscommandlist.md) interface for the command list.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

|Return value|Description|
|-|-|
|E_OUTOFMEMORY|There is insufficient memory to create the command list.|

See [Direct3D 12 return codes](/windows/win32/direct3d12/d3d12-graphics-reference-returnvalues) for other possible return values.

## -remarks

The device creates command lists from the command allocator.

## Examples

The <a href="/windows/win32/direct3d12/working-samples">D3D12Bundles</a> sample uses **ID3D12Device::CreateCommandList** as follows.

Create the pipeline objects.

```cpp
ComPtr<ID3D12CommandAllocator> m_commandAllocator;
ComPtr<ID3D12GraphicsCommandList> m_commandList;
```

Create a command allocator.

```cpp
ThrowIfFailed(m_device->CreateCommandAllocator(D3D12_COMMAND_LIST_TYPE_DIRECT, IID_PPV_ARGS(&m_commandAllocator)));
```

Creating the direct command list.

```cpp
ThrowIfFailed(m_device->CreateCommandList(0, D3D12_COMMAND_LIST_TYPE_DIRECT, m_commandAllocator.Get(), nullptr, IID_PPV_ARGS(&m_commandList)));
```

Refer to the <a href="/windows/win32/direct3d12/notes-on-example-code">Example Code in the D3D12 Reference</a>.

## -see-also

[ID3D12Device](./nn-d3d12-id3d12device.md)

[ID3D12GraphicsCommandList::Reset](./nf-d3d12-id3d12graphicscommandlist-reset.md)
