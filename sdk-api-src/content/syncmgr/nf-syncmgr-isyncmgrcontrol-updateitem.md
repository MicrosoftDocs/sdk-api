---
UID: NF:syncmgr.ISyncMgrControl.UpdateItem
title: ISyncMgrControl::UpdateItem (syncmgr.h)
description: Informs Sync Center that properties of a sync item have changed.
helpviewer_keywords: ["ISyncMgrControl interface [Windows Shell]","UpdateItem method","ISyncMgrControl.UpdateItem","ISyncMgrControl::UpdateItem","UpdateItem","UpdateItem method [Windows Shell]","UpdateItem method [Windows Shell]","ISyncMgrControl interface","_shell_ISyncMgrControl_UpdateItem","shell.ISyncMgrControl_UpdateItem","syncmgr/ISyncMgrControl::UpdateItem"]
old-location: shell\ISyncMgrControl_UpdateItem.htm
tech.root: shell
ms.assetid: deb87d2f-74da-450a-a424-505240eadacb
ms.date: 12/05/2018
ms.keywords: ISyncMgrControl interface [Windows Shell],UpdateItem method, ISyncMgrControl.UpdateItem, ISyncMgrControl::UpdateItem, UpdateItem, UpdateItem method [Windows Shell], UpdateItem method [Windows Shell],ISyncMgrControl interface, _shell_ISyncMgrControl_UpdateItem, shell.ISyncMgrControl_UpdateItem, syncmgr/ISyncMgrControl::UpdateItem
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
 - ISyncMgrControl::UpdateItem
 - syncmgr/ISyncMgrControl::UpdateItem
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
 - ISyncMgrControl.UpdateItem
---

# ISyncMgrControl::UpdateItem


## -description

Informs Sync Center that properties of a sync item have changed.

## -parameters

### -param pszHandlerID [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the unique ID of the handler that manages the item. This string is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character.

### -param pszItemID [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the unique ID of the item. This string is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character.

### -param nControlFlags [in]

Type: <b><a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_control_flags">SYNCMGR_CONTROL_FLAGS</a></b>

A value from the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_control_flags">SYNCMGR_CONTROL_FLAGS</a> enumeration specifying whether the update should be performed synchronously or asynchronously.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If SYNCMGR_CF_WAIT is set in the <i>nControlFlags</i> parameter, <b>UpdateItem</b> does not return until Sync Center has loaded the specified handler and reloaded all handler and item information. If the handler is provided by a handler collection, the handler collection is also loaded to reload the handler.


#### Examples



The following example shows the usage of <b>ISyncMgrControl::UpdateItem</b> by a handler's procedure.


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
        // Tell Sync Center that properties of the item have changed.
        hr = pControl->UpdateItem(s_szMySyncHandlerID,
                                  s_szMySyncHandlerMusicContentID,
                                  SYNCMGR_CF_WAIT);
        pControl->Release();
    }

    ...

}

```