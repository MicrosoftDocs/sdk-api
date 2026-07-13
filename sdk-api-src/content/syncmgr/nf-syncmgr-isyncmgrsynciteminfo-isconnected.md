---
UID: NF:syncmgr.ISyncMgrSyncItemInfo.IsConnected
title: ISyncMgrSyncItemInfo::IsConnected (syncmgr.h)
description: Generates a value that indicates whether the item — typically some type of external device — is connected.
helpviewer_keywords: ["ISyncMgrSyncItemInfo interface [Windows Shell]","IsConnected method","ISyncMgrSyncItemInfo.IsConnected","ISyncMgrSyncItemInfo::IsConnected","IsConnected","IsConnected method [Windows Shell]","IsConnected method [Windows Shell]","ISyncMgrSyncItemInfo interface","_shell_ISyncMgrSyncItemInfo_IsConnected","shell.ISyncMgrSyncItemInfo_IsConnected","syncmgr/ISyncMgrSyncItemInfo::IsConnected"]
old-location: shell\ISyncMgrSyncItemInfo_IsConnected.htm
tech.root: shell
ms.assetid: 12ecfdba-87fb-4b73-8dac-0279f3f140fc
ms.date: 12/05/2018
ms.keywords: ISyncMgrSyncItemInfo interface [Windows Shell],IsConnected method, ISyncMgrSyncItemInfo.IsConnected, ISyncMgrSyncItemInfo::IsConnected, IsConnected, IsConnected method [Windows Shell], IsConnected method [Windows Shell],ISyncMgrSyncItemInfo interface, _shell_ISyncMgrSyncItemInfo_IsConnected, shell.ISyncMgrSyncItemInfo_IsConnected, syncmgr/ISyncMgrSyncItemInfo::IsConnected
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
 - ISyncMgrSyncItemInfo::IsConnected
 - syncmgr/ISyncMgrSyncItemInfo::IsConnected
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
 - ISyncMgrSyncItemInfo.IsConnected
---

# ISyncMgrSyncItemInfo::IsConnected


## -description

Generates a value that indicates whether the item—typically some type of external device—is connected.



## -returns

Type: <b>HRESULT</b>

Returns S_OK if the item is connected; otherwise, S_FALSE. An error returned by this method will be interpreted as S_OK.

## -remarks

If an item is disconnected, it is not synchronized by Sync Center. Also, many of the possible actions available to a item—such as Sync—are removed or disabled in the UI.

This value is available in the folder UI as the System.Sync.Connected (PKEY_Sync_Connected) property.

Sync Center calls this method whenever the <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-updatehandler">UpdateHandler</a> method is called.


#### Examples



The following example shows an implementation of this method that calls a private class function to retrieve the connected state.


```cpp
STDMETHODIMP CMyDeviceSyncItem::IsConnected()
{
    return (_IsConnected() ? S_OK : S_FALSE);
}

```
