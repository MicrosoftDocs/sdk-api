---
UID: NF:peerdist.PeerDistUnregisterForStatusChangeNotification
title: PeerDistUnregisterForStatusChangeNotification function
author: windows-sdk-content
description: PeerDistUnregisterForStatusChangeNotification function unregisters the status change notification for the session associated with the specified handle.
old-location: p2p\peerdistunregisterforstatuschangenotification.htm
tech.root: P2PSdk
ms.assetid: cb18c8bb-92b3-4d4e-9ce8-77c5628a9a1a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: PeerDistUnregisterForStatusChangeNotification, PeerDistUnregisterForStatusChangeNotification function [Peer Networking], p2p.peerdistunregisterforstatuschangenotification, peerdist/PeerDistUnregisterForStatusChangeNotification
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: peerdist.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: PeerDist.lib
req.dll: PeerDist.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - PeerDist.dll
api_name:
 - PeerDistUnregisterForStatusChangeNotification
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- PeerDistUnregisterForStatusChangeNotification
: 
---

# PeerDistUnregisterForStatusChangeNotification function


## -description


The <b>PeerDistUnregisterForStatusChangeNotification</b> function unregisters the status change notification for the session associated with the specified handle.


## -parameters




### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. Otherwise, the function may return one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hPeerDist</i> handle is invalid.

</td>
</tr>
</table>
 




## -remarks



This function cancels any registered notification  previously set by a <a href="https://msdn.microsoft.com/7b01a499-534b-4c0f-9c9c-bafa066ad742">PeerDistRegisterForStatusChangeNotification</a> function call.

To confirm successfully canceled operations, a call should be made to <a href="http://go.microsoft.com/fwlink/p/?linkid=131012">GetOverlappedResult</a> using the <b>OVERLAPPED</b> structure returned by <a href="http://go.microsoft.com/fwlink/p/?linkid=131008">GetQueuedCompletionStatus</a> with an expected return of <b>FALSE</b>.

Additionally, calling <a href="http://go.microsoft.com/fwlink/p/?linkid=131013">GetLastError</a> immediately after a successful <a href="https://msdn.microsoft.com/7b01a499-534b-4c0f-9c9c-bafa066ad742">PeerDistRegisterForStatusChangeNotification</a> will return the <b>ERROR_OPERATION_ABORTED</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7b01a499-534b-4c0f-9c9c-bafa066ad742">PeerDistRegisterForStatusChangeNotification</a>
 

 

