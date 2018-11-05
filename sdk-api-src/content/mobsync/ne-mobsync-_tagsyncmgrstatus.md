---
UID: NE:mobsync._tagSYNCMGRSTATUS
title: "_tagSYNCMGRSTATUS"
author: windows-sdk-content
description: Used in the ISyncMgrSynchronize::SetItemStatus method to specify the updated status for the item.
old-location: shell\syncmgr_syncmgrstatus.htm
tech.root: shell
ms.assetid: a2bdc883-2e61-42a4-a88b-8fab42f018e1
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: SYNCMGRSTATUS, SYNCMGRSTATUS enumeration [Windows Shell], SYNCMGRSTATUS_DELETED, SYNCMGRSTATUS_FAILED, SYNCMGRSTATUS_PAUSED, SYNCMGRSTATUS_PENDING, SYNCMGRSTATUS_RESUMING, SYNCMGRSTATUS_SKIPPED, SYNCMGRSTATUS_STOPPED, SYNCMGRSTATUS_SUCCEEDED, SYNCMGRSTATUS_UPDATING, SYNCMGRSTATUS_UPDATING_INDETERMINATE, _tagSYNCMGRSTATUS, mobsync/SYNCMGRSTATUS, mobsync/SYNCMGRSTATUS_DELETED, mobsync/SYNCMGRSTATUS_FAILED, mobsync/SYNCMGRSTATUS_PAUSED, mobsync/SYNCMGRSTATUS_PENDING, mobsync/SYNCMGRSTATUS_RESUMING, mobsync/SYNCMGRSTATUS_SKIPPED, mobsync/SYNCMGRSTATUS_STOPPED, mobsync/SYNCMGRSTATUS_SUCCEEDED, mobsync/SYNCMGRSTATUS_UPDATING, mobsync/SYNCMGRSTATUS_UPDATING_INDETERMINATE, shell.syncmgr_syncmgrstatus, syncmgr.syncmgrstatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mobsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Mobsync.h
api_name:
 - SYNCMGRSTATUS
product: Windows
targetos: Windows
req.typenames: SYNCMGRSTATUS
req.redist: 
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
 

 

