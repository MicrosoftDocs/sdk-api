---
UID: NE:syncmgr.SYNCMGR_ITEM_POLICIES
title: SYNCMGR_ITEM_POLICIES (syncmgr.h)
description: Specifies an item's policies to control how they can be enabled or disabled by group policy.
helpviewer_keywords: ["SYNCMGR_IPM_DISABLE_BROWSE","SYNCMGR_IPM_DISABLE_DELETE","SYNCMGR_IPM_DISABLE_DISABLE","SYNCMGR_IPM_DISABLE_ENABLE","SYNCMGR_IPM_DISABLE_START_SYNC","SYNCMGR_IPM_DISABLE_STOP_SYNC","SYNCMGR_IPM_HIDDEN_BY_DEFAULT","SYNCMGR_IPM_NONE","SYNCMGR_IPM_PREVENT_DISABLE","SYNCMGR_IPM_PREVENT_ENABLE","SYNCMGR_IPM_PREVENT_START_SYNC","SYNCMGR_IPM_PREVENT_STOP_SYNC","SYNCMGR_IPM_VALID_MASK","SYNCMGR_ITEM_POLICIES","SYNCMGR_ITEM_POLICIES enumeration [Windows Shell]","shell.SYNCMGR_ITEM_POLICIES","shell_SYNCMGR_ITEM_POLICIES","syncmgr/SYNCMGR_IPM_DISABLE_BROWSE","syncmgr/SYNCMGR_IPM_DISABLE_DELETE","syncmgr/SYNCMGR_IPM_DISABLE_DISABLE","syncmgr/SYNCMGR_IPM_DISABLE_ENABLE","syncmgr/SYNCMGR_IPM_DISABLE_START_SYNC","syncmgr/SYNCMGR_IPM_DISABLE_STOP_SYNC","syncmgr/SYNCMGR_IPM_HIDDEN_BY_DEFAULT","syncmgr/SYNCMGR_IPM_NONE","syncmgr/SYNCMGR_IPM_PREVENT_DISABLE","syncmgr/SYNCMGR_IPM_PREVENT_ENABLE","syncmgr/SYNCMGR_IPM_PREVENT_START_SYNC","syncmgr/SYNCMGR_IPM_PREVENT_STOP_SYNC","syncmgr/SYNCMGR_IPM_VALID_MASK","syncmgr/SYNCMGR_ITEM_POLICIES"]
old-location: shell\SYNCMGR_ITEM_POLICIES.htm
tech.root: shell
ms.assetid: d894beca-855c-472f-931a-db5c6f3f891e
ms.date: 12/05/2018
ms.keywords: SYNCMGR_IPM_DISABLE_BROWSE, SYNCMGR_IPM_DISABLE_DELETE, SYNCMGR_IPM_DISABLE_DISABLE, SYNCMGR_IPM_DISABLE_ENABLE, SYNCMGR_IPM_DISABLE_START_SYNC, SYNCMGR_IPM_DISABLE_STOP_SYNC, SYNCMGR_IPM_HIDDEN_BY_DEFAULT, SYNCMGR_IPM_NONE, SYNCMGR_IPM_PREVENT_DISABLE, SYNCMGR_IPM_PREVENT_ENABLE, SYNCMGR_IPM_PREVENT_START_SYNC, SYNCMGR_IPM_PREVENT_STOP_SYNC, SYNCMGR_IPM_VALID_MASK, SYNCMGR_ITEM_POLICIES, SYNCMGR_ITEM_POLICIES enumeration [Windows Shell], shell.SYNCMGR_ITEM_POLICIES, shell_SYNCMGR_ITEM_POLICIES, syncmgr/SYNCMGR_IPM_DISABLE_BROWSE, syncmgr/SYNCMGR_IPM_DISABLE_DELETE, syncmgr/SYNCMGR_IPM_DISABLE_DISABLE, syncmgr/SYNCMGR_IPM_DISABLE_ENABLE, syncmgr/SYNCMGR_IPM_DISABLE_START_SYNC, syncmgr/SYNCMGR_IPM_DISABLE_STOP_SYNC, syncmgr/SYNCMGR_IPM_HIDDEN_BY_DEFAULT, syncmgr/SYNCMGR_IPM_NONE, syncmgr/SYNCMGR_IPM_PREVENT_DISABLE, syncmgr/SYNCMGR_IPM_PREVENT_ENABLE, syncmgr/SYNCMGR_IPM_PREVENT_START_SYNC, syncmgr/SYNCMGR_IPM_PREVENT_STOP_SYNC, syncmgr/SYNCMGR_IPM_VALID_MASK, syncmgr/SYNCMGR_ITEM_POLICIES
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
req.typenames: SYNCMGR_ITEM_POLICIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SYNCMGR_ITEM_POLICIES
 - syncmgr/SYNCMGR_ITEM_POLICIES
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
 - SYNCMGR_ITEM_POLICIES
---

# SYNCMGR_ITEM_POLICIES enumeration


## -description

Specifies an item's policies to control how they can be enabled or disabled by group policy.

## -enum-fields

### -field SYNCMGR_IPM_NONE:0

No policy flags are set.

### -field SYNCMGR_IPM_PREVENT_ENABLE:0x1

Enabling of the item is not supported at the time of the call. This value can be used by an item to implement support for group policy that prevents the item from being enabled. If this value is set, the <b>Enable</b> task is not shown in the handler's folder when this item is selected. The item should provide a comment—returned from its implementation of <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynciteminfo-getcomment">ISyncMgrSyncItemInfo::GetComment</a>—to let the user know why the <b>Enable</b> task is not available. Most items should not set this value.

### -field SYNCMGR_IPM_PREVENT_DISABLE:0x2

Disabling of the item is not supported at the time of the call. This value can be used by an item to implement support for group policy that prevents the item from being disabled. If this value is set, the <b>Disable</b> task is not shown in the handler's folder when this item is selected. The item should provide a comment—returned from its implementation of <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynciteminfo-getcomment">ISyncMgrSyncItemInfo::GetComment</a>—to let the user know why the <b>Disable</b> task is not available. Most items should not set this value.

### -field SYNCMGR_IPM_PREVENT_START_SYNC:0x4

Starting a sync through the user interface or through the APIs is not supported.  Sync can be started only by an external application that creates a session creator to report progress. If this value is set, then the Start Sync task will not be shown in the handler's folder when the sync item is selected. Note that Start Sync must be supported on a handler in order for it to be supported on a sync item. Most sync items should not set this value.

### -field SYNCMGR_IPM_PREVENT_STOP_SYNC:0x8

Stopping a sync through the user interface or through the APIs is not supported. If this value is set, the Stop Sync task is not shown in the handler's folder when the sync item is selected. Note that Stop Sync must be supported on a handler in order for it to be supported on a sync item. Most sync items should not set this value.

### -field SYNCMGR_IPM_DISABLE_ENABLE:0x10

The enable task should be disabled when it is shown for this sync item. With this policy set, the <b>Enable</b> option appears in the context menu, if SYNCMGR_IPM_PREVENT_ENABLE is not set, but is disabled.

### -field SYNCMGR_IPM_DISABLE_DISABLE:0x20

The disable task should be disabled when it is shown for this sync item. With this policy set, the <b>Disable</b> option appears in the context menu, if SYNCMGR_IPM_PREVENT_DISABLE is not set, but is disabled.

### -field SYNCMGR_IPM_DISABLE_START_SYNC:0x40

The Start Sync task should be disabled when it is shown for this sync item. With this policy set, the <b>Start Sync</b> option appears in the context menu, if SYNCMGR_IPM_PREVENT_START_SYNC is not set and if SYNCMGR_HPM_PREVENT_START_SYNC is not set on the handle, but is disabled.

### -field SYNCMGR_IPM_DISABLE_STOP_SYNC:0x80

The <b>Stop Sync</b> task should be disabled when it is shown for this sync item. With this policy set, the <b>Stop Sync</b> option appears in the context menu, if SYNCMGR_IPM_PREVENT_STOP_SYNC is not set and if SYNCMGR_HPM_PREVENT_STOP_SYNC is not set on the handler, but is disabled.

### -field SYNCMGR_IPM_DISABLE_BROWSE:0x100

The <b>Browse</b> task should be disabled when it is shown for this sync item. The <b>Browse</b> task is shown only if the SYNCMGR_ICM_CAN_BROWSE_CONTENT value is returned from the <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-getcapabilities">ISyncMgrSyncItem::GetCapabilities</a> method.

### -field SYNCMGR_IPM_DISABLE_DELETE:0x200

The handler normally supports deleting items, but that this item cannot be deleted at the time of the call. With this policy set, the <b>Delete</b> option appears as disabled in the context menu for the sync item.

### -field SYNCMGR_IPM_HIDDEN_BY_DEFAULT:0x10000

The item should be hidden from the user unless the <b>Show Hidden Files</b> option has been enabled. This policy only applies the first time the item is loaded. After that, the hidden state is maintained by Sync Center and can be changed by the user through the property sheet.

### -field SYNCMGR_IPM_VALID_MASK:0x102ff

A mask used to retrieve valid <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_item_policies">SYNCMGR_ITEM_POLICIES</a> flags.
