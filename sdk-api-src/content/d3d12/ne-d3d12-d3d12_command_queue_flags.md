---
UID: NE:d3d12.D3D12_COMMAND_QUEUE_FLAGS
title: D3D12_COMMAND_QUEUE_FLAGS (d3d12.h)
description: Specifies flags to be used when creating a command queue.
helpviewer_keywords: ["D3D12_COMMAND_QUEUE_FLAGS","D3D12_COMMAND_QUEUE_FLAGS enumeration","D3D12_COMMAND_QUEUE_FLAG_DISABLE_GPU_TIMEOUT","D3D12_COMMAND_QUEUE_FLAG_NONE","d3d12/D3D12_COMMAND_QUEUE_FLAGS","d3d12/D3D12_COMMAND_QUEUE_FLAG_DISABLE_GPU_TIMEOUT","d3d12/D3D12_COMMAND_QUEUE_FLAG_NONE","direct3d12.d3d12_command_queue_flags"]
old-location: direct3d12\d3d12_command_queue_flags.htm
tech.root: direct3d12
ms.assetid: 95040CB8-445B-4E10-8407-AA09637544FB
ms.date: 12/05/2018
ms.keywords: D3D12_COMMAND_QUEUE_FLAGS, D3D12_COMMAND_QUEUE_FLAGS enumeration, D3D12_COMMAND_QUEUE_FLAG_DISABLE_GPU_TIMEOUT, D3D12_COMMAND_QUEUE_FLAG_NONE, d3d12/D3D12_COMMAND_QUEUE_FLAGS, d3d12/D3D12_COMMAND_QUEUE_FLAG_DISABLE_GPU_TIMEOUT, d3d12/D3D12_COMMAND_QUEUE_FLAG_NONE, direct3d12.d3d12_command_queue_flags
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
req.typenames: D3D12_COMMAND_QUEUE_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_COMMAND_QUEUE_FLAGS
 - d3d12/D3D12_COMMAND_QUEUE_FLAGS
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
 - D3D12_COMMAND_QUEUE_FLAGS
---

# D3D12_COMMAND_QUEUE_FLAGS enumeration


## -description

Specifies flags to be used when creating a command queue.

## -enum-fields

### -field D3D12_COMMAND_QUEUE_FLAG_NONE:0

Indicates a default command queue.

### -field D3D12_COMMAND_QUEUE_FLAG_DISABLE_GPU_TIMEOUT:0x1

Indicates that the GPU timeout should be disabled for this command queue.

## -remarks

This enum is used by the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_queue_desc">D3D12_COMMAND_QUEUE_DESC</a> structure.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
