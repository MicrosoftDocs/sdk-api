---
UID: NN:syncmgr.ISyncMgrEventStore
title: ISyncMgrEventStore (syncmgr.h)
description: Exposes methods that allow a handler to provide its own event store and manage its own sync events, instead of using the default Sync Center event store. These events are displayed in the Sync Results folder.
helpviewer_keywords: ["ISyncMgrEventStore","ISyncMgrEventStore interface [Windows Shell]","ISyncMgrEventStore interface [Windows Shell]","described","_shell_ISyncMgrEventStore","shell.ISyncMgrEventStore","syncmgr/ISyncMgrEventStore"]
old-location: shell\ISyncMgrEventStore.htm
tech.root: shell
ms.assetid: 218875bf-be6b-4ca5-8904-81c81c7fbf70
ms.date: 12/05/2018
ms.keywords: ISyncMgrEventStore, ISyncMgrEventStore interface [Windows Shell], ISyncMgrEventStore interface [Windows Shell],described, _shell_ISyncMgrEventStore, shell.ISyncMgrEventStore, syncmgr/ISyncMgrEventStore
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISyncMgrEventStore
 - syncmgr/ISyncMgrEventStore
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrEventStore
---

# ISyncMgrEventStore interface


## -description

Exposes methods that allow a handler to provide its own event store and manage its own sync events, instead of using the default Sync Center event store. These events are displayed in the Sync Results folder.

## -inheritance

The <b>ISyncMgrEventStore</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrEventStore</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Sync Center provides a default event store that handlers can use to report events, which are then displayed in the Sync Results folder. If a component already logs events, it might be more convenient for it to provide its own event store that enumerates events for that handler. The event store in that case would simply translate the event as logged by the component into a form that can be used by Sync Center.

Sync Center requests an event store from a handler by first examining the mask returned by <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getcapabilities">ISyncMgrHandler::GetCapabilities</a> for the SYNCMGR_HCM_EVENT_STORE flag. If that value is present, Sync Center calls <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getobject">ISyncMgrHandler::GetObject</a> with the SYNCMGR_OBJECTID_EventStore value. The handler can also provide an event store filtered by item by setting the SYNCMGR_ICM_EVENT_STORE flag in the mask returned from <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-getcapabilities">ISyncMgrSyncItem::GetCapabilities</a>.

If events are added to the event store, the handler (or a related component) should call <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-updateevents">ISyncMgrControl::UpdateEvents</a> so that the Sync Results folder and the error counts can be updated.
