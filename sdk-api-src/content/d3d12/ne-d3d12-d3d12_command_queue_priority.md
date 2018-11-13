---
UID: NE:d3d12.D3D12_COMMAND_QUEUE_PRIORITY
title: D3D12_COMMAND_QUEUE_PRIORITY
author: windows-sdk-content
description: Defines priority levels for a command queue.
old-location: direct3d12\d3d12_command_queue_priority.htm
tech.root: direct3d12
ms.assetid: 33C07FE4-D85F-4F94-BF0E-C9E0ED05765C
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: D3D12_COMMAND_QUEUE_PRIORITY, D3D12_COMMAND_QUEUE_PRIORITY enumeration, D3D12_COMMAND_QUEUE_PRIORITY_GLOBAL_REALTIME, D3D12_COMMAND_QUEUE_PRIORITY_HIGH, D3D12_COMMAND_QUEUE_PRIORITY_NORMAL, d3d12/D3D12_COMMAND_QUEUE_PRIORITY, d3d12/D3D12_COMMAND_QUEUE_PRIORITY_GLOBAL_REALTIME, d3d12/D3D12_COMMAND_QUEUE_PRIORITY_HIGH, d3d12/D3D12_COMMAND_QUEUE_PRIORITY_NORMAL, direct3d12.d3d12_command_queue_priority
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
 - d3d12.h
api_name:
 - D3D12_COMMAND_QUEUE_PRIORITY
product: Windows
targetos: Windows
req.typenames: D3D12_COMMAND_QUEUE_PRIORITY
req.redist: 
---

# D3D12_COMMAND_QUEUE_PRIORITY enumeration


## -description


Defines priority levels for a command queue.


## -enum-fields




### -field D3D12_COMMAND_QUEUE_PRIORITY_NORMAL

Normal priority.


### -field D3D12_COMMAND_QUEUE_PRIORITY_HIGH

High priority.


### -field D3D12_COMMAND_QUEUE_PRIORITY_GLOBAL_REALTIME

Global realtime priority.


## -remarks



This enumeration is used by the <b>Priority</b> member of the
          <a href="https://msdn.microsoft.com/8C43C45B-0A7B-4336-B546-1E6F13D153F3">D3D12_COMMAND_QUEUE_DESC</a>structure.
        

An application must be sufficiently privileged in order to create a command queue that has global realtime priority. If the application is not sufficiently privileged or if neither the adapter or driver can provide the necessary preemption, then requests to create a global realtime priority queue fail; such a failure could be due to a lack of hardware support or due to conflicts with other command queue parameters. Requests to create a global realtime command queue won't silently downgrade the priority when it can't be supported; the request succeeds or fails as-is to indicate to the application whether or not the command queue is guaranteed to execute before any other queue.




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

