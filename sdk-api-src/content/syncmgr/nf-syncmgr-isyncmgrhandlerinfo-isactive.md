---
UID: NF:syncmgr.ISyncMgrHandlerInfo.IsActive
title: ISyncMgrHandlerInfo::IsActive (syncmgr.h)
description: Gets a value that indicates whether the handler can be synchronized.
helpviewer_keywords: ["ISyncMgrHandlerInfo interface [Windows Shell]","IsActive method","ISyncMgrHandlerInfo.IsActive","ISyncMgrHandlerInfo::IsActive","IsActive","IsActive method [Windows Shell]","IsActive method [Windows Shell]","ISyncMgrHandlerInfo interface","_shell_ISyncMgrHandlerInfo_IsActive","shell.ISyncMgrHandlerInfo_IsActive","syncmgr/ISyncMgrHandlerInfo::IsActive"]
old-location: shell\ISyncMgrHandlerInfo_IsActive.htm
tech.root: shell
ms.assetid: 0bcb06ba-a94a-4a18-a284-48be19ec4b44
ms.date: 12/05/2018
ms.keywords: ISyncMgrHandlerInfo interface [Windows Shell],IsActive method, ISyncMgrHandlerInfo.IsActive, ISyncMgrHandlerInfo::IsActive, IsActive, IsActive method [Windows Shell], IsActive method [Windows Shell],ISyncMgrHandlerInfo interface, _shell_ISyncMgrHandlerInfo_IsActive, shell.ISyncMgrHandlerInfo_IsActive, syncmgr/ISyncMgrHandlerInfo::IsActive
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
 - ISyncMgrHandlerInfo::IsActive
 - syncmgr/ISyncMgrHandlerInfo::IsActive
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
 - ISyncMgrHandlerInfo.IsActive
---

# ISyncMgrHandlerInfo::IsActive


## -description

Gets a value that indicates whether the handler can be synchronized.



## -returns

Type: <b>HRESULT</b>

Returns S_OK if the handler is active; otherwise, S_FALSE.
                    
                    

If the handler wants Sync Center to maintain the current state, it can return E_NOTIMPL. If any other value is returned, Sync Center sets the handler's state to the last known value. If the handler's last known value in that situation was inactive, Sync Center disables the <b>Setup</b> task. If the handler's last known value was active, the <b>Delete</b> task is not disabled.

If either the SYNCMGR_HCM_QUERY_BEFORE_ACTIVATE or SYNCMGR_HCM_QUERY_BEFORE_DEACTIVE flag is set in the mask returned from <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getcapabilities">GetCapabilities</a>, the handler must manage its own activation state and therefore must return either S_OK or S_FALSE. Any other return value will be considered an error.

## -remarks

If a handler is not active, it appears in the Sync Setup folder. Handlers in that folder cannot be synchronized. To move a handler to the Sync Center folder, the user selects the <b>Setup</b> task on the handler's shortcut menu or from the command module.

If a handler is active it appears in the main Sync Center folder. A handler that is active can be synchronized either by the user or through the <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrcontrol">ISyncMgrControl</a> interface. To move a handler to the Sync Setup folder, the user selects the <b>Delete</b> task on the handler's shortcut menu or on the command module.

Sync Center calls this method whenever the <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-updatehandler">UpdateHandler</a> method is called.


#### Examples



The following example shows an implementation of this method that calls a private class function to retrieve the active state.


```cpp
STDMETHODIMP CMyDeviceHandler::IsActive()
{
    // Return a previously-calculated value.
    return (_fIsActive ? S_OK : S_FALSE);
}

```

## -see-also

<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-activate">Activate</a>



<a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrhandlerinfo">ISyncMgrHandlerInfo</a>
