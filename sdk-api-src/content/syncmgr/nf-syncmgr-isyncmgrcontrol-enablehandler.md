---
UID: NF:syncmgr.ISyncMgrControl.EnableHandler
title: ISyncMgrControl::EnableHandler (syncmgr.h)
description: Enables or disables a handler.
helpviewer_keywords: ["EnableHandler","EnableHandler method [Windows Shell]","EnableHandler method [Windows Shell]","ISyncMgrControl interface","ISyncMgrControl interface [Windows Shell]","EnableHandler method","ISyncMgrControl.EnableHandler","ISyncMgrControl::EnableHandler","_shell_ISyncMgrControl_EnableHandler","shell.ISyncMgrControl_EnableHandler","syncmgr/ISyncMgrControl::EnableHandler"]
old-location: shell\ISyncMgrControl_EnableHandler.htm
tech.root: shell
ms.assetid: 92a9525c-bf06-4720-a3e2-5352fa693c8e
ms.date: 12/05/2018
ms.keywords: EnableHandler, EnableHandler method [Windows Shell], EnableHandler method [Windows Shell],ISyncMgrControl interface, ISyncMgrControl interface [Windows Shell],EnableHandler method, ISyncMgrControl.EnableHandler, ISyncMgrControl::EnableHandler, _shell_ISyncMgrControl_EnableHandler, shell.ISyncMgrControl_EnableHandler, syncmgr/ISyncMgrControl::EnableHandler
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
 - ISyncMgrControl::EnableHandler
 - syncmgr/ISyncMgrControl::EnableHandler
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
 - ISyncMgrControl.EnableHandler
---

# ISyncMgrControl::EnableHandler


## -description

Enables or disables a handler.

## -parameters

### -param fEnable [in]

Type: <b>BOOL</b>

<b>TRUE</b> to enable; <b>FALSE</b> to disable.

### -param pszHandlerID [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the unique ID of the handler. This string is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character.

### -param hwndOwner [in]

Type: <b>HWND</b>

A handle to a window that can be used by the handler to display any necessary UI. This value can be <b>NULL</b>.

### -param nControlFlags [in]

Type: <b><a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_control_flags">SYNCMGR_CONTROL_FLAGS</a></b>

A value from the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_control_flags">SYNCMGR_CONTROL_FLAGS</a> enumeration specifying whether the enabling or disabling of the handler should be performed synchronously or asynchronously.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

An active handler appears in the Sync Center folder; an inactive handler appears in the Sync Setup folder.

If the specified handler returns <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_capabilities">SYNCMGR_HCM_QUERY_BEFORE_ENABLE</a> or <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_capabilities">SYNCMGR_HCM_QUERY_BEFORE_DISABLE</a> in the mask returned from the <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getcapabilities">GetCapabilities</a> method, the user is presented with a confirmation dialog requested before the handler is enabled or disabled. If no query UI is requested or once the user confirms the operation, the handler's <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-enable">Enable</a> method is called.

If SYNCMGR_CF_WAIT is set in the <i>nControlFlags</i> parameter, <b>EnableHandler</b> does not return until Sync Center has processed this notification.


#### Examples



The following example shows the usage of <b>ISyncMgrControl::EnableHandler</b> by a handler's procedure.


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
        // Tell Sync Center to enable our handler.
        hr = pControl->EnableHandler(TRUE, 
                                     s_szMySyncHandlerID, 
                                     hwnd,
                                     SYNCMGR_CF_NOWAIT);
        pControl->Release();
    }

    ...

}

```