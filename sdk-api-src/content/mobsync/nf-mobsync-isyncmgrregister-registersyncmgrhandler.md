---
UID: NF:mobsync.ISyncMgrRegister.RegisterSyncMgrHandler
title: ISyncMgrRegister::RegisterSyncMgrHandler (mobsync.h)
author: windows-sdk-content
description: Registers a handler with the synchronization manager when the handler has items to synchronize.
old-location: shell\syncmgr_isyncmgrregister_registersyncmgrhandler.htm
tech.root: shell
ms.assetid: 8c980c57-90a1-4f97-8d0c-22a3abdefabb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISyncMgrRegister interface [Windows Shell],RegisterSyncMgrHandler method, ISyncMgrRegister.RegisterSyncMgrHandler, ISyncMgrRegister::RegisterSyncMgrHandler, RegisterSyncMgrHandler, RegisterSyncMgrHandler method [Windows Shell], RegisterSyncMgrHandler method [Windows Shell],ISyncMgrRegister interface, mobsync/ISyncMgrRegister::RegisterSyncMgrHandler, shell.syncmgr_isyncmgrregister_registersyncmgrhandler, syncmgr.isyncmgrregister_registersyncmgrhandler
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
 - ISyncMgrRegister.RegisterSyncMgrHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrRegister::RegisterSyncMgrHandler


## -description


Registers a handler with the synchronization manager when the handler has items to synchronize.
      


## -parameters




### -param clsidHandler [in]

Type: <b>REFCLSID</b>

The CLSID of the handler that should be registered to do synchronizations.


### -param pwszDescription [in]

Type: <b>LPCWSTR</b>

Text identifying the handler. This parameter may be <b>NULL</b>.


### -param dwSyncMgrRegisterFlags [in]

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
The handler was successfully registered.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1feed230-5a50-4ff5-a8a9-e0ce15ba8f1c">ISyncMgrRegister</a>
 

 

