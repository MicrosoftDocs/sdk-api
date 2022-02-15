---
UID: NF:syncmgr.ISyncMgrSyncItemInfo.IsEnabled
title: ISyncMgrSyncItemInfo::IsEnabled (syncmgr.h)
description: Generates a value that indicates whether the item is enabled.
helpviewer_keywords: ["ISyncMgrSyncItemInfo interface [Windows Shell]","IsEnabled method","ISyncMgrSyncItemInfo.IsEnabled","ISyncMgrSyncItemInfo::IsEnabled","IsEnabled","IsEnabled method [Windows Shell]","IsEnabled method [Windows Shell]","ISyncMgrSyncItemInfo interface","_shell_ISyncMgrSyncItemInfo_IsEnabled","shell.ISyncMgrSyncItemInfo_IsEnabled","syncmgr/ISyncMgrSyncItemInfo::IsEnabled"]
old-location: shell\ISyncMgrSyncItemInfo_IsEnabled.htm
tech.root: shell
ms.assetid: 47383322-3fb6-47aa-9c97-9d432845fd35
ms.date: 12/05/2018
ms.keywords: ISyncMgrSyncItemInfo interface [Windows Shell],IsEnabled method, ISyncMgrSyncItemInfo.IsEnabled, ISyncMgrSyncItemInfo::IsEnabled, IsEnabled, IsEnabled method [Windows Shell], IsEnabled method [Windows Shell],ISyncMgrSyncItemInfo interface, _shell_ISyncMgrSyncItemInfo_IsEnabled, shell.ISyncMgrSyncItemInfo_IsEnabled, syncmgr/ISyncMgrSyncItemInfo::IsEnabled
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
 - ISyncMgrSyncItemInfo::IsEnabled
 - syncmgr/ISyncMgrSyncItemInfo::IsEnabled
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
 - ISyncMgrSyncItemInfo.IsEnabled
---

# ISyncMgrSyncItemInfo::IsEnabled


## -description

Generates a value that indicates whether the item is enabled.



## -returns

Type: <b>HRESULT</b>

Returns S_OK if the item is enabled; otherwise, S_FALSE.
                    
                    

If the item wants Sync Center to maintain the current state, it can return E_NOTIMPL. If any other value is returned, Sync Center sets the item's enabled state to the last known value and enables or disables the associated tasks as appropriate.

If either the SYNCMGR_ICM_QUERY_BEFORE_ENABLE or SYNCMGR_ICM_QUERY_BEFORE_DISABLE flags are set in the mask returned from <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-getcapabilities">GetCapabilities</a>, the handler must manage its own enabled state and therefore must return either S_OK or S_FALSE. Any other return value will be considered an error.

## -remarks

If an item is disabled, it is not synchronized by Sync Center. Also, many of the possible actions available to an item—such as Sync—are removed or disabled in the UI.

An item can implement a <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynciteminfo-isconnected">Disconnected</a> state by returning S_FALSE from <b>IsEnabled</b> and setting the SYNCMR_IPM_PREVENT_ENABLE flag in its <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-getpolicies">GetPolicies</a> implementation. This shows the item as disabled and prevents the user from enabling it manually.

The enabled value is available in the folder UI as the System.Sync.Enabled (PKEY_Sync_Enabled) property.

Sync Center calls this method whenever the <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-updatehandler">UpdateHandler</a> method is called.


#### Examples



The following example shows an implementation of this method that calls a private class function to retrieve the enabled state.


```cpp
STDMETHODIMP CMyDeviceSyncItem::IsEnabled()
{
    // Return a previously-calculated value.
    return (_fIsEnabled ? S_OK : S_FALSE);
}

```
