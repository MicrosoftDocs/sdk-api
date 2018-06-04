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

# SYNCMGR_PRESENTER_CHOICE enumeration


## -description


Describes what choice a user makes about a sync manager conflict resolution. Used by <a href="https://msdn.microsoft.com/ec9a2050-23ad-4478-a705-0a7324e8f84d">ISyncMgrConflictPresenter</a>.


## -enum-fields




### -field SYNCMGR_PC_NO_CHOICE

The user is skipping this conflict, or conflict resolution is being canceled.


### -field SYNCMGR_PC_KEEP_ONE

The user chooses to keep only one item.


### -field SYNCMGR_PC_KEEP_MULTIPLE

The user chooses to keep multiple items.


### -field SYNCMGR_PC_KEEP_RECENT

The user chooses to keep the most recent item.


### -field SYNCMGR_PC_REMOVE_FROM_SYNC_SET

The item is to be removed from the sync set.


### -field SYNCMGR_PC_SKIP

The item is not being resolved now but is instead being skipped so that it can be resolved later.


## -see-also




<a href="https://msdn.microsoft.com/277eee0e-3f75-4ed1-8df2-75289838d3e5">ISyncMgrConflictResolveInfo::GetPresenterChoice</a>



<a href="https://msdn.microsoft.com/5f4bfe69-1ff3-4d21-9c27-f5d8ecfc8371">ISyncMgrConflictResolveInfo::SetPresenterChoice</a>
 

 

