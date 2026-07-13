---
UID: NF:syncmgr.ISyncMgrHandlerInfo.IsEnabled
title: ISyncMgrHandlerInfo::IsEnabled (syncmgr.h)
description: Gets a value that indicates whether the handler is enabled.
helpviewer_keywords: ["ISyncMgrHandlerInfo interface [Windows Shell]","IsEnabled method","ISyncMgrHandlerInfo.IsEnabled","ISyncMgrHandlerInfo::IsEnabled","IsEnabled","IsEnabled method [Windows Shell]","IsEnabled method [Windows Shell]","ISyncMgrHandlerInfo interface","_shell_ISyncMgrHandlerInfo_IsEnabled","shell.ISyncMgrHandlerInfo_IsEnabled","syncmgr/ISyncMgrHandlerInfo::IsEnabled"]
old-location: shell\ISyncMgrHandlerInfo_IsEnabled.htm
tech.root: shell
ms.assetid: 1485ae25-20b8-4ee9-a30d-247f719047cd
ms.date: 12/05/2018
ms.keywords: ISyncMgrHandlerInfo interface [Windows Shell],IsEnabled method, ISyncMgrHandlerInfo.IsEnabled, ISyncMgrHandlerInfo::IsEnabled, IsEnabled, IsEnabled method [Windows Shell], IsEnabled method [Windows Shell],ISyncMgrHandlerInfo interface, _shell_ISyncMgrHandlerInfo_IsEnabled, shell.ISyncMgrHandlerInfo_IsEnabled, syncmgr/ISyncMgrHandlerInfo::IsEnabled
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
 - ISyncMgrHandlerInfo::IsEnabled
 - syncmgr/ISyncMgrHandlerInfo::IsEnabled
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
 - ISyncMgrHandlerInfo.IsEnabled
---

# ISyncMgrHandlerInfo::IsEnabled


## -description

Gets a value that indicates whether the handler is enabled.



## -returns

Type: <b>HRESULT</b>

Returns S_OK if the handler is enabled; otherwise, S_FALSE.
                    
                    

If the handler wants Sync Center to maintain the current state, it can return E_NOTIMPL. If any other value is returned, Sync Center sets the handler's enabled state to the last known value and enables or disables the associated tasks as appropriate.

If either the SYNCMGR_HCM_QUERY_BEFORE_ENABLE or SYNCMGR_HCM_QUERY_BEFORE_DISABLE flag is set in the mask returned from <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getcapabilities">GetCapabilities</a>, the handler must manage its own enabled state and therefore must return either S_OK or S_FALSE. Any other return value will be considered an error.

## -remarks

If a handler is disabled, neither it nor any of its items will be synchronized by Sync Center. Also, many of the possible actions available to a handler—such as Sync—are removed or disabled in the Sync Center folder UI.

This value is available in the folder UI as the System.Sync.Enabled (PKEY_Sync_Enabled) property.

Sync Center calls this method whenever the <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-updatehandler">UpdateHandler</a> method is called.


#### Examples



The following example shows an implementation of this method that calls a private class function to retrieve the enabled state.


```cpp
STDMETHODIMP CMyDeviceHandler::IsEnabled()
{
    // Return a previously-calculated value.
    return (_fIsEnabled ? S_OK : S_FALSE);
}

```

## -see-also

<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-enable">Enable</a>



<a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrhandlerinfo">ISyncMgrHandlerInfo</a>
