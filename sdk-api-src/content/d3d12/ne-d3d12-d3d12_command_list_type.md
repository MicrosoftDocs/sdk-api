---
UID: NE:d3d12.D3D12_COMMAND_LIST_TYPE
title: D3D12_COMMAND_LIST_TYPE
author: windows-sdk-content
description: Specifies the type of a command list.
old-location: direct3d12\d3d12_command_list_type.htm
tech.root: direct3d12
ms.assetid: 28BC70FF-6818-4B8D-9DE4-8316AB2FB288
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: D3D12_COMMAND_LIST_TYPE, D3D12_COMMAND_LIST_TYPE enumeration, D3D12_COMMAND_LIST_TYPE_BUNDLE, D3D12_COMMAND_LIST_TYPE_COMPUTE, D3D12_COMMAND_LIST_TYPE_COPY, D3D12_COMMAND_LIST_TYPE_DIRECT, D3D12_COMMAND_LIST_TYPE_VIDEO_DECODE, D3D12_COMMAND_LIST_TYPE_VIDEO_PROCESS, d3d12/D3D12_COMMAND_LIST_TYPE, d3d12/D3D12_COMMAND_LIST_TYPE_BUNDLE, d3d12/D3D12_COMMAND_LIST_TYPE_COMPUTE, d3d12/D3D12_COMMAND_LIST_TYPE_COPY, d3d12/D3D12_COMMAND_LIST_TYPE_DIRECT, d3d12/D3D12_COMMAND_LIST_TYPE_VIDEO_DECODE, d3d12/D3D12_COMMAND_LIST_TYPE_VIDEO_PROCESS, direct3d12.d3d12_command_list_type
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_COMMAND_LIST_TYPE
product: Windows
targetos: Windows
req.typenames: D3D12_COMMAND_LIST_TYPE
req.redist: 
---

# D3D12_COMMAND_LIST_TYPE enumeration


## -description


Specifies the type of a command list.


## -enum-fields




### -field D3D12_COMMAND_LIST_TYPE_DIRECT

Specifies a command buffer that the GPU can execute. A direct command list doesn't inherit any GPU state.  


### -field D3D12_COMMAND_LIST_TYPE_BUNDLE

Specifies a command buffer that can be executed only directly via a direct command list. A bundle command list inherits all GPU state (except for the currently set pipeline state object and primitive topology).


### -field D3D12_COMMAND_LIST_TYPE_COMPUTE

Specifies a command buffer for computing. 


### -field D3D12_COMMAND_LIST_TYPE_COPY

Specifies a command buffer for copying.


### -field D3D12_COMMAND_LIST_TYPE_VIDEO_DECODE

Specifies a command buffer for video decoding.


### -field D3D12_COMMAND_LIST_TYPE_VIDEO_PROCESS

Specifies a command buffer for video processing.


## -remarks



This enum is used by the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/28DA0D59-3DB7-4652-B1EA-3360EA85A659">CreateCommandAllocator</a>
</li>
<li>
<a href="https://msdn.microsoft.com/556D068C-9939-4B42-AFC2-4EBB2D7B553B">CreateCommandQueue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4C615D7D-6DBC-4EDA-8D72-271EC53047BF">CreateCommandList</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

