---
UID: NS:d3d12.D3D12_COMMAND_QUEUE_DESC
title: D3D12_COMMAND_QUEUE_DESC (d3d12.h)
description: Describes a command queue.
helpviewer_keywords: ["D3D12_COMMAND_QUEUE_DESC","D3D12_COMMAND_QUEUE_DESC structure","d3d12/D3D12_COMMAND_QUEUE_DESC","direct3d12.d3d12_command_queue_desc"]
old-location: direct3d12\d3d12_command_queue_desc.htm
tech.root: direct3d12
ms.assetid: 8C43C45B-0A7B-4336-B546-1E6F13D153F3
ms.date: 12/05/2018
ms.keywords: D3D12_COMMAND_QUEUE_DESC, D3D12_COMMAND_QUEUE_DESC structure, d3d12/D3D12_COMMAND_QUEUE_DESC, direct3d12.d3d12_command_queue_desc
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D12_COMMAND_QUEUE_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_COMMAND_QUEUE_DESC
 - d3d12/D3D12_COMMAND_QUEUE_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_COMMAND_QUEUE_DESC
---

# D3D12_COMMAND_QUEUE_DESC structure


## -description

Describes a command queue.

## -struct-fields

### -field Type

Specifies one member of <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type">D3D12_COMMAND_LIST_TYPE</a>.

### -field Priority

The priority for the command queue, as a 
            <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_command_queue_priority">D3D12_COMMAND_QUEUE_PRIORITY</a> enumeration constant to select normal or high priority.

### -field Flags

Specifies any flags from the <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_command_queue_flags">D3D12_COMMAND_QUEUE_FLAGS</a> enumeration.

### -field NodeMask

For single GPU operation, set this to zero. If there are multiple GPU nodes, set a bit to identify the node (the  device's physical adapter) to which the command queue applies.
            Each bit in the mask corresponds to a single node.
            Only 1 bit must be set.
          Refer to <a href="/windows/win32/direct3d12/multi-engine">Multi-adapter systems</a>.

## -remarks

This structure is passed into <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue">CreateCommandQueue</a>.
        

This structure is returned by <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getdesc">ID3D12CommandQueue::GetDesc</a>.

## -see-also

<a href="/windows/win32/direct3d12/direct3d-12-structures">Core Structures</a>

