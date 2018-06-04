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

# _tagSYNCMGRSTATUS enumeration


## -description


Used in the <a href="https://msdn.microsoft.com/311e916c-46a0-4eb2-a5e3-8da417ae7d71">ISyncMgrSynchronize::SetItemStatus</a> method to specify the updated status for the item.


## -enum-fields




### -field SYNCMGRSTATUS_STOPPED

Synchronization has been stopped.


### -field SYNCMGRSTATUS_SKIPPED

Indicates that this item should be skipped.


### -field SYNCMGRSTATUS_PENDING

Synchronization for the item is pending.


### -field SYNCMGRSTATUS_UPDATING

The item is currently being synchronized.


### -field SYNCMGRSTATUS_SUCCEEDED

The synchronization for the item succeeded.


### -field SYNCMGRSTATUS_FAILED

Synchronization for the item failed.


### -field SYNCMGRSTATUS_PAUSED

Synchronization for the item paused.


### -field SYNCMGRSTATUS_RESUMING

Synchronization for the item is resuming.


### -field SYNCMGRSTATUS_UPDATING_INDETERMINATE

<b>Windows Vista and later</b>. Shows marquee progress for the synchronized item. Sets the progress bar in the folder to marquee the synchronization progress.


### -field SYNCMGRSTATUS_DELETED

The item has been deleted. This value has been deprecated for Windows Vista and later.


## -see-also




<a href="https://msdn.microsoft.com/311e916c-46a0-4eb2-a5e3-8da417ae7d71">ISyncMgrSynchronize::SetItemStatus</a>
 

 

