---
UID: NE:d3d12.D3D12_COMMAND_LIST_SUPPORT_FLAGS
title: D3D12_COMMAND_LIST_SUPPORT_FLAGS (d3d12.h)
author: windows-sdk-content
description: Used to determine which kinds of command lists are capable of supporting various operations.
old-location: direct3d12\d3d12_command_list_support_flags.htm
tech.root: direct3d12
ms.assetid: C30F6F72-65B4-4A7B-849C-7E8C3F7FE60F
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D12_COMMAND_LIST_SUPPORT_FLAGS, D3D12_COMMAND_LIST_SUPPORT_FLAGS enumeration, D3D12_COMMAND_LIST_SUPPORT_FLAG_BUNDLE, D3D12_COMMAND_LIST_SUPPORT_FLAG_COMPUTE, D3D12_COMMAND_LIST_SUPPORT_FLAG_COPY, D3D12_COMMAND_LIST_SUPPORT_FLAG_DIRECT, D3D12_COMMAND_LIST_SUPPORT_FLAG_NONE, D3D12_COMMAND_LIST_SUPPORT_FLAG_VIDEO_DECODE, D3D12_COMMAND_LIST_SUPPORT_FLAG_VIDEO_PROCESS, d3d12/D3D12_COMMAND_LIST_SUPPORT_FLAGS, d3d12/D3D12_COMMAND_LIST_SUPPORT_FLAG_BUNDLE, d3d12/D3D12_COMMAND_LIST_SUPPORT_FLAG_COMPUTE, d3d12/D3D12_COMMAND_LIST_SUPPORT_FLAG_COPY, d3d12/D3D12_COMMAND_LIST_SUPPORT_FLAG_DIRECT, d3d12/D3D12_COMMAND_LIST_SUPPORT_FLAG_NONE, d3d12/D3D12_COMMAND_LIST_SUPPORT_FLAG_VIDEO_DECODE, d3d12/D3D12_COMMAND_LIST_SUPPORT_FLAG_VIDEO_PROCESS, direct3d12.d3d12_command_list_support_flags
ms.topic: enum
f1_keywords: 
 - "d3d12/D3D12_COMMAND_LIST_SUPPORT_FLAGS"
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
 - d3d12.h
api_name:
 - D3D12_COMMAND_LIST_SUPPORT_FLAGS
product: Windows
targetos: Windows
req.typenames: D3D12_COMMAND_LIST_SUPPORT_FLAGS
req.redist: 
ms.custom: 19H1
---

# D3D12_COMMAND_LIST_SUPPORT_FLAGS enumeration


## -description


Used to determine which kinds of command lists are capable of supporting various operations. For example, whether a command list supports immediate writes.
      


## -enum-fields




### -field D3D12_COMMAND_LIST_SUPPORT_FLAG_NONE

Specifies that no command list supports the operation in question.


### -field D3D12_COMMAND_LIST_SUPPORT_FLAG_DIRECT

Specifies that direct command lists can support the operation in question.


### -field D3D12_COMMAND_LIST_SUPPORT_FLAG_BUNDLE

Specifies that command list bundles can support the operation in question.


### -field D3D12_COMMAND_LIST_SUPPORT_FLAG_COMPUTE

Specifies that compute command lists can support the operation in question.


### -field D3D12_COMMAND_LIST_SUPPORT_FLAG_COPY

Specifies that copy command lists can support the operation in question.


### -field D3D12_COMMAND_LIST_SUPPORT_FLAG_VIDEO_DECODE

Specifies that video-decode command lists can support the operation in question.


### -field D3D12_COMMAND_LIST_SUPPORT_FLAG_VIDEO_PROCESS

Specifies that video-processing command lists can support the operation is question.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type">D3D12_COMMAND_LIST_TYPE.</a>
 

 

