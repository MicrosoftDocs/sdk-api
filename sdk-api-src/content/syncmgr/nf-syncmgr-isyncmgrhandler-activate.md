---
UID: NF:syncmgr.ISyncMgrHandler.Activate
title: ISyncMgrHandler::Activate (syncmgr.h)
description: Requests that the handler is activated or deactivated. An active handler can be synchronized; an inactive handler cannot.
helpviewer_keywords: ["Activate","Activate method [Windows Shell]","Activate method [Windows Shell]","ISyncMgrHandler interface","ISyncMgrHandler interface [Windows Shell]","Activate method","ISyncMgrHandler.Activate","ISyncMgrHandler::Activate","_shell_ISyncMgrHandler_Activate","shell.ISyncMgrHandler_Activate","syncmgr/ISyncMgrHandler::Activate"]
old-location: shell\ISyncMgrHandler_Activate.htm
tech.root: shell
ms.assetid: 0061387d-516d-44c5-b511-3236593382a9
ms.date: 12/05/2018
ms.keywords: Activate, Activate method [Windows Shell], Activate method [Windows Shell],ISyncMgrHandler interface, ISyncMgrHandler interface [Windows Shell],Activate method, ISyncMgrHandler.Activate, ISyncMgrHandler::Activate, _shell_ISyncMgrHandler_Activate, shell.ISyncMgrHandler_Activate, syncmgr/ISyncMgrHandler::Activate
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
 - ISyncMgrHandler::Activate
 - syncmgr/ISyncMgrHandler::Activate
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
 - ISyncMgrHandler.Activate
---

# ISyncMgrHandler::Activate


## -description

Requests that the handler is activated or deactivated. An active handler can be synchronized; an inactive handler cannot.

## -parameters

### -param fActivate [in]

Type: <b>BOOL</b>

<b>TRUE</b> to activate; <b>FALSE</b> to deactivate.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

An active handler appears in the Sync Center folder and can be synchronized. An inactive handler appears in the Sync Setup folder and must be activated (which moves it to the Sync Center folder) before it can be synchronized.

The activation state should not be confused with the enabled state. An active handler can be disabled. This means that it is still shown in the Sync Center folder but that it cannot be synchronized.

Sync Center calls this method in the following two instances.
            
                

<ul>
<li>When the user selects the handler in the Sync Setup folder and launches its <b>Setup</b> task. If the handler supports the <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getobject">SYNCMGR_OBJECTID_QueryBeforeActivate</a> object, this method is only called if the UI operation, which consists of a dialog asking the user to confirm whether they want to activate the handler, was successful.</li>
<li>When the user selects the handler in the Sync Center folder and launches its <b>Delete</b> task, but only if the handler has not set the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_policies">SYNCMGR_HPM_PREVENT_DEACTIVATE</a> flag. If the handler supports the <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getobject">SYNCMGR_OBJECTID_QueryBeforeDeactivate</a> object, this method is only called if the UI operation was successful.</li>
</ul>
If the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_policies">SYNCMGR_HPM_PREVENT_ACTIVATE</a> flag is set in the value retrieved by <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getcapabilities">ISyncMgrHandler::GetCapabilities</a>, a call to this method requesting activation of the handler will fail.

The activation state of an individual handler can be found by calling <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandlerinfo-isactive">IsActive</a>.

If the handler does not need to perform any actions when it is activated, it can return either S_OK or E_NOTIMPL as shown in the example below.


#### Examples



The following example shows a simple implementation of this method.


```cpp
STDMETHODIMP CMyDeviceHandler::Activate(__in BOOL fActivate)
{
    return E_NOTIMPL;
}

```

## -see-also

<a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrhandler">ISyncMgrHandler</a>



<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getobject">ISyncMgrHandler::GetObject</a>



<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgruioperation-run">ISyncMgrUIOperation::Run</a>