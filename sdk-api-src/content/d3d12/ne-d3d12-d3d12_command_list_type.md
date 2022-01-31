---
UID: NE:d3d12.D3D12_COMMAND_LIST_TYPE
title: D3D12_COMMAND_LIST_TYPE (d3d12.h)
description: Specifies the type of a command list.
helpviewer_keywords: ["D3D12_COMMAND_LIST_TYPE","D3D12_COMMAND_LIST_TYPE enumeration","D3D12_COMMAND_LIST_TYPE_BUNDLE","D3D12_COMMAND_LIST_TYPE_COMPUTE","D3D12_COMMAND_LIST_TYPE_COPY","D3D12_COMMAND_LIST_TYPE_DIRECT","D3D12_COMMAND_LIST_TYPE_VIDEO_DECODE","D3D12_COMMAND_LIST_TYPE_VIDEO_PROCESS","d3d12/D3D12_COMMAND_LIST_TYPE","d3d12/D3D12_COMMAND_LIST_TYPE_BUNDLE","d3d12/D3D12_COMMAND_LIST_TYPE_COMPUTE","d3d12/D3D12_COMMAND_LIST_TYPE_COPY","d3d12/D3D12_COMMAND_LIST_TYPE_DIRECT","d3d12/D3D12_COMMAND_LIST_TYPE_VIDEO_DECODE","d3d12/D3D12_COMMAND_LIST_TYPE_VIDEO_PROCESS","direct3d12.d3d12_command_list_type"]
old-location: direct3d12\d3d12_command_list_type.htm
tech.root: direct3d12
ms.assetid: 28BC70FF-6818-4B8D-9DE4-8316AB2FB288
ms.date: 12/05/2018
ms.keywords: D3D12_COMMAND_LIST_TYPE, D3D12_COMMAND_LIST_TYPE enumeration, D3D12_COMMAND_LIST_TYPE_BUNDLE, D3D12_COMMAND_LIST_TYPE_COMPUTE, D3D12_COMMAND_LIST_TYPE_COPY, D3D12_COMMAND_LIST_TYPE_DIRECT, D3D12_COMMAND_LIST_TYPE_VIDEO_DECODE, D3D12_COMMAND_LIST_TYPE_VIDEO_PROCESS, d3d12/D3D12_COMMAND_LIST_TYPE, d3d12/D3D12_COMMAND_LIST_TYPE_BUNDLE, d3d12/D3D12_COMMAND_LIST_TYPE_COMPUTE, d3d12/D3D12_COMMAND_LIST_TYPE_COPY, d3d12/D3D12_COMMAND_LIST_TYPE_DIRECT, d3d12/D3D12_COMMAND_LIST_TYPE_VIDEO_DECODE, d3d12/D3D12_COMMAND_LIST_TYPE_VIDEO_PROCESS, direct3d12.d3d12_command_list_type
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
req.typenames: D3D12_COMMAND_LIST_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_COMMAND_LIST_TYPE
 - d3d12/D3D12_COMMAND_LIST_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_COMMAND_LIST_TYPE
---

# D3D12_COMMAND_LIST_TYPE enumeration


## -description

Specifies the type of a command list.

## -enum-fields

### -field D3D12_COMMAND_LIST_TYPE_DIRECT:0

Specifies a command buffer that the GPU can execute. A direct command list doesn't inherit any GPU state.

### -field D3D12_COMMAND_LIST_TYPE_BUNDLE:1

Specifies a command buffer that can be executed only directly via a direct command list. A bundle command list inherits all GPU state (except for the currently set pipeline state object and primitive topology).

### -field D3D12_COMMAND_LIST_TYPE_COMPUTE:2

Specifies a command buffer for computing.

### -field D3D12_COMMAND_LIST_TYPE_COPY:3

Specifies a command buffer for copying.

### -field D3D12_COMMAND_LIST_TYPE_VIDEO_DECODE:4

Specifies a command buffer for video decoding.

### -field D3D12_COMMAND_LIST_TYPE_VIDEO_PROCESS:5

Specifies a command buffer for video processing.

## -remarks

This enum is used by the following methods:

<ul>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandallocator">CreateCommandAllocator</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandqueue">CreateCommandQueue</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandlist">CreateCommandList</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
