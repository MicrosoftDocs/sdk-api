---
UID: NE:syncmgr.SYNCMGR_RESOLUTION_ABILITIES
title: SYNCMGR_RESOLUTION_ABILITIES (syncmgr.h)
description: Indicates abilities and the conflict resolution activity to follow. Used with ISyncMgrResolutionHandler::QueryAbilities.
helpviewer_keywords: ["SYNCMGR_RA_KEEPOTHER","SYNCMGR_RA_KEEPRECENT","SYNCMGR_RA_KEEP_MULTIPLE","SYNCMGR_RA_KEEP_SINGLE","SYNCMGR_RA_REMOVEFROMSYNCSET","SYNCMGR_RA_VALID","SYNCMGR_RESOLUTION_ABILITIES","SYNCMGR_RESOLUTION_ABILITIES enumeration [Windows Shell]","_shell_SYNCMGR_RESOLUTION_ABILITIES","shell.SYNCMGR_RESOLUTION_ABILITIES","syncmgr/SYNCMGR_RA_KEEPOTHER","syncmgr/SYNCMGR_RA_KEEPRECENT","syncmgr/SYNCMGR_RA_KEEP_MULTIPLE","syncmgr/SYNCMGR_RA_KEEP_SINGLE","syncmgr/SYNCMGR_RA_REMOVEFROMSYNCSET","syncmgr/SYNCMGR_RA_VALID","syncmgr/SYNCMGR_RESOLUTION_ABILITIES"]
old-location: shell\SYNCMGR_RESOLUTION_ABILITIES.htm
tech.root: shell
ms.assetid: 5a7ff366-e155-43c0-aafe-f61ad0caf550
ms.date: 12/05/2018
ms.keywords: SYNCMGR_RA_KEEPOTHER, SYNCMGR_RA_KEEPRECENT, SYNCMGR_RA_KEEP_MULTIPLE, SYNCMGR_RA_KEEP_SINGLE, SYNCMGR_RA_REMOVEFROMSYNCSET, SYNCMGR_RA_VALID, SYNCMGR_RESOLUTION_ABILITIES, SYNCMGR_RESOLUTION_ABILITIES enumeration [Windows Shell], _shell_SYNCMGR_RESOLUTION_ABILITIES, shell.SYNCMGR_RESOLUTION_ABILITIES, syncmgr/SYNCMGR_RA_KEEPOTHER, syncmgr/SYNCMGR_RA_KEEPRECENT, syncmgr/SYNCMGR_RA_KEEP_MULTIPLE, syncmgr/SYNCMGR_RA_KEEP_SINGLE, syncmgr/SYNCMGR_RA_REMOVEFROMSYNCSET, syncmgr/SYNCMGR_RA_VALID, syncmgr/SYNCMGR_RESOLUTION_ABILITIES
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
targetos: Windows
req.typenames: SYNCMGR_RESOLUTION_ABILITIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SYNCMGR_RESOLUTION_ABILITIES
 - syncmgr/SYNCMGR_RESOLUTION_ABILITIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Syncmgr.h
api_name:
 - SYNCMGR_RESOLUTION_ABILITIES
---

# SYNCMGR_RESOLUTION_ABILITIES enumeration


## -description

Indicates abilities and the conflict resolution activity to follow. Used with <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrresolutionhandler-queryabilities">ISyncMgrResolutionHandler::QueryAbilities</a>.

## -enum-fields

### -field SYNCMGR_RA_KEEPOTHER:0x1

The resolution handler supports merging items and will produce a merged file to keep.

### -field SYNCMGR_RA_KEEPRECENT:0x2

Enables methods <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrresolutionhandler-keeprecent">ISyncMgrResolutionHandler::KeepRecent</a> and <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrresolutionhandler-keepother">ISyncMgrResolutionHandler::KeepOther</a> to be called.

### -field SYNCMGR_RA_REMOVEFROMSYNCSET:0x4

Enables method <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrresolutionhandler-removefromsyncset">ISyncMgrResolutionHandler::RemoveFromSyncSet</a> to be called.

### -field SYNCMGR_RA_KEEP_SINGLE:0x8

Not used.

### -field SYNCMGR_RA_KEEP_MULTIPLE:0x10

Enables method <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrresolutionhandler-keepitems">ISyncMgrResolutionHandler::KeepItems</a> to be called with more than one item in <i>pArray</i>.

### -field SYNCMGR_RA_VALID:0x1f

A mask for valid <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_resolution_abilities">SYNCMGR_RESOLUTION_ABILITIES</a> values.
