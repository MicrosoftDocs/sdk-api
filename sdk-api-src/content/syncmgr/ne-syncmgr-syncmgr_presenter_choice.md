---
UID: NE:syncmgr.SYNCMGR_PRESENTER_CHOICE
title: SYNCMGR_PRESENTER_CHOICE
author: windows-sdk-content
description: Describes what choice a user makes about a sync manager conflict resolution. Used by ISyncMgrConflictPresenter.
old-location: shell\SYNCMGR_PRESENTER_CHOICE.htm
tech.root: shell
ms.assetid: 5e98754b-51d7-4798-9c69-8a9a839c4cda
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: SYNCMGR_PC_KEEP_MULTIPLE, SYNCMGR_PC_KEEP_ONE, SYNCMGR_PC_KEEP_RECENT, SYNCMGR_PC_NO_CHOICE, SYNCMGR_PC_REMOVE_FROM_SYNC_SET, SYNCMGR_PC_SKIP, SYNCMGR_PRESENTER_CHOICE, SYNCMGR_PRESENTER_CHOICE enumeration [Windows Shell], _shell_SYNCMGR_PRESENTER_CHOICE, shell.SYNCMGR_PRESENTER_CHOICE, syncmgr/SYNCMGR_PC_KEEP_MULTIPLE, syncmgr/SYNCMGR_PC_KEEP_ONE, syncmgr/SYNCMGR_PC_KEEP_RECENT, syncmgr/SYNCMGR_PC_NO_CHOICE, syncmgr/SYNCMGR_PC_REMOVE_FROM_SYNC_SET, syncmgr/SYNCMGR_PC_SKIP, syncmgr/SYNCMGR_PRESENTER_CHOICE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: syncmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Syncmgr.idl
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
 - Syncmgr.h
api_name:
 - SYNCMGR_PRESENTER_CHOICE
product: Windows
targetos: Windows
req.typenames: SYNCMGR_PRESENTER_CHOICE
req.redist: 
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
 

 

