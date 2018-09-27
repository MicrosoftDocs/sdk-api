---
UID: NF:syncmgr.ISyncMgrControl.ActivateHandler
title: ISyncMgrControl::ActivateHandler
author: windows-sdk-content
description: Activates or deactivates a handler.
old-location: shell\ISyncMgrControl_ActivateHandler.htm
tech.root: shell
ms.assetid: 95f332a4-c76c-437f-a756-528cbbb39e2d
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ActivateHandler, ActivateHandler method [Windows Shell], ActivateHandler method [Windows Shell],ISyncMgrControl interface, ISyncMgrControl interface [Windows Shell],ActivateHandler method, ISyncMgrControl.ActivateHandler, ISyncMgrControl::ActivateHandler, _shell_ISyncMgrControl_ActivateHandler, shell.ISyncMgrControl_ActivateHandler, syncmgr/ISyncMgrControl::ActivateHandler
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrControl.ActivateHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

Type: <b><a href="https://msdn.microsoft.com/cfba36ba-8cbd-41ae-91ae-e568546508b9">SYNCMGR_CONTROL_FLAGS</a></b>

A value from the <a href="https://msdn.microsoft.com/cfba36ba-8cbd-41ae-91ae-e568546508b9">SYNCMGR_CONTROL_FLAGS</a> enumeration specifying whether the activation or deactivation of the handler should be performed synchronously or asynchronously.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An active handler appears in the Sync Center folder; an inactive handler appears in the Sync Setup folder.

If the specified handler returns <a href="https://msdn.microsoft.com/99b0bebf-8131-49d0-bc9d-18fdf41c1371">SYNCMGR_HCM_QUERY_BEFORE_ACTIVATE</a> or <a href="https://msdn.microsoft.com/99b0bebf-8131-49d0-bc9d-18fdf41c1371">SYNCMGR_HCM_QUERY_BEFORE_DEACTIVATE</a> in the mask returned from the <a href="https://msdn.microsoft.com/3eb43984-f284-4df9-934b-1dd2f0e62e26">GetCapabilities</a> method, the query operation is requested before the handler is activated or deactivated. If no query UI is requested or once the user confirms the operation, the handler's <a href="https://msdn.microsoft.com/0061387d-516d-44c5-b511-3236593382a9">Activate</a> method is called.

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




