---
UID: NF:syncmgr.ISyncMgrControl.UpdateHandlerCollection
title: ISyncMgrControl::UpdateHandlerCollection (syncmgr.h)
description: Instructs Sync Center to reenumerate the handler collection, or informs it that properties of a handler in the handler collection have changed.
helpviewer_keywords: ["ISyncMgrControl interface [Windows Shell]","UpdateHandlerCollection method","ISyncMgrControl.UpdateHandlerCollection","ISyncMgrControl::UpdateHandlerCollection","UpdateHandlerCollection","UpdateHandlerCollection method [Windows Shell]","UpdateHandlerCollection method [Windows Shell]","ISyncMgrControl interface","_shell_ISyncMgrControl_UpdateHandlerCollection","shell.ISyncMgrControl_UpdateHandlerCollection","syncmgr/ISyncMgrControl::UpdateHandlerCollection"]
old-location: shell\ISyncMgrControl_UpdateHandlerCollection.htm
tech.root: shell
ms.assetid: 752f197e-0dad-4b3d-9f70-352f5f50e9ee
ms.date: 12/05/2018
ms.keywords: ISyncMgrControl interface [Windows Shell],UpdateHandlerCollection method, ISyncMgrControl.UpdateHandlerCollection, ISyncMgrControl::UpdateHandlerCollection, UpdateHandlerCollection, UpdateHandlerCollection method [Windows Shell], UpdateHandlerCollection method [Windows Shell],ISyncMgrControl interface, _shell_ISyncMgrControl_UpdateHandlerCollection, shell.ISyncMgrControl_UpdateHandlerCollection, syncmgr/ISyncMgrControl::UpdateHandlerCollection
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
 - ISyncMgrControl::UpdateHandlerCollection
 - syncmgr/ISyncMgrControl::UpdateHandlerCollection
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
 - ISyncMgrControl.UpdateHandlerCollection
---

# ISyncMgrControl::UpdateHandlerCollection


## -description

Instructs Sync Center to reenumerate the handler collection, or informs it that properties of a handler in the handler collection have changed.

## -parameters

### -param rclsidCollectionID [in]

Type: <b>REFCLSID</b>

A reference to the handler collection's CLSID.

### -param nControlFlags [in]

Type: <b><a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_control_flags">SYNCMGR_CONTROL_FLAGS</a></b>

A value from the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_control_flags">SYNCMGR_CONTROL_FLAGS</a> enumeration specifying whether the update should be performed synchronously or asynchronously.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If SYNCMGR_CF_WAIT is set in the <i>nControlFlags</i> parameter, <b>UpdateHandlerCollection</b> does not return until Sync Center has loaded the specified handler collection and reloaded all handler and item information.


#### Examples



The following example shows the usage of <b>ISyncMgrControl::UpdateHandlerCollection</b> by a handler's procedure.


```cpp
void CMyDeviceHandler::MiscProc(...)
{
    ...

    // Get the Sync Center control object.
    ISyncMgrControl *pControl = NULL;
    
    hr = CoCreateInstance(CLSID_SyncMgrControl, 
                          CLSCTX_SERVER, 
                          IID_PPV_ARGS(&pControl));
    if (SUCCEEDED(hr))
    {
        // Tell Sync Center that a new computer has been added.
        hr = pControl->UpdateHandlerCollection(CLSID_FRSHandlerCollection,
                                               SYNCMGR_CF_NOWAIT);
        pControl->Release();
    }

    ...

}

```