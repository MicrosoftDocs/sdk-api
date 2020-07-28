---
UID: NF:peerdist.PeerDistServerCancelAsyncOperation
title: PeerDistServerCancelAsyncOperation function (peerdist.h)
description: PeerDistServerCancelAsyncOperation function cancels the asynchronous operation associated with the content identifier and OVERLAPPED structure.
helpviewer_keywords: ["PeerDistServerCancelAsyncOperation","PeerDistServerCancelAsyncOperation function [Peer Networking]","p2p.peerdistservercancelasyncoperation","peerdist/PeerDistServerCancelAsyncOperation"]
old-location: p2p\peerdistservercancelasyncoperation.htm
tech.root: p2p
ms.assetid: b8daa90a-f184-40cb-a62b-b1d122eb7781
ms.date: 12/05/2018
ms.keywords: PeerDistServerCancelAsyncOperation, PeerDistServerCancelAsyncOperation function [Peer Networking], p2p.peerdistservercancelasyncoperation, peerdist/PeerDistServerCancelAsyncOperation
f1_keywords:
- peerdist/PeerDistServerCancelAsyncOperation
dev_langs:
- c++
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
- PeerDistServerCancelAsyncOperation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PeerDistServerCancelAsyncOperation function


## -description


The <b>PeerDistServerCancelAsyncOperation</b> function cancels the asynchronous operation associated with the content identifier and <a href="https://msdn.microsoft.com/library/ms684342.aspx">OVERLAPPED</a> structure.


## -parameters




### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="https://docs.microsoft.com/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>.


### -param cbContentIdentifier

The length, in bytes, of the content identifier.


### -param pContentIdentifier [in]

Pointer to an array that contains the content identifier.


### -param pOverlapped [in]

Pointer to an <a href="https://msdn.microsoft.com/library/ms684342.aspx">OVERLAPPED</a> structure that contains the canceling asynchronous operation data.


## -returns



The function will return <b>ERROR_SUCCESS</b> value if the operation associated with <a href="https://msdn.microsoft.com/library/ms684342.aspx">OVERLAPPED</a> structure is successfully canceled. Otherwise, the function may return one of the following values:

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
<tr>
<td width="40%">
<dl>
<dt><b>PEERDIST_ERROR_OPERATION_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The operation for <a href="https://msdn.microsoft.com/library/ms684342.aspx">OVERLAPPED</a> structure cannot be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DISABLED_BY_POLICY</b></dt>
</dl>
</td>
<td width="60%">
The feature is disabled by Group Policy.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEERDIST_ERROR_SERVICE_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The service is unavailable.

</td>
</tr>
</table>
 




## -remarks



This function will synchronously cancel the operation, but will not return until the cancelation result is posted to the completion port or wait event is set to the 'signaled' state. Any threads in waiting can receive the completion notice for the operation before or after the <b>PeerDistServerCancelAsyncOperation</b> function returns.

This function  does not guarantee that the operation will complete as canceled. The cancellation result will be posted only if no other results have been posted.

To confirm successfully canceled operations, a call should be made to <a href="https://msdn.microsoft.com/library/ms683209.aspx">GetOverlappedResult</a> with an expected return of <b>FALSE</b>.  

Additionally, calling <a href="https://msdn.microsoft.com/library/ms679360.aspx">GetLastError</a> immediately after a successful <b>PeerDistServerCancelAsyncOperation</b> will return the <b>ERROR_OPERATION_ABORTED</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/peerdist/nf-peerdist-peerdistclientcancelasyncoperation">PeerDistClientCancelAsyncOperation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/peerdist/nf-peerdist-peerdistclientopencontent">PeerDistClientOpenContent</a>
 

 

