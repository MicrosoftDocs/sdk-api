---
UID: NE:syncmgr.SYNCMGR_SYNC_CONTROL_FLAGS
title: SYNCMGR_SYNC_CONTROL_FLAGS (syncmgr.h)
description: Indicates flags used by ISyncMgrControl::StartHandlerSync and ISyncMgrControl::StartItemSync.
helpviewer_keywords: ["SYNCMGR_SCF_IGNORE_IF_ALREADY_SYNCING","SYNCMGR_SCF_NONE","SYNCMGR_SCF_VALID","SYNCMGR_SYNC_CONTROL_FLAGS","SYNCMGR_SYNC_CONTROL_FLAGS enumeration [Windows Shell]","_shell_SYNCMGR_SYNC_CONTROL_FLAGS","shell.SYNCMGR_SYNC_CONTROL_FLAGS","syncmgr/SYNCMGR_SCF_IGNORE_IF_ALREADY_SYNCING","syncmgr/SYNCMGR_SCF_NONE","syncmgr/SYNCMGR_SCF_VALID","syncmgr/SYNCMGR_SYNC_CONTROL_FLAGS"]
old-location: shell\SYNCMGR_SYNC_CONTROL_FLAGS.htm
tech.root: shell
ms.assetid: 2191c105-788d-434e-a3c1-4f7b7dc543c4
ms.date: 12/05/2018
ms.keywords: SYNCMGR_SCF_IGNORE_IF_ALREADY_SYNCING, SYNCMGR_SCF_NONE, SYNCMGR_SCF_VALID, SYNCMGR_SYNC_CONTROL_FLAGS, SYNCMGR_SYNC_CONTROL_FLAGS enumeration [Windows Shell], _shell_SYNCMGR_SYNC_CONTROL_FLAGS, shell.SYNCMGR_SYNC_CONTROL_FLAGS, syncmgr/SYNCMGR_SCF_IGNORE_IF_ALREADY_SYNCING, syncmgr/SYNCMGR_SCF_NONE, syncmgr/SYNCMGR_SCF_VALID, syncmgr/SYNCMGR_SYNC_CONTROL_FLAGS
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
req.typenames: SYNCMGR_SYNC_CONTROL_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SYNCMGR_SYNC_CONTROL_FLAGS
 - syncmgr/SYNCMGR_SYNC_CONTROL_FLAGS
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
 - SYNCMGR_SYNC_CONTROL_FLAGS
---

# SYNCMGR_SYNC_CONTROL_FLAGS enumeration


## -description

Indicates flags used by <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-starthandlersync">ISyncMgrControl::StartHandlerSync</a> and <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-startitemsync">ISyncMgrControl::StartItemSync</a>.

## -enum-fields

### -field SYNCMGR_SCF_NONE:0

Sync all items, regardless of whether they were just synced.

### -field SYNCMGR_SCF_IGNORE_IF_ALREADY_SYNCING:0x1

Sync only items that are not currently syncing.

### -field SYNCMGR_SCF_VALID:0x1

A mask used to retrieve or verify valid <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_sync_control_flags">SYNCMGR_SYNC_CONTROL_FLAGS</a> flags.

## -remarks

 Typically, sync requests are queued if a synchronization is currently in progress. An item might be in both the ongoing synchronization and the queued synchronization. These flags specify whether such an item should be resynched when the queued synchronization is performed.
