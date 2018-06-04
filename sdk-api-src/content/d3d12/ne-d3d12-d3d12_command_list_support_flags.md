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




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>



<a href="https://msdn.microsoft.com/28BC70FF-6818-4B8D-9DE4-8316AB2FB288">D3D12_COMMAND_LIST_TYPE.</a>
 

 

