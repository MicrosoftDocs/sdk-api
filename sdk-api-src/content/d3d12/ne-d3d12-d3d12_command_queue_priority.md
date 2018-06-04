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
          <a href="https://msdn.microsoft.com/8C43C45B-0A7B-4336-B546-1E6F13D153F3">D3D12_COMMAND_QUEUE_DESC</a>
          structure.
        

An application must be sufficiently privileged in order to create a command queue that has global realtime priority. If the application is not sufficiently privileged or if neither the adapter or driver can provide the necessary preemption, then requests to create a global realtime priority queue fail; such a failure could be due to a lack of hardware support or due to conflicts with other command queue parameters. Requests to create a global realtime command queue won't silently downgrade the priority when it can't be supported; the request succeeds or fails as-is to indicate to the application whether or not the command queue is guaranteed to execute before any other queue.




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

