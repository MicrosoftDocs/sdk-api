---
UID: NF:syncmgr.ISyncMgrHandlerInfo.IsConnected
title: ISyncMgrHandlerInfo::IsConnected (syncmgr.h)
description: Gets a value that indicates whether the handler — typically some type of external device — is connected.
helpviewer_keywords: ["ISyncMgrHandlerInfo interface [Windows Shell]","IsConnected method","ISyncMgrHandlerInfo.IsConnected","ISyncMgrHandlerInfo::IsConnected","IsConnected","IsConnected method [Windows Shell]","IsConnected method [Windows Shell]","ISyncMgrHandlerInfo interface","_shell_ISyncMgrHandlerInfo_IsConnected","shell.ISyncMgrHandlerInfo_IsConnected","syncmgr/ISyncMgrHandlerInfo::IsConnected"]
old-location: shell\ISyncMgrHandlerInfo_IsConnected.htm
tech.root: shell
ms.assetid: b51a32e7-962b-44f6-8508-26f819be483a
ms.date: 12/05/2018
ms.keywords: ISyncMgrHandlerInfo interface [Windows Shell],IsConnected method, ISyncMgrHandlerInfo.IsConnected, ISyncMgrHandlerInfo::IsConnected, IsConnected, IsConnected method [Windows Shell], IsConnected method [Windows Shell],ISyncMgrHandlerInfo interface, _shell_ISyncMgrHandlerInfo_IsConnected, shell.ISyncMgrHandlerInfo_IsConnected, syncmgr/ISyncMgrHandlerInfo::IsConnected
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
 - ISyncMgrHandlerInfo::IsConnected
 - syncmgr/ISyncMgrHandlerInfo::IsConnected
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
 - ISyncMgrHandlerInfo.IsConnected
---

# ISyncMgrHandlerInfo::IsConnected


## -description

Gets a value that indicates whether the handler—typically some type of external device—is connected.



## -returns

Type: <b>HRESULT</b>

Returns S_OK if the handler is connected; otherwise, S_FALSE. An error returned by this method will be interpreted as S_OK.

## -remarks

If a handler is disconnected, neither it nor any of its items will be synchronized by Sync Center. Also, many of the possible actions available to a handler—such as Sync—are removed or disabled in the Sync Center folder UI.

This value is available in the folder UI as the System.Sync.Connected (PKEY_Sync_Connected) property.

Sync Center calls this method whenever the <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-updatehandler">UpdateHandler</a> method is called.


#### Examples



The following example shows an implementation of this method that calls a private class function to retrieve the connected state.


```cpp
STDMETHODIMP CMyDeviceHandler::IsConnected()
{
    return (_IsConnected() ? S_OK : S_FALSE);
}

```
