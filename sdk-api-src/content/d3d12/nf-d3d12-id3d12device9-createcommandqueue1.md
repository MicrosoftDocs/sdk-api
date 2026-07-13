---
UID: NF:d3d12.ID3D12Device9.CreateCommandQueue1
title: ID3D12Device9::CreateCommandQueue1
description: Creates a command queue with a creator ID.
tech.root: direct3d12
ms.date: 08/09/2021
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
 - ID3D12Device9::CreateCommandQueue1
f1_keywords:
 - ID3D12Device9::CreateCommandQueue1
 - d3d12/ID3D12Device9::CreateCommandQueue1
dev_langs:
 - c++
---

## -description

Creates a command queue with a creator ID.

Also see [ID3D12Device::CreateCommandQueue](nf-d3d12-id3d12device-createcommandqueue.md).

## -parameters

### -param pDesc

Type: \_In\_ **const [D3D12_COMMAND_QUEUE_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc)\***

Specifies a **D3D12_COMMAND_QUEUE_DESC** that describes the command queue.

### -param CreatorID

Type: **[REFIID](/openspecs/windows_protocols/ms-oaut/bbde795f-5398-42d8-9f59-3613da03c318)**

A creator ID. See **Remarks**.

### -param riid

Type: **[REFIID](/openspecs/windows_protocols/ms-oaut/bbde795f-5398-42d8-9f59-3613da03c318)**

The globally unique identifier (GUID) for the command queue interface.

### -param ppCommandQueue

Type: \_COM\_Outptr\_ **void\*\***

A pointer to a memory block that receives a pointer to the [ID3D12CommandQueue](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) interface for the command queue.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

Returns **E_OUTOFMEMORY** if there's insufficient memory to create the command queue; otherwise **S_OK**. See [Direct3D 12 return codes](/windows/win32/direct3d12/d3d12-graphics-reference-returnvalues) for other possible return values.

## -remarks

When multiple components in the same process are sharing a single Direct3D 12 device, often they will end up with separate workloads on independent command queues. In some hardware implementations, independent queues can run in parallel only with specific other command queues.
	 
Direct3D 12 applies a first-come, first-serve grouping for queues, which might not work well for all application or component designs. To help inform Direct3D 12's grouping of queues, you can specify a *creator ID* (which is unique per component) that restricts the grouping to other queues with the same ID. When possible, a component should choose the same unique ID for all of its queues. Microsoft has reserved a few well-known creator IDs for use by Microsoft-developed implementations of APIs on top of Direct3D 12.

## -see-also

* [ID3D12Device::CreateCommandQueue](nf-d3d12-id3d12device-createcommandqueue.md)
