---
UID: NF:syncmgr.ISyncMgrControl.UpdateHandler
title: ISyncMgrControl::UpdateHandler (syncmgr.h)
description: Instructs Sync Center to reenumerate the items managed by a handler or informs it that properties of the handler have changed.
helpviewer_keywords: ["ISyncMgrControl interface [Windows Shell]","UpdateHandler method","ISyncMgrControl.UpdateHandler","ISyncMgrControl::UpdateHandler","UpdateHandler","UpdateHandler method [Windows Shell]","UpdateHandler method [Windows Shell]","ISyncMgrControl interface","_shell_ISyncMgrControl_UpdateHandler","shell.ISyncMgrControl_UpdateHandler","syncmgr/ISyncMgrControl::UpdateHandler"]
old-location: shell\ISyncMgrControl_UpdateHandler.htm
tech.root: shell
ms.assetid: d961aef7-c559-4caa-894e-e86836b142c0
ms.date: 12/05/2018
ms.keywords: ISyncMgrControl interface [Windows Shell],UpdateHandler method, ISyncMgrControl.UpdateHandler, ISyncMgrControl::UpdateHandler, UpdateHandler, UpdateHandler method [Windows Shell], UpdateHandler method [Windows Shell],ISyncMgrControl interface, _shell_ISyncMgrControl_UpdateHandler, shell.ISyncMgrControl_UpdateHandler, syncmgr/ISyncMgrControl::UpdateHandler
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
 - ISyncMgrControl::UpdateHandler
 - syncmgr/ISyncMgrControl::UpdateHandler
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
 - ISyncMgrControl.UpdateHandler
---

# ISyncMgrControl::UpdateHandler


## -description

Instructs Sync Center to reenumerate the items managed by a handler or informs it that properties of the handler have changed.

## -parameters

### -param pszHandlerID [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the unique ID of the handler. This string is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character.

### -param nControlFlags [in]

Type: <b><a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_control_flags">SYNCMGR_CONTROL_FLAGS</a></b>

A value from the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_control_flags">SYNCMGR_CONTROL_FLAGS</a> enumeration specifying whether the update should be performed synchronously or asynchronously.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If SYNCMGR_CF_WAIT is set in the <i>nControlFlags</i> parameter, <b>UpdateHandler</b> does not return until Sync Center has loaded the specified handler and reloaded all handler and item information. If the handler is provided by a handler collection, the handler collection is also loaded to reload the handler.


#### Examples



The following example shows the usage of <b>ISyncMgrControl::UpdateHandler</b> by a handler's procedure.


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
        // Tell Sync Center that properties on the handler have changed.
        hr = pControl->UpdateHandler(s_szMySyncHandlerID, SYNCMGR_CF_WAIT);
        pControl->Release();
    }

    ...

}

```