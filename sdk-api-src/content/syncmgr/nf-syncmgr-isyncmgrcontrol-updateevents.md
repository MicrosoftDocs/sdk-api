---
UID: NF:syncmgr.ISyncMgrControl.UpdateEvents
title: ISyncMgrControl::UpdateEvents (syncmgr.h)
description: Informs Sync Center that events have been added for a specific handler or item.
helpviewer_keywords: ["ISyncMgrControl interface [Windows Shell]","UpdateEvents method","ISyncMgrControl.UpdateEvents","ISyncMgrControl::UpdateEvents","UpdateEvents","UpdateEvents method [Windows Shell]","UpdateEvents method [Windows Shell]","ISyncMgrControl interface","_shell_ISyncMgrControl_UpdateEvents","shell.ISyncMgrControl_UpdateEvents","syncmgr/ISyncMgrControl::UpdateEvents"]
old-location: shell\ISyncMgrControl_UpdateEvents.htm
tech.root: shell
ms.assetid: 72848e6a-eec3-45fc-b599-a5a8da2e1070
ms.date: 12/05/2018
ms.keywords: ISyncMgrControl interface [Windows Shell],UpdateEvents method, ISyncMgrControl.UpdateEvents, ISyncMgrControl::UpdateEvents, UpdateEvents, UpdateEvents method [Windows Shell], UpdateEvents method [Windows Shell],ISyncMgrControl interface, _shell_ISyncMgrControl_UpdateEvents, shell.ISyncMgrControl_UpdateEvents, syncmgr/ISyncMgrControl::UpdateEvents
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
 - ISyncMgrControl::UpdateEvents
 - syncmgr/ISyncMgrControl::UpdateEvents
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
 - ISyncMgrControl.UpdateEvents
---

# ISyncMgrControl::UpdateEvents


## -description

Informs Sync Center that events have been added for a specific handler or item.

## -parameters

### -param pszHandlerID [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the unique ID of the handler that manages the item. This string is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character.

### -param pszItemID [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the unique ID of the item. This string is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character. This parameter can be <b>NULL</b> if the event occurred on the handler rather than on a specific item.

### -param nControlFlags [in]

Type: <b><a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_control_flags">SYNCMGR_CONTROL_FLAGS</a></b>

A value from the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_control_flags">SYNCMGR_CONTROL_FLAGS</a> enumeration specifying whether the update should be performed synchronously or asynchronously.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If SYNCMGR_CF_WAIT is set in the <i>nControlFlags</i> parameter, <b>UpdateEvents</b> does not return until Sync Center has loaded the specified handler, retrieved the handler's event store, and reloaded all events from that store. If the handler is provided by a handler collection, the handler collection is also loaded to reload the handler.


#### Examples



The following example shows the usage of <b>ISyncMgrControl::UpdateEvents</b> by a handler's procedure.


```cpp
void CMyDeviceHandler::Synchronize(...)
{
    ...
    // Add events to the event store.

    // Get the Sync Center control object.
    ISyncMgrControl *pControl = NULL;
    
    hr = CoCreateInstance(CLSID_SyncMgrControl, 
                          CLSCTX_SERVER, 
                          IID_PPV_ARGS(&pControl));
    if (SUCCEEDED(hr))
    {
        // Tell Sync Center that we added events to our event store.
        // By passing NULL in pszItemID, we tell Sync Center that the event
        // occurred on the handler rather than a specific item.
        hr = pControl->UpdateEvents(s_szMyDeviceSyncHandlerID, 
                                    NULL,
                                    SYNCMGR_CF_NOWAIT);
        pControl->Release();
    }

    ...

}

```