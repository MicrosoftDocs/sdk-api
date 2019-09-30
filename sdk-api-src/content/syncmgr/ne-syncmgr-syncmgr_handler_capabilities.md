---
UID: NE:syncmgr.SYNCMGR_HANDLER_CAPABILITIES
title: SYNCMGR_HANDLER_CAPABILITIES (syncmgr.h)
author: windows-sdk-content
description: Specifies the capabilities of a handler regarding the actions that can be performed against it.
old-location: shell\SYNCMGR_HANDLER_CAPABILITIES.htm
tech.root: shell
ms.assetid: 99b0bebf-8131-49d0-bc9d-18fdf41c1371
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SYNCMGR_HANDLER_CAPABILITIES, SYNCMGR_HANDLER_CAPABILITIES enumeration [Windows Shell], SYNCMGR_HCM_CAN_BROWSE_CONTENT, SYNCMGR_HCM_CAN_SHOW_SCHEDULE, SYNCMGR_HCM_CONFLICT_STORE, SYNCMGR_HCM_EVENT_STORE, SYNCMGR_HCM_NONE, SYNCMGR_HCM_PROVIDES_ICON, SYNCMGR_HCM_QUERY_BEFORE_ACTIVATE, SYNCMGR_HCM_QUERY_BEFORE_DEACTIVATE, SYNCMGR_HCM_QUERY_BEFORE_DISABLE, SYNCMGR_HCM_QUERY_BEFORE_ENABLE, SYNCMGR_HCM_SUPPORTS_CONCURRENT_SESSIONS, SYNCMGR_HCM_VALID_MASK, shell.SYNCMGR_HANDLER_CAPABILITIES, shell_SYNCMGR_HANDLER_CAPABILITIES, syncmgr/SYNCMGR_HANDLER_CAPABILITIES, syncmgr/SYNCMGR_HCM_CAN_BROWSE_CONTENT, syncmgr/SYNCMGR_HCM_CAN_SHOW_SCHEDULE, syncmgr/SYNCMGR_HCM_CONFLICT_STORE, syncmgr/SYNCMGR_HCM_EVENT_STORE, syncmgr/SYNCMGR_HCM_NONE, syncmgr/SYNCMGR_HCM_PROVIDES_ICON, syncmgr/SYNCMGR_HCM_QUERY_BEFORE_ACTIVATE, syncmgr/SYNCMGR_HCM_QUERY_BEFORE_DEACTIVATE, syncmgr/SYNCMGR_HCM_QUERY_BEFORE_DISABLE, syncmgr/SYNCMGR_HCM_QUERY_BEFORE_ENABLE, syncmgr/SYNCMGR_HCM_SUPPORTS_CONCURRENT_SESSIONS, syncmgr/SYNCMGR_HCM_VALID_MASK
ms.topic: enum
f1_keywords: 
 - "syncmgr/SYNCMGR_HANDLER_CAPABILITIES"
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
 - SYNCMGR_HANDLER_CAPABILITIES
targetos: Windows
req.typenames: SYNCMGR_HANDLER_CAPABILITIES
req.redist: 
ms.custom: 19H1
---

# SYNCMGR_HANDLER_CAPABILITIES enumeration


## -description


Specifies the capabilities of a handler regarding the actions that can be performed against it.


## -enum-fields




### -field SYNCMGR_HCM_NONE

No capability flags are set.


### -field SYNCMGR_HCM_PROVIDES_ICON

The handler returns a valid object from <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getobject">ISyncMgrHandler::GetObject</a> when that method is called with the SYNCMGR_OBJECTID_Icon flag. The object returned from <b>ISyncMgrHandler::GetObject</b> must implement <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nn-shlobj_core-iextracticona">IExtractIcon</a>. Generally, this value should not be returned if possible.


### -field SYNCMGR_HCM_EVENT_STORE

The handler returns a valid object from <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getobject">ISyncMgrHandler::GetObject</a> when that method is called with the SYNCMGR_OBJECTID_EventStore flag. The object returned from <b>ISyncMgrHandler::GetObject</b> must implement <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgreventstore">ISyncMgrEventStore</a>.


### -field SYNCMGR_HCM_CONFLICT_STORE

The handler returns a valid object from <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getobject">ISyncMgrHandler::GetObject</a> when that method is called with the SYNCMGR_OBJECTID_ConflictStore flag. The object returned from <b>ISyncMgrHandler::GetObject</b> must implement <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrconflictstore">ISyncMgrConflictStore</a>.


### -field SYNCMGR_HCM_SUPPORTS_CONCURRENT_SESSIONS

If a handler sets this flag in the mask returned from the handler's <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getcapabilities">ISyncMgrHandler::GetCapabilities</a> method, it indicates that the handler plans to create multiple simultaneous synchronization sessions using <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsessioncreator-createsession">ISyncMgrSessionCreator::CreateSession</a>. This is useful for handlers that implement a background synchronization architecture in which the handler simply signals another process to perform the synchronization rather than performing the synchronization in its <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-synchronize">ISyncMgrHandler::Synchronize</a> method directly. This allows synchronization engines to report progress, conflicts, and events (through <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrsynccallback">ISyncMgrSyncCallback</a>) when synchronization requests come from sources other than Sync Center. For example, this could be the result of a data change notification or through application-specific UI. If more than one session is synchronizing the same item, then the progress for that item will be reported as indeterminate.


### -field SYNCMGR_HCM_CAN_BROWSE_CONTENT

The handler returns a valid object from <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getobject">ISyncMgrHandler::GetObject</a> when that method is called with the SYNCMGR_OBJECTID_BrowseContent flag. If this value is set, the <b>Browse Content</b> task is added to the handler's shortcut menu. The object returned from <b>ISyncMgrHandler::GetObject</b> must implement <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgruioperation">ISyncMgrUIOperation</a>.


### -field SYNCMGR_HCM_CAN_SHOW_SCHEDULE

The handler returns a valid object from <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getobject">ISyncMgrHandler::GetObject</a> when that method is called with the SYNCMGR_OBJECTID_ShowSchedule flag. If this value is set, the <b>Show Schedule</b> task is added to the handler's shortcut menu. The object returned from <b>ISyncMgrHandler::GetObject</b> must implement <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgruioperation">ISyncMgrUIOperation</a>. This value is used by <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrschedulewizarduioperation">ISyncMgrScheduleWizardUIOperation</a>.


### -field SYNCMGR_HCM_QUERY_BEFORE_ACTIVATE

The handler returns a valid object from <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getobject">ISyncMgrHandler::GetObject</a> when that method is called with the SYNCMGR_OBJECTID_QueryBeforeActivate flag. The object returned from <b>ISyncMgrHandler::GetObject</b> must implement <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgruioperation">ISyncMgrUIOperation</a>.


### -field SYNCMGR_HCM_QUERY_BEFORE_DEACTIVATE

The handler returns a valid object from <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getobject">ISyncMgrHandler::GetObject</a> when that method is called with the SYNCMGR_OBJECTID_QueryBeforeDeactivate flag. The object returned from <b>ISyncMgrHandler::GetObject</b> must implement <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgruioperation">ISyncMgrUIOperation</a>.


### -field SYNCMGR_HCM_QUERY_BEFORE_ENABLE

The handler returns a valid object from <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getobject">ISyncMgrHandler::GetObject</a> when that method is called with the SYNCMGR_OBJECTID_QueryBeforeEnable flag. The object returned from <b>ISyncMgrHandler::GetObject</b> must implement <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgruioperation">ISyncMgrUIOperation</a>.


### -field SYNCMGR_HCM_QUERY_BEFORE_DISABLE

The handler returns a valid object from <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getobject">ISyncMgrHandler::GetObject</a> when that method is called with the SYNCMGR_OBJECTID_QueryBeforeDisable flag. The object returned from <b>ISyncMgrHandler::GetObject</b> must implement <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgruioperation">ISyncMgrUIOperation</a>.


### -field SYNCMGR_HCM_VALID_MASK

A mask used to determine valid <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_capabilities">SYNCMGR_HANDLER_CAPABILITIES</a> flags. Compare against the value retrieved by <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getcapabilities">ISyncMgrHandler::GetCapabilities</a> to verify valid results.


## -remarks



Sync Center queries the handler for its capabilities through <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getcapabilities">ISyncMgrHandler::GetCapabilities</a> whenever the <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-updatehandler">ISyncMgrControl::UpdateHandler</a> or <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-updatehandlercollection">ISyncMgrControl::UpdateHandlerCollection</a> method is called.



