---
UID: NF:syncmgr.ISyncMgrControl.ActivateHandler
title: ISyncMgrControl::ActivateHandler (syncmgr.h)
description: Activates or deactivates a handler.
helpviewer_keywords: ["ActivateHandler","ActivateHandler method [Windows Shell]","ActivateHandler method [Windows Shell]","ISyncMgrControl interface","ISyncMgrControl interface [Windows Shell]","ActivateHandler method","ISyncMgrControl.ActivateHandler","ISyncMgrControl::ActivateHandler","_shell_ISyncMgrControl_ActivateHandler","shell.ISyncMgrControl_ActivateHandler","syncmgr/ISyncMgrControl::ActivateHandler"]
old-location: shell\ISyncMgrControl_ActivateHandler.htm
tech.root: shell
ms.assetid: 95f332a4-c76c-437f-a756-528cbbb39e2d
ms.date: 12/05/2018
ms.keywords: ActivateHandler, ActivateHandler method [Windows Shell], ActivateHandler method [Windows Shell],ISyncMgrControl interface, ISyncMgrControl interface [Windows Shell],ActivateHandler method, ISyncMgrControl.ActivateHandler, ISyncMgrControl::ActivateHandler, _shell_ISyncMgrControl_ActivateHandler, shell.ISyncMgrControl_ActivateHandler, syncmgr/ISyncMgrControl::ActivateHandler
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
 - ISyncMgrControl::ActivateHandler
 - syncmgr/ISyncMgrControl::ActivateHandler
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
 - ISyncMgrControl.ActivateHandler
---

# ISyncMgrControl::ActivateHandler


## -description

Activates or deactivates a handler.

## -parameters

### -param fActivate [in]

Type: <b>BOOL</b>

<b>TRUE</b> to activate; <b>FALSE</b> to deactivate.

### -param pszHandlerID [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the unique ID of the handler. This string is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character.

### -param hwndOwner [in]

Type: <b>HWND</b>

A handle to a window that can be used by the handler to display any necessary UI. This value can be <b>NULL</b>.

### -param nControlFlags [in]

Type: <b><a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_control_flags">SYNCMGR_CONTROL_FLAGS</a></b>

A value from the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_control_flags">SYNCMGR_CONTROL_FLAGS</a> enumeration specifying whether the activation or deactivation of the handler should be performed synchronously or asynchronously.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

An active handler appears in the Sync Center folder; an inactive handler appears in the Sync Setup folder.

If the specified handler returns <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_capabilities">SYNCMGR_HCM_QUERY_BEFORE_ACTIVATE</a> or <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_capabilities">SYNCMGR_HCM_QUERY_BEFORE_DEACTIVATE</a> in the mask returned from the <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getcapabilities">GetCapabilities</a> method, the query operation is requested before the handler is activated or deactivated. If no query UI is requested or once the user confirms the operation, the handler's <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-activate">Activate</a> method is called.

If SYNCMGR_CF_WAIT is set in the <i>nControlFlags</i> parameter, <b>ActivateHandler</b> does not return until Sync Center has processed this notification.


#### Examples



The following example shows the usage of <b>ISyncMgrControl::ActivateHandler</b> by a handler's procedure.


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
        // Tell Sync Center to activate our handler.
        hr = pControl->ActivateHandler(TRUE, 
                                       s_szMySyncHandlerID, 
                                       hwndOwner,
                                       SYNCMGR_CF_NOWAIT);
        pControl->Release();
    }

    ...

}

```