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

# SYNCMGR_ITEM_POLICIES enumeration


## -description


Specifies an item's policies to control how they can be enabled or disabled by group policy.


## -enum-fields




### -field SYNCMGR_IPM_NONE

No policy flags are set.


### -field SYNCMGR_IPM_PREVENT_ENABLE

Enabling of the item is not supported at the time of the call. This value can be used by an item to implement support for group policy that prevents the item from being enabled. If this value is set, the <b>Enable</b> task is not shown in the handler's folder when this item is selected. The item should provide a comment—returned from its implementation of <a href="https://msdn.microsoft.com/3959784b-2926-43fd-b8e5-bb1884e5d321">ISyncMgrSyncItemInfo::GetComment</a>—to let the user know why the <b>Enable</b> task is not available. Most items should not set this value.


### -field SYNCMGR_IPM_PREVENT_DISABLE

Disabling of the item is not supported at the time of the call. This value can be used by an item to implement support for group policy that prevents the item from being disabled. If this value is set, the <b>Disable</b> task is not shown in the handler's folder when this item is selected. The item should provide a comment—returned from its implementation of <a href="https://msdn.microsoft.com/3959784b-2926-43fd-b8e5-bb1884e5d321">ISyncMgrSyncItemInfo::GetComment</a>—to let the user know why the <b>Disable</b> task is not available. Most items should not set this value.


### -field SYNCMGR_IPM_PREVENT_START_SYNC

Starting a sync through the user interface or through the APIs is not supported.  Sync can be started only by an external application that creates a session creator to report progress. If this value is set, then the Start Sync task will not be shown in the handler's folder when the sync item is selected. Note that Start Sync must be supported on a handler in order for it to be supported on a sync item. Most sync items should not set this value.


### -field SYNCMGR_IPM_PREVENT_STOP_SYNC

Stopping a sync through the user interface or through the APIs is not supported. If this value is set, the Stop Sync task is not shown in the handler's folder when the sync item is selected. Note that Stop Sync must be supported on a handler in order for it to be supported on a sync item. Most sync items should not set this value.


### -field SYNCMGR_IPM_DISABLE_ENABLE

The enable task should be disabled when it is shown for this sync item. With this policy set, the <b>Enable</b> option appears in the context menu, if SYNCMGR_IPM_PREVENT_ENABLE is not set, but is disabled.


### -field SYNCMGR_IPM_DISABLE_DISABLE

The disable task should be disabled when it is shown for this sync item. With this policy set, the <b>Disable</b> option appears in the context menu, if SYNCMGR_IPM_PREVENT_DISABLE is not set, but is disabled.


### -field SYNCMGR_IPM_DISABLE_START_SYNC

The Start Sync task should be disabled when it is shown for this sync item. With this policy set, the <b>Start Sync</b> option appears in the context menu, if SYNCMGR_IPM_PREVENT_START_SYNC is not set and if SYNCMGR_HPM_PREVENT_START_SYNC is not set on the handle, but is disabled.


### -field SYNCMGR_IPM_DISABLE_STOP_SYNC

The <b>Stop Sync</b> task should be disabled when it is shown for this sync item. With this policy set, the <b>Stop Sync</b> option appears in the context menu, if SYNCMGR_IPM_PREVENT_STOP_SYNC is not set and if SYNCMGR_HPM_PREVENT_STOP_SYNC is not set on the handler, but is disabled.


### -field SYNCMGR_IPM_DISABLE_BROWSE

The <b>Browse</b> task should be disabled when it is shown for this sync item. The <b>Browse</b> task is shown only if the SYNCMGR_ICM_CAN_BROWSE_CONTENT value is returned from the <a href="https://msdn.microsoft.com/6cb98b83-cf17-451c-ba29-700408f474c7">ISyncMgrSyncItem::GetCapabilities</a> method.


### -field SYNCMGR_IPM_DISABLE_DELETE

The handler normally supports deleting items, but that this item cannot be deleted at the time of the call. With this policy set, the <b>Delete</b> option appears as disabled in the context menu for the sync item.


### -field SYNCMGR_IPM_HIDDEN_BY_DEFAULT

The item should be hidden from the user unless the <b>Show Hidden Files</b> option has been enabled. This policy only applies the first time the item is loaded. After that, the hidden state is maintained by Sync Center and can be changed by the user through the property sheet.


### -field SYNCMGR_IPM_VALID_MASK

A mask used to retrieve valid <a href="https://msdn.microsoft.com/d894beca-855c-472f-931a-db5c6f3f891e">SYNCMGR_ITEM_POLICIES</a> flags.

