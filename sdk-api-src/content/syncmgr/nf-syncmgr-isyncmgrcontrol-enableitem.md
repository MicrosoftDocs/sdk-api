---
UID: NF:syncmgr.ISyncMgrControl.EnableItem
title: ISyncMgrControl::EnableItem (syncmgr.h)
description: Enables or disables a sync item managed by a specified handler.
helpviewer_keywords: ["EnableItem","EnableItem method [Windows Shell]","EnableItem method [Windows Shell]","ISyncMgrControl interface","ISyncMgrControl interface [Windows Shell]","EnableItem method","ISyncMgrControl.EnableItem","ISyncMgrControl::EnableItem","_shell_ISyncMgrControl_EnableItem","shell.ISyncMgrControl_EnableItem","syncmgr/ISyncMgrControl::EnableItem"]
old-location: shell\ISyncMgrControl_EnableItem.htm
tech.root: shell
ms.assetid: 2e88fb21-201c-47b9-b341-1a8d9358a455
ms.date: 12/05/2018
ms.keywords: EnableItem, EnableItem method [Windows Shell], EnableItem method [Windows Shell],ISyncMgrControl interface, ISyncMgrControl interface [Windows Shell],EnableItem method, ISyncMgrControl.EnableItem, ISyncMgrControl::EnableItem, _shell_ISyncMgrControl_EnableItem, shell.ISyncMgrControl_EnableItem, syncmgr/ISyncMgrControl::EnableItem
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
 - ISyncMgrControl::EnableItem
 - syncmgr/ISyncMgrControl::EnableItem
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
 - ISyncMgrControl.EnableItem
---

# ISyncMgrControl::EnableItem


## -description

Enables or disables a sync item managed by a specified handler.

## -parameters

### -param fEnable [in]

Type: <b>BOOL</b>

<b>TRUE</b> to enable; <b>FALSE</b> to disable.

### -param pszHandlerID [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the unique ID of the handler. This string is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character.

### -param pszItemID [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the unique ID of the item. This string is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character.

### -param hwndOwner [in]

Type: <b>HWND</b>

A handle to a window that can be used by the item to display any necessary UI. This value can be <b>NULL</b>.

### -param nControlFlags [in]

Type: <b><a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_control_flags">SYNCMGR_CONTROL_FLAGS</a></b>

A value from the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_control_flags">SYNCMGR_CONTROL_FLAGS</a> enumeration specifying whether the enabling or disabling of the item should be performed synchronously or asynchronously.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

An <i>enabled</i> item is an item that can be synchronized.

If the specified item returns <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_item_capabilities">SYNCMGR_ICM_QUERY_BEFORE_ENABLE</a> or <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_item_capabilities">SYNCMGR_ICM_QUERY_BEFORE_DISABLE</a> in the mask returned from the <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-getcapabilities">GetCapabilities</a> method, the user is presented with a confirmation dialog box requested before the item is enabled or disabled. If no query UI is requested or once the user confirms the operation, the item's <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-enable">Enable</a> method is called.

If SYNCMGR_CF_WAIT is set in the <i>nControlFlags</i> parameter, <b>EnableItem</b> does not return until Sync Center has processed this notification.


#### Examples



The following example shows the usage of <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-enablehandler">ISyncMgrControl::EnableHandler</a> by a handler's procedure.


```cpp
void MiscProc(...)
{
    ...

    // Get the Sync Center control object.
    ISyncMgrControl *pControl = NULL;
    
    hr = CoCreateInstance(CLSID_SyncMgrControl, 
                          CLSCTX_SERVER, 
                          IID_PPV_ARGS(&pControl));
    if (SUCCEEDED(hr))
    {
        // Tell Sync Center to disable the item.
        hr = pControl->EnableItem(FALSE, 
                                  s_szMySyncHandlerID,
                                  s_szMySyncHandlerMusicContentID, 
                                  hwnd,
                                  SYNCMGR_CF_WAIT);
        pControl->Release();
    }

    ...

}

```