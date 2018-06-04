---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

