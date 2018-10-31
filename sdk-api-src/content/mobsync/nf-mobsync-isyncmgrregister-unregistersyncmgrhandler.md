---
UID: NF:mobsync.ISyncMgrRegister.UnregisterSyncMgrHandler
title: ISyncMgrRegister::UnregisterSyncMgrHandler
author: windows-sdk-content
description: Removes a handler's class identifier (CLSID) from the registration. A handler should call this when it no longer has any items to synchronize.
old-location: shell\syncmgr_isyncmgrregister_unregistersyncmgrhandler.htm
tech.root: shell
ms.assetid: cd823d73-a07a-4c75-a29c-6c48ad2c23dc
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ISyncMgrRegister interface [Windows Shell],UnregisterSyncMgrHandler method, ISyncMgrRegister.UnregisterSyncMgrHandler, ISyncMgrRegister::UnregisterSyncMgrHandler, UnregisterSyncMgrHandler, UnregisterSyncMgrHandler method [Windows Shell], UnregisterSyncMgrHandler method [Windows Shell],ISyncMgrRegister interface, mobsync/ISyncMgrRegister::UnregisterSyncMgrHandler, shell.syncmgr_isyncmgrregister_unregistersyncmgrhandler, syncmgr.isyncmgrregister_unregistersyncmgrhandler
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mobsync.dll
api_name:
 - ISyncMgrRegister.UnregisterSyncMgrHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrRegister::UnregisterSyncMgrHandler


## -description


Removes a handler's class identifier (CLSID) from the registration. A handler should call this when it no longer has any items to synchronize.


## -parameters




### -param clsidHandler

TBD


### -param dwReserved [in]

Type: <b>DWORD</b>


#### - rclsidHandler [in]

Type: <b>REFCLSID</b>

The CLSID of the handler that should be unregistered.


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




<a href="https://msdn.microsoft.com/1feed230-5a50-4ff5-a8a9-e0ce15ba8f1c">ISyncMgrRegister</a>
 

 

