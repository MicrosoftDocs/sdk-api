---
UID: NE:syncmgr.SYNCMGR_ITEM_CAPABILITIES
title: SYNCMGR_ITEM_CAPABILITIES (syncmgr.h)
description: Specifies the actions that can be performed against an item.
helpviewer_keywords: ["SYNCMGR_ICM_CAN_BROWSE_CONTENT","SYNCMGR_ICM_CAN_DELETE","SYNCMGR_ICM_CONFLICT_STORE","SYNCMGR_ICM_EVENT_STORE","SYNCMGR_ICM_NONE","SYNCMGR_ICM_PROVIDES_ICON","SYNCMGR_ICM_QUERY_BEFORE_DELETE","SYNCMGR_ICM_QUERY_BEFORE_DISABLE","SYNCMGR_ICM_QUERY_BEFORE_ENABLE","SYNCMGR_ICM_VALID_MASK","SYNCMGR_ITEM_CAPABILITIES","SYNCMGR_ITEM_CAPABILITIES enumeration [Windows Shell]","shell.SYNCMGR_ITEM_CAPABILITIES","shell_SYNCMGR_ITEM_CAPABILITIES","syncmgr/SYNCMGR_ICM_CAN_BROWSE_CONTENT","syncmgr/SYNCMGR_ICM_CAN_DELETE","syncmgr/SYNCMGR_ICM_CONFLICT_STORE","syncmgr/SYNCMGR_ICM_EVENT_STORE","syncmgr/SYNCMGR_ICM_NONE","syncmgr/SYNCMGR_ICM_PROVIDES_ICON","syncmgr/SYNCMGR_ICM_QUERY_BEFORE_DELETE","syncmgr/SYNCMGR_ICM_QUERY_BEFORE_DISABLE","syncmgr/SYNCMGR_ICM_QUERY_BEFORE_ENABLE","syncmgr/SYNCMGR_ICM_VALID_MASK","syncmgr/SYNCMGR_ITEM_CAPABILITIES"]
old-location: shell\SYNCMGR_ITEM_CAPABILITIES.htm
tech.root: shell
ms.assetid: 55f72e18-fba6-4a59-b553-06c6c7c3ee52
ms.date: 12/05/2018
ms.keywords: SYNCMGR_ICM_CAN_BROWSE_CONTENT, SYNCMGR_ICM_CAN_DELETE, SYNCMGR_ICM_CONFLICT_STORE, SYNCMGR_ICM_EVENT_STORE, SYNCMGR_ICM_NONE, SYNCMGR_ICM_PROVIDES_ICON, SYNCMGR_ICM_QUERY_BEFORE_DELETE, SYNCMGR_ICM_QUERY_BEFORE_DISABLE, SYNCMGR_ICM_QUERY_BEFORE_ENABLE, SYNCMGR_ICM_VALID_MASK, SYNCMGR_ITEM_CAPABILITIES, SYNCMGR_ITEM_CAPABILITIES enumeration [Windows Shell], shell.SYNCMGR_ITEM_CAPABILITIES, shell_SYNCMGR_ITEM_CAPABILITIES, syncmgr/SYNCMGR_ICM_CAN_BROWSE_CONTENT, syncmgr/SYNCMGR_ICM_CAN_DELETE, syncmgr/SYNCMGR_ICM_CONFLICT_STORE, syncmgr/SYNCMGR_ICM_EVENT_STORE, syncmgr/SYNCMGR_ICM_NONE, syncmgr/SYNCMGR_ICM_PROVIDES_ICON, syncmgr/SYNCMGR_ICM_QUERY_BEFORE_DELETE, syncmgr/SYNCMGR_ICM_QUERY_BEFORE_DISABLE, syncmgr/SYNCMGR_ICM_QUERY_BEFORE_ENABLE, syncmgr/SYNCMGR_ICM_VALID_MASK, syncmgr/SYNCMGR_ITEM_CAPABILITIES
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
req.typenames: SYNCMGR_ITEM_CAPABILITIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SYNCMGR_ITEM_CAPABILITIES
 - syncmgr/SYNCMGR_ITEM_CAPABILITIES
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
 - SYNCMGR_ITEM_CAPABILITIES
---

# SYNCMGR_ITEM_CAPABILITIES enumeration


## -description

Specifies the actions that can be performed against an item.

## -enum-fields

### -field SYNCMGR_ICM_NONE:0

No capability flags are set.

### -field SYNCMGR_ICM_PROVIDES_ICON:0x1

The item returns a valid object from <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-getobject">ISyncMgrSyncItem::GetObject</a> when that method is called with the SYNCMGR_OBJECTID_Icon flag.

### -field SYNCMGR_ICM_EVENT_STORE:0x2

The item returns a valid object from <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-getobject">ISyncMgrSyncItem::GetObject</a> when that method is called with the SYNCMGR_OBJECTID_EventStore flag.

### -field SYNCMGR_ICM_CONFLICT_STORE:0x4

The item returns a valid object from <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-getobject">ISyncMgrSyncItem::GetObject</a> when that method is called with the SYNCMGR_OBJECTID_ConflictStore flag.

### -field SYNCMGR_ICM_CAN_DELETE:0x10

The user is allowed to delete the item from the handler's folder. This can be used by an item to remove itself from the handler's sync set (for instance, remove a folder from the set of Offline Files). If this value is set, the <b>Delete</b> task is shown in the handler's folder when this item is selected.

### -field SYNCMGR_ICM_CAN_BROWSE_CONTENT:0x10000

The item returns a valid object from <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-getobject">ISyncMgrSyncItem::GetObject</a> when that method is called with the SYNCMGR_OBJECTID_BrowseContent flag. If this value is set, the <b>Browse Content</b> task is added to the item's shortcut menu.

### -field SYNCMGR_ICM_QUERY_BEFORE_ENABLE:0x100000

The item returns a valid object from <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-getobject">ISyncMgrSyncItem::GetObject</a> when that method is called with the SYNCMGR_OBJECTID_QueryBeforeEnable flag.

### -field SYNCMGR_ICM_QUERY_BEFORE_DISABLE:0x200000

The item returns a valid object from <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-getobject">ISyncMgrSyncItem::GetObject</a> when that method is called with the SYNCMGR_OBJECTID_QueryBeforeDisable flag.

### -field SYNCMGR_ICM_QUERY_BEFORE_DELETE:0x400000

The item returns a valid object from <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-getobject">ISyncMgrSyncItem::GetObject</a> when that method is called with the SYNCMGR_OBJECTID_QueryBeforeDelete flag.

### -field SYNCMGR_ICM_VALID_MASK:0x710017

A mask used to retrieve valid <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_item_capabilities">SYNCMGR_ITEM_CAPABILITIES</a> flags.

## -remarks

Sync Center queries the item for its capabilities through <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-getcapabilities">ISyncMgrSyncItem::GetCapabilities</a> whenever the <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-updateitem">ISyncMgrControl::UpdateItem</a> method is called.
