---
UID: NF:syncmgr.ISyncMgrSyncCallback.ReportEvent
title: ISyncMgrSyncCallback::ReportEvent (syncmgr.h)
description: Provides an event to add to the Sync Results folder for an item being synchronized.
helpviewer_keywords: ["ISyncMgrSyncCallback interface [Windows Shell]","ReportEvent method","ISyncMgrSyncCallback.ReportEvent","ISyncMgrSyncCallback::ReportEvent","ReportEvent","ReportEvent method [Windows Shell]","ReportEvent method [Windows Shell]","ISyncMgrSyncCallback interface","_shell_ISyncMgrSyncCallback_ReportEvent","shell.ISyncMgrSyncCallback_ReportEvent","syncmgr/ISyncMgrSyncCallback::ReportEvent"]
old-location: shell\ISyncMgrSyncCallback_ReportEvent.htm
tech.root: shell
ms.assetid: 4c7d6627-1652-4920-9dce-a61673e6e656
ms.date: 12/05/2018
ms.keywords: ISyncMgrSyncCallback interface [Windows Shell],ReportEvent method, ISyncMgrSyncCallback.ReportEvent, ISyncMgrSyncCallback::ReportEvent, ReportEvent, ReportEvent method [Windows Shell], ReportEvent method [Windows Shell],ISyncMgrSyncCallback interface, _shell_ISyncMgrSyncCallback_ReportEvent, shell.ISyncMgrSyncCallback_ReportEvent, syncmgr/ISyncMgrSyncCallback::ReportEvent
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
 - ISyncMgrSyncCallback::ReportEvent
 - syncmgr/ISyncMgrSyncCallback::ReportEvent
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
 - ISyncMgrSyncCallback.ReportEvent
---

# ISyncMgrSyncCallback::ReportEvent


## -description

Provides an event to add to the Sync Results folder for an item being synchronized.

## -parameters

### -param pszItemID [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains the unique ID of the item currently being synchronized. This string is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character.

### -param nLevel [in]

Type: <b><a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_event_level">SYNCMGR_EVENT_LEVEL</a></b>

A value from the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_event_level">SYNCMGR_EVENT_LEVEL</a> enumeration declaring the type of event involved.

### -param nFlags [in]

Type: <b><a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_event_flags">SYNCMGR_EVENT_FLAGS</a></b>

Not used.

### -param pszName [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains the name of the event.

### -param pszDescription [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains a description of the event.

### -param pszLinkText [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains the text to be used in a hyperlink to the item. This parameter can be <b>NULL</b>

### -param pszLinkReference [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains the URL of the item. This parameter can be <b>NULL</b>

### -param pszContext [in]

Type: <b>LPCWSTR</b>

Handler-specific data to associate with the event.

### -param pguidEventID [out]

Type: <b>GUID*</b>

When this method returns, contains a pointer to a unique ID for the event.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For the handler to provide more details to the user about the sync result, the property sheet for individual sync results reported by the handler can be extended.

This method replaces <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-logerror">LogError</a>.

The event is stored only in memory, so all events are cleared when the user logs off or shuts down. This is one reason to implement a custom <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgreventstore">ISyncMgrEventStore</a>, which can provide its events from anywhere, including a file, over the network, or the registry. The sync results folder, however, shows events provided both by the internal event store and by custom event stores provided by sync handlers.


#### Examples



The following example shows the usage of <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynccallback-reportprogress">ISyncMgrSyncCallback::ReportProgress</a> by the <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-synchronize">Synchronize</a> method.


```cpp
STDMETHODIMP CMyDeviceHandler::Synchronize(...)
{
    ...
    // Get the event receiver interface.
    ISyncMgrEventReceiver *pEventReceiver = NULL;
    hr = pCallback->QueryInterface(IID_ISyncMgrEventReceiver,
                                   (void **) &pEventReceiver);

    ...

    // Start synchronizing the sync item.

    ...

    // Generate a GUID for this item.
    // Construct a string to display in the Sync Results folder.
    // Store the information about this event so we can display more details.
    // Report the event to Sync Center.
    hr = pEventReceiver->ReportEvent(pszItemID,
                                     SYNCMGR_EL_INFORMATION,
                                     SYNCMGR_EF_NONE,
                                     pszEventName,
                                     pszEventDescription,
                                     NULL,
                                     NULL,
                                     NULL,
                                     &guidEventID);
    ...
}

```