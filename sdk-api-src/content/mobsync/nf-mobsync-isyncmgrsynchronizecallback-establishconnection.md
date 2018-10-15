---
UID: NF:mobsync.ISyncMgrSynchronizeCallback.EstablishConnection
title: ISyncMgrSynchronizeCallback::EstablishConnection
author: windows-sdk-content
description: Called by the registered application's handler when a network connection is required.
old-location: shell\syncmgr_isyncmgrsynchronizecallback_establishconnection.htm
tech.root: shell
ms.assetid: f7d1aff8-a77e-4067-9fc9-4adc69bfc0d1
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: EstablishConnection, EstablishConnection method [Windows Shell], EstablishConnection method [Windows Shell],ISyncMgrSynchronizeCallback interface, ISyncMgrSynchronizeCallback interface [Windows Shell],EstablishConnection method, ISyncMgrSynchronizeCallback.EstablishConnection, ISyncMgrSynchronizeCallback::EstablishConnection, mobsync/ISyncMgrSynchronizeCallback::EstablishConnection, shell.syncmgr_isyncmgrsynchronizecallback_establishconnection, syncmgr.isyncmgrsynchronizecallback_establishconnection
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
 - ISyncMgrSynchronizeCallback.EstablishConnection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrSynchronizeCallback::EstablishConnection


## -description


Called by the registered application's handler when a network connection is required.


## -parameters




### -param pwszConnection [in]

Type: <b>LPCWSTR</b>

The name of the connection to dial.


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
The connection was successfully established.

</td>
</tr>
</table>
 




## -remarks



SyncMgr should use the default autodial connection if <i>pwszConnection</i> is <b>NULL</b>.

When an instance of <b>EstablishConnection</b> is called by a handler, SyncMgr tries to establish the connection. If a subsequent 
<b>EstablishConnection</b> is called then SyncMgr attempts the new connection without causing the previous connection to stop responding. All connections remain until all handlers have finished synchronizing. After all handlers have synchronized, then any opened connections are closed by SyncMgr.




## -see-also




<a href="https://msdn.microsoft.com/1c817a21-be91-43af-86c8-aa7909ae2fa2">ISyncMgrSynchronizeCallback</a>
 

 

