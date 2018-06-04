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

# _DFS_STORAGE_INFO structure


## -description


Contains information about a DFS root or link target in a DFS namespace or from the cache maintained 
    by the DFS client. Information about a DFS root or link target in a DFS namespace is retrieved by 
    calling the <a href="https://msdn.microsoft.com/bbb2f24d-1c49-4016-a16b-60fde4a78193">NetDfsGetInfo</a> function. Information about a 
    DFS root or link target from the cache maintained by the DFS client is retrieved by calling the 
    <a href="https://msdn.microsoft.com/065ec002-cb90-4d78-a70c-6ac37f71994f">NetDfsGetClientInfo</a> function.


## -struct-fields




### -field State

State of the target.

When this structure is returned as a result of calling the 
      <a href="https://msdn.microsoft.com/bbb2f24d-1c49-4016-a16b-60fde4a78193">NetDfsGetInfo</a> function, this member can be one of the 
      following values.



#### DFS_STORAGE_STATE_OFFLINE (0x00000001)

The DFS root or link target is offline.



#### DFS_STORAGE_STATE_ONLINE (0x00000002)

The DFS root or link target is online.

When this structure is returned as a result of calling the 
      <a href="https://msdn.microsoft.com/065ec002-cb90-4d78-a70c-6ac37f71994f">NetDfsGetClientInfo</a> function, the 
      <b>DFS_STORAGE_STATE_ONLINE</b> (0x00000002) state is set by default. If the target is the 
      active target in the DFS client cache, the following value is logically combined with the default value via the 
      <b>OR</b> operator.



#### DFS_STORAGE_STATE_ACTIVE (0x00000004)

The DFS root or link target is the active target.


### -field ServerName

Pointer to a null-terminated Unicode string that specifies the DFS root target or link target server 
      name.


### -field ShareName

Pointer to a null-terminated Unicode string that specifies the DFS root target or link target share 
      name.


## -remarks



The <a href="https://msdn.microsoft.com/fd60cb52-fa17-4cac-a7e8-9803303336dc">DFS_INFO_3</a> and 
    <a href="https://msdn.microsoft.com/0b255be8-b719-4f40-9051-7e8a1bffa0e0">DFS_INFO_4</a> structures each contain one or more 
    <b>DFS_STORAGE_INFO</b> structures, one for each DFS target. 
    Only one target can be marked as the active target. It is possible that no targets will be marked active.




## -see-also




<a href="https://msdn.microsoft.com/fd60cb52-fa17-4cac-a7e8-9803303336dc">DFS_INFO_3</a>



<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System (DFS) Functions</a>



<a href="https://msdn.microsoft.com/c05a8d78-41f4-4c19-a25e-ef4885869584">NetDfsEnum</a>



<a href="https://msdn.microsoft.com/bbb2f24d-1c49-4016-a16b-60fde4a78193">NetDfsGetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>
 

 

