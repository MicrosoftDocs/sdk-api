---
UID: NF:p2p.PeerCollabCloseHandle
title: PeerCollabCloseHandle function
author: windows-sdk-content
description: Closes the handle to a Peer Collaboration activity invitation.
old-location: p2p\peercollabclosehandle.htm
old-project: P2PSdk
ms.assetid: fbcf65c7-a133-44b9-b5bb-309b1c257a90
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: PeerCollabCloseHandle, PeerCollabCloseHandle function [Peer Networking], p2p.peercollabclosehandle, p2p/PeerCollabCloseHandle
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PEER_WATCH_PERMISSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2P.dll
api_name:
 - PeerCollabCloseHandle
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: ADAM
---

# PeerCollabCloseHandle function


## -description


The <b>PeerCollabCloseHandle</b> function closes the handle to a Peer Collaboration activity invitation.


## -parameters




### -param hInvitation

TBD




#### - handle [in]

Handle obtained by a previous call to <a href="https://msdn.microsoft.com/2101e16e-ee05-417f-835b-c00cba7f6576">PeerCollabAsyncInviteContact</a> or <a href="https://msdn.microsoft.com/2606d2ef-26d3-4c52-b481-3ea38350295a">PeerCollabAsyncInviteEndpoint</a>.


## -returns



Returns S_OK if the function succeeds. Otherwise, the function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to support this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle specified is invalid.

</td>
</tr>
</table>
 




## -remarks



You must call this API after the handle has been signaled for an event and any data associated with the event has been obtained.




## -see-also




<a href="https://msdn.microsoft.com/00c3c1f1-c36c-469a-a644-0ec60f02d25e">Peer Collaboration API Functions</a>



<a href="https://msdn.microsoft.com/2101e16e-ee05-417f-835b-c00cba7f6576">PeerCollabAsyncInviteContact</a>



<a href="https://msdn.microsoft.com/2606d2ef-26d3-4c52-b481-3ea38350295a">PeerCollabAsyncInviteEndpoint</a>
 

 

