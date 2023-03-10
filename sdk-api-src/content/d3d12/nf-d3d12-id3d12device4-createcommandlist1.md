---
UID: NF:d3d12.ID3D12Device4.CreateCommandList1
title: ID3D12Device4::CreateCommandList1
description: Creates a command list in the closed state.
helpviewer_keywords: ["ID3D12Device4 interface","CreateCommandList1 method","ID3D12Device4.CreateCommandList1","ID3D12Device4::CreateCommandList1","CreateCommandList1","CreateCommandList1 method","CreateCommandList1 method","ID3D12Device4 interface","direct3d12.id3d12device4_createcommandList1","d3d12/ID3D12Device4::CreateCommandList1"]
tech.root: direct3d12
ms.date: 10/14/2019
ms.keywords: ID3D12Device4 interface,CreateCommandList1 method, ID3D12Device4.CreateCommandList1, ID3D12Device4::CreateCommandList1, CreateCommandList1, CreateCommandList1 method, CreateCommandList1 method,ID3D12Device4 interface, direct3d12.id3d12device4_createcommandList1, d3d12/ID3D12Device4::CreateCommandList1
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
 - ID3D12Device4::CreateCommandList1
 - d3d12/ID3D12Device4::CreateCommandList1
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
 - ID3D12Device4::CreateCommandList1
---

## -description

Creates a command list in the closed state. Also see [ID3D12Device::CreateCommandList](./nf-d3d12-id3d12device-createcommandlist.md).

## -parameters

### -param nodeMask [in]

Type: **[UINT](/windows/win32/WinProg/windows-data-types)**

For single-GPU operation, set this to zero. If there are multiple GPU nodes, then set a bit to identify the node (the device's physical adapter) for which to create the command list. Each bit in the mask corresponds to a single node. Only one bit must be set. Also see [Multi-adapter systems](/windows/win32/direct3d12/multi-engine).

### -param type [in]

Type: **[D3D12_COMMAND_LIST_TYPE](./ne-d3d12-d3d12_command_list_type.md)**

Specifies the type of command list to create.

### -param flags

Type: **[D3D12_COMMAND_LIST_FLAGS](./ne-d3d12-d3d12_command_list_flags.md)**

Specifies creation flags.

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

## -see-also

[ID3D12Device::CreateCommandList](./nf-d3d12-id3d12device-createcommandlist.md)
