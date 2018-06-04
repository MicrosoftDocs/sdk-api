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

# _DFS_STORAGE_INFO_1 structure


## -description


Contains information about a DFS target, including the DFS target server name and share name as well as the target's state and priority.


## -struct-fields




### -field State

State of the target. This member can be one of the following values.



#### DFS_STORAGE_STATE_OFFLINE (0x00000001)

The DFS storage is offline.



#### DFS_STORAGE_STATE_ONLINE (0x00000002)

The DFS storage is online.



#### DFS_STORAGE_STATES (0x0000000F)

Mask value that indicates which storage flags are set.


### -field ServerName

Pointer to a null-terminated Unicode string that specifies the DFS root target or link target server name.


### -field ShareName

Pointer to a null-terminated Unicode string that specifies the DFS root target or link target share name.


### -field TargetPriority


<a href="https://msdn.microsoft.com/b8f645ab-e3b4-4e0f-809a-57e27ab1e641">DFS_TARGET_PRIORITY</a> structure that contains a DFS target's priority class and rank.


## -remarks



This structure is used as the <b>Storage</b> member of the <a href="https://msdn.microsoft.com/96a9c5eb-f79f-4577-b320-ebacff84fcc4">DFS_INFO_6</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/96a9c5eb-f79f-4577-b320-ebacff84fcc4">DFS_INFO_6</a>
 

 

