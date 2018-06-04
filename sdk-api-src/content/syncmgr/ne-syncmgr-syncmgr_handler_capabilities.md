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

# SYNCMGR_HANDLER_CAPABILITIES enumeration


## -description


Specifies the capabilities of a handler regarding the actions that can be performed against it.


## -enum-fields




### -field SYNCMGR_HCM_NONE

No capability flags are set.


### -field SYNCMGR_HCM_PROVIDES_ICON

The handler returns a valid object from <a href="https://msdn.microsoft.com/91441b28-a2d8-4114-86dd-9a3e826deef4">ISyncMgrHandler::GetObject</a> when that method is called with the SYNCMGR_OBJECTID_Icon flag. The object returned from <b>ISyncMgrHandler::GetObject</b> must implement <a href="https://msdn.microsoft.com/f8e0ab98-c225-4cc1-93f8-b7ab6b2f706f">IExtractIcon</a>. Generally, this value should not be returned if possible.


### -field SYNCMGR_HCM_EVENT_STORE

The handler returns a valid object from <a href="https://msdn.microsoft.com/91441b28-a2d8-4114-86dd-9a3e826deef4">ISyncMgrHandler::GetObject</a> when that method is called with the SYNCMGR_OBJECTID_EventStore flag. The object returned from <b>ISyncMgrHandler::GetObject</b> must implement <a href="https://msdn.microsoft.com/218875bf-be6b-4ca5-8904-81c81c7fbf70">ISyncMgrEventStore</a>.


### -field SYNCMGR_HCM_CONFLICT_STORE

The handler returns a valid object from <a href="https://msdn.microsoft.com/91441b28-a2d8-4114-86dd-9a3e826deef4">ISyncMgrHandler::GetObject</a> when that method is called with the SYNCMGR_OBJECTID_ConflictStore flag. The object returned from <b>ISyncMgrHandler::GetObject</b> must implement <a href="https://msdn.microsoft.com/25f47c73-eb9f-4beb-aa10-4f12b38d6507">ISyncMgrConflictStore</a>.


### -field SYNCMGR_HCM_SUPPORTS_CONCURRENT_SESSIONS

If a handler sets this flag in the mask returned from the handler's <a href="https://msdn.microsoft.com/3eb43984-f284-4df9-934b-1dd2f0e62e26">ISyncMgrHandler::GetCapabilities</a> method, it indicates that the handler plans to create multiple simultaneous synchronization sessions using <a href="https://msdn.microsoft.com/d1df43b6-406c-4da0-89f0-a17e51101520">ISyncMgrSessionCreator::CreateSession</a>. This is useful for handlers that implement a background synchronization architecture in which the handler simply signals another process to perform the synchronization rather than performing the synchronization in its <a href="https://msdn.microsoft.com/6742f6a8-eda8-4ef0-8a11-dc70baefcc83">ISyncMgrHandler::Synchronize</a> method directly. This allows synchronization engines to report progress, conflicts, and events (through <a href="https://msdn.microsoft.com/4f2b6dc3-3b81-4c0a-b0a2-b48f13fba397">ISyncMgrSyncCallback</a>) when synchronization requests come from sources other than Sync Center. For example, this could be the result of a data change notification or through application-specific UI. If more than one session is synchronizing the same item, then the progress for that item will be reported as indeterminate.


### -field SYNCMGR_HCM_CAN_BROWSE_CONTENT

The handler returns a valid object from <a href="https://msdn.microsoft.com/91441b28-a2d8-4114-86dd-9a3e826deef4">ISyncMgrHandler::GetObject</a> when that method is called with the SYNCMGR_OBJECTID_BrowseContent flag. If this value is set, the <b>Browse Content</b> task is added to the handler's shortcut menu. The object returned from <b>ISyncMgrHandler::GetObject</b> must implement <a href="https://msdn.microsoft.com/6fa4b0ac-3c75-4cda-b20d-582a3e18fb28">ISyncMgrUIOperation</a>.


### -field SYNCMGR_HCM_CAN_SHOW_SCHEDULE

The handler returns a valid object from <a href="https://msdn.microsoft.com/91441b28-a2d8-4114-86dd-9a3e826deef4">ISyncMgrHandler::GetObject</a> when that method is called with the SYNCMGR_OBJECTID_ShowSchedule flag. If this value is set, the <b>Show Schedule</b> task is added to the handler's shortcut menu. The object returned from <b>ISyncMgrHandler::GetObject</b> must implement <a href="https://msdn.microsoft.com/6fa4b0ac-3c75-4cda-b20d-582a3e18fb28">ISyncMgrUIOperation</a>. This value is used by <a href="https://msdn.microsoft.com/dcbe22fb-624f-4784-b1c3-5c463d6502a3">ISyncMgrScheduleWizardUIOperation</a>.


### -field SYNCMGR_HCM_QUERY_BEFORE_ACTIVATE

The handler returns a valid object from <a href="https://msdn.microsoft.com/91441b28-a2d8-4114-86dd-9a3e826deef4">ISyncMgrHandler::GetObject</a> when that method is called with the SYNCMGR_OBJECTID_QueryBeforeActivate flag. The object returned from <b>ISyncMgrHandler::GetObject</b> must implement <a href="https://msdn.microsoft.com/6fa4b0ac-3c75-4cda-b20d-582a3e18fb28">ISyncMgrUIOperation</a>.


### -field SYNCMGR_HCM_QUERY_BEFORE_DEACTIVATE

The handler returns a valid object from <a href="https://msdn.microsoft.com/91441b28-a2d8-4114-86dd-9a3e826deef4">ISyncMgrHandler::GetObject</a> when that method is called with the SYNCMGR_OBJECTID_QueryBeforeDeactivate flag. The object returned from <b>ISyncMgrHandler::GetObject</b> must implement <a href="https://msdn.microsoft.com/6fa4b0ac-3c75-4cda-b20d-582a3e18fb28">ISyncMgrUIOperation</a>.


### -field SYNCMGR_HCM_QUERY_BEFORE_ENABLE

The handler returns a valid object from <a href="https://msdn.microsoft.com/91441b28-a2d8-4114-86dd-9a3e826deef4">ISyncMgrHandler::GetObject</a> when that method is called with the SYNCMGR_OBJECTID_QueryBeforeEnable flag. The object returned from <b>ISyncMgrHandler::GetObject</b> must implement <a href="https://msdn.microsoft.com/6fa4b0ac-3c75-4cda-b20d-582a3e18fb28">ISyncMgrUIOperation</a>.


### -field SYNCMGR_HCM_QUERY_BEFORE_DISABLE

The handler returns a valid object from <a href="https://msdn.microsoft.com/91441b28-a2d8-4114-86dd-9a3e826deef4">ISyncMgrHandler::GetObject</a> when that method is called with the SYNCMGR_OBJECTID_QueryBeforeDisable flag. The object returned from <b>ISyncMgrHandler::GetObject</b> must implement <a href="https://msdn.microsoft.com/6fa4b0ac-3c75-4cda-b20d-582a3e18fb28">ISyncMgrUIOperation</a>.


### -field SYNCMGR_HCM_VALID_MASK

A mask used to determine valid <a href="https://msdn.microsoft.com/99b0bebf-8131-49d0-bc9d-18fdf41c1371">SYNCMGR_HANDLER_CAPABILITIES</a> flags. Compare against the value retrieved by <a href="https://msdn.microsoft.com/3eb43984-f284-4df9-934b-1dd2f0e62e26">ISyncMgrHandler::GetCapabilities</a> to verify valid results.


## -remarks



Sync Center queries the handler for its capabilities through <a href="https://msdn.microsoft.com/3eb43984-f284-4df9-934b-1dd2f0e62e26">ISyncMgrHandler::GetCapabilities</a> whenever the <a href="https://msdn.microsoft.com/d961aef7-c559-4caa-894e-e86836b142c0">ISyncMgrControl::UpdateHandler</a> or <a href="https://msdn.microsoft.com/752f197e-0dad-4b3d-9f70-352f5f50e9ee">ISyncMgrControl::UpdateHandlerCollection</a> method is called.



