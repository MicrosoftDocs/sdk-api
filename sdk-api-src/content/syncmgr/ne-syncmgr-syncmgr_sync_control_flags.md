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

# SYNCMGR_SYNC_CONTROL_FLAGS enumeration


## -description


Indicates flags used by <a href="https://msdn.microsoft.com/ab0e6634-d30a-4f56-94ff-3b032c789cec">ISyncMgrControl::StartHandlerSync</a> and <a href="https://msdn.microsoft.com/7e4798ce-04ee-4c75-8be2-0ad8fdc400a5">ISyncMgrControl::StartItemSync</a>.


## -enum-fields




### -field SYNCMGR_SCF_NONE

Sync all items, regardless of whether they were just synced.


### -field SYNCMGR_SCF_IGNORE_IF_ALREADY_SYNCING

Sync only items that are not currently syncing.


### -field SYNCMGR_SCF_VALID

A mask used to retrieve or verify valid <a href="https://msdn.microsoft.com/2191c105-788d-434e-a3c1-4f7b7dc543c4">SYNCMGR_SYNC_CONTROL_FLAGS</a> flags.


## -remarks



 Typically, sync requests are queued if a synchronization is currently in progress. An item might be in both the ongoing synchronization and the queued synchronization. These flags specify whether such an item should be resynched when the queued synchronization is performed.



