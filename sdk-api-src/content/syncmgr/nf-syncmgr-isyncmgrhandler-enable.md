---
UID: NF:syncmgr.ISyncMgrHandler.Enable
title: ISyncMgrHandler::Enable (syncmgr.h)
description: Requests that an active handler be enabled or disabled. An enabled handler can be synchronized and a disabled handler cannot.
helpviewer_keywords: ["Enable","Enable method [Windows Shell]","Enable method [Windows Shell]","ISyncMgrHandler interface","ISyncMgrHandler interface [Windows Shell]","Enable method","ISyncMgrHandler.Enable","ISyncMgrHandler::Enable","_shell_ISyncMgrHandler_Enable","shell.ISyncMgrHandler_Enable","syncmgr/ISyncMgrHandler::Enable"]
old-location: shell\ISyncMgrHandler_Enable.htm
tech.root: shell
ms.assetid: ea3efba1-9b7c-4f93-aca5-08475a6005a8
ms.date: 12/05/2018
ms.keywords: Enable, Enable method [Windows Shell], Enable method [Windows Shell],ISyncMgrHandler interface, ISyncMgrHandler interface [Windows Shell],Enable method, ISyncMgrHandler.Enable, ISyncMgrHandler::Enable, _shell_ISyncMgrHandler_Enable, shell.ISyncMgrHandler_Enable, syncmgr/ISyncMgrHandler::Enable
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
 - ISyncMgrHandler::Enable
 - syncmgr/ISyncMgrHandler::Enable
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
 - ISyncMgrHandler.Enable
---

# ISyncMgrHandler::Enable


## -description

Requests that an <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-activate">active</a> handler be enabled or disabled. An enabled handler can be synchronized and a disabled handler cannot.

## -parameters

### -param fEnable [in]

Type: <b>BOOL</b>

<b>TRUE</b> to enable; <b>FALSE</b> to disable.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A handler must set the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_capabilities">SYNCMGR_HCM_CAN_ENABLE</a> and <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_capabilities">SYNCMGR_HCM_CAN_DISABLE</a> flags for the <b>Enable</b> and <b>Disable</b> entries to appear on the handler's shortcut menu when the handler is shown in the Sync Center folder. Choosing to enable a handler means that it can be synchronized; choosing to disable a handler means that it cannot.

Sync Center calls this method in the following two instances.
            
                

<ul>
<li>When the user selects the handler in the Sync Center folder and launches its <b>Enable</b> task. If the handler supports the <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getobject">SYNCMGR_OBJECTID_QueryBeforeEnable</a> object, this method is only called if the UI operation was successful.</li>
<li>When the user selects the handler in the Sync Center folder and launches its <b>Disable</b> task. If the handler supports the <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getobject">SYNCMGR_OBJECTID_QueryBeforeDisable</a> object, this method is only called if the UI operation was successful.</li>
</ul>
If the handler does not need to perform any actions when it is activated, it can return either S_OK or E_NOTIMPL as shown in the example below.


#### Examples



The following example shows a simple implementation of this method.


```cpp
STDMETHODIMP CMyDeviceHandler::Enable(__in BOOL fEnable)
{
    return E_NOTIMPL;
}

```

## -see-also

<a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrhandler">ISyncMgrHandler</a>



<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getobject">ISyncMgrHandler::GetObject</a>



<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandlerinfo-isenabled">IsEnabled</a>