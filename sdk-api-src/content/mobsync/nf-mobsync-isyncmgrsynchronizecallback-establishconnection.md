---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

