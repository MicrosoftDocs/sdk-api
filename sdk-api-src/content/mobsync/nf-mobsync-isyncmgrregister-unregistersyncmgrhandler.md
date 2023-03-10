---
UID: NF:mobsync.ISyncMgrRegister.UnregisterSyncMgrHandler
title: ISyncMgrRegister::UnregisterSyncMgrHandler (mobsync.h)
description: Removes a handler's class identifier (CLSID) from the registration. A handler should call this when it no longer has any items to synchronize.
helpviewer_keywords: ["ISyncMgrRegister interface [Windows Shell]","UnregisterSyncMgrHandler method","ISyncMgrRegister.UnregisterSyncMgrHandler","ISyncMgrRegister::UnregisterSyncMgrHandler","UnregisterSyncMgrHandler","UnregisterSyncMgrHandler method [Windows Shell]","UnregisterSyncMgrHandler method [Windows Shell]","ISyncMgrRegister interface","mobsync/ISyncMgrRegister::UnregisterSyncMgrHandler","shell.syncmgr_isyncmgrregister_unregistersyncmgrhandler","syncmgr.isyncmgrregister_unregistersyncmgrhandler"]
old-location: shell\syncmgr_isyncmgrregister_unregistersyncmgrhandler.htm
tech.root: shell
ms.assetid: cd823d73-a07a-4c75-a29c-6c48ad2c23dc
ms.date: 12/05/2018
ms.keywords: ISyncMgrRegister interface [Windows Shell],UnregisterSyncMgrHandler method, ISyncMgrRegister.UnregisterSyncMgrHandler, ISyncMgrRegister::UnregisterSyncMgrHandler, UnregisterSyncMgrHandler, UnregisterSyncMgrHandler method [Windows Shell], UnregisterSyncMgrHandler method [Windows Shell],ISyncMgrRegister interface, mobsync/ISyncMgrRegister::UnregisterSyncMgrHandler, shell.syncmgr_isyncmgrregister_unregistersyncmgrhandler, syncmgr.isyncmgrregister_unregistersyncmgrhandler
req.header: mobsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mobsync.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISyncMgrRegister::UnregisterSyncMgrHandler
 - mobsync/ISyncMgrRegister::UnregisterSyncMgrHandler
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mobsync.dll
api_name:
 - ISyncMgrRegister.UnregisterSyncMgrHandler
---

# ISyncMgrRegister::UnregisterSyncMgrHandler


## -description

Removes a handler's class identifier (CLSID) from the registration. A handler should call this when it no longer has any items to synchronize.

## -parameters

### -param clsidHandler [in]

Type: <b>REFCLSID</b>

The CLSID of the handler that should be unregistered.

### -param dwReserved [in]

Type: <b>DWORD</b>

## -returns

Type: <b>HRESULT</b>

This method supports the standard return values E_INVALIDARG, E_UNEXPECTED, and E_OUTOFMEMORY, as well as the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The handler was successfully removed from the registry with SyncMgr.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrregister">ISyncMgrRegister</a>