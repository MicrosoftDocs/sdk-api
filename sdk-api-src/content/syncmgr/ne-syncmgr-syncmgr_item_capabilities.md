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

# SYNCMGR_ITEM_CAPABILITIES enumeration


## -description


Specifies the actions that can be performed against an item.


## -enum-fields




### -field SYNCMGR_ICM_NONE

No capability flags are set.


### -field SYNCMGR_ICM_PROVIDES_ICON

The item returns a valid object from <a href="https://msdn.microsoft.com/54336c43-348b-4767-94e4-fe7dc47c0876">ISyncMgrSyncItem::GetObject</a> when that method is called with the SYNCMGR_OBJECTID_Icon flag.


### -field SYNCMGR_ICM_EVENT_STORE

The item returns a valid object from <a href="https://msdn.microsoft.com/54336c43-348b-4767-94e4-fe7dc47c0876">ISyncMgrSyncItem::GetObject</a> when that method is called with the SYNCMGR_OBJECTID_EventStore flag.


### -field SYNCMGR_ICM_CONFLICT_STORE

The item returns a valid object from <a href="https://msdn.microsoft.com/54336c43-348b-4767-94e4-fe7dc47c0876">ISyncMgrSyncItem::GetObject</a> when that method is called with the SYNCMGR_OBJECTID_ConflictStore flag.


### -field SYNCMGR_ICM_CAN_DELETE

The user is allowed to delete the item from the handler's folder. This can be used by an item to remove itself from the handler's sync set (for instance, remove a folder from the set of Offline Files). If this value is set, the <b>Delete</b> task is shown in the handler's folder when this item is selected.


### -field SYNCMGR_ICM_CAN_BROWSE_CONTENT

The item returns a valid object from <a href="https://msdn.microsoft.com/54336c43-348b-4767-94e4-fe7dc47c0876">ISyncMgrSyncItem::GetObject</a> when that method is called with the SYNCMGR_OBJECTID_BrowseContent flag. If this value is set, the <b>Browse Content</b> task is added to the item's shortcut menu.


### -field SYNCMGR_ICM_QUERY_BEFORE_ENABLE

The item returns a valid object from <a href="https://msdn.microsoft.com/54336c43-348b-4767-94e4-fe7dc47c0876">ISyncMgrSyncItem::GetObject</a> when that method is called with the SYNCMGR_OBJECTID_QueryBeforeEnable flag.


### -field SYNCMGR_ICM_QUERY_BEFORE_DISABLE

The item returns a valid object from <a href="https://msdn.microsoft.com/54336c43-348b-4767-94e4-fe7dc47c0876">ISyncMgrSyncItem::GetObject</a> when that method is called with the SYNCMGR_OBJECTID_QueryBeforeDisable flag.


### -field SYNCMGR_ICM_QUERY_BEFORE_DELETE

The item returns a valid object from <a href="https://msdn.microsoft.com/54336c43-348b-4767-94e4-fe7dc47c0876">ISyncMgrSyncItem::GetObject</a> when that method is called with the SYNCMGR_OBJECTID_QueryBeforeDelete flag.


### -field SYNCMGR_ICM_VALID_MASK

A mask used to retrieve valid <a href="https://msdn.microsoft.com/55f72e18-fba6-4a59-b553-06c6c7c3ee52">SYNCMGR_ITEM_CAPABILITIES</a> flags.


## -remarks



Sync Center queries the item for its capabilities through <a href="https://msdn.microsoft.com/6cb98b83-cf17-451c-ba29-700408f474c7">ISyncMgrSyncItem::GetCapabilities</a> whenever the <a href="https://msdn.microsoft.com/deb87d2f-74da-450a-a424-505240eadacb">ISyncMgrControl::UpdateItem</a> method is called.



