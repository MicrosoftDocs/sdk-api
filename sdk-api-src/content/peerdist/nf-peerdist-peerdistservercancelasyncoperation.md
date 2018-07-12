---
UID: NF:peerdist.PeerDistServerCancelAsyncOperation
title: PeerDistServerCancelAsyncOperation function
author: windows-sdk-content
description: PeerDistServerCancelAsyncOperation function cancels the asynchronous operation associated with the content identifier and OVERLAPPED structure.
old-location: p2p\peerdistservercancelasyncoperation.htm
old-project: p2psdk
ms.assetid: b8daa90a-f184-40cb-a62b-b1d122eb7781
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: PeerDistServerCancelAsyncOperation, PeerDistServerCancelAsyncOperation function [Peer Networking], p2p.peerdistservercancelasyncoperation, peerdist/PeerDistServerCancelAsyncOperation
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS, *PPEERDIST_CLIENT_INFO_BY_HANDLE_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - PeerDist.dll
api_name:
 - PeerDistServerCancelAsyncOperation
product: Windows
targetos: Windows
req.lib: PeerDist.lib
req.dll: PeerDist.dll
req.irql: 
req.product: ADAM
---

# PeerDistServerCancelAsyncOperation function


## -description


The <b>PeerDistServerCancelAsyncOperation</b> function cancels the asynchronous operation associated with the content identifier and <a href="http://go.microsoft.com/fwlink/p/?linkid=131007">OVERLAPPED</a> structure.


## -parameters




### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>.


### -param cbContentIdentifier

The length, in bytes, of the content identifier.


### -param pContentIdentifier [in]

Pointer to an array that contains the content identifier.


### -param pOverlapped [in]

Pointer to an <a href="http://go.microsoft.com/fwlink/p/?linkid=131007">OVERLAPPED</a> structure that contains the canceling asynchronous operation data.


## -returns



The function will return <b>ERROR_SUCCESS</b> value if the operation associated with <a href="http://go.microsoft.com/fwlink/p/?linkid=131007">OVERLAPPED</a> structure is successfully canceled. Otherwise, the function may return one of the following values:

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
The operation for <a href="http://go.microsoft.com/fwlink/p/?linkid=131007">OVERLAPPED</a> structure cannot be found.

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

To confirm successfully canceled operations, a call should be made to <a href="http://go.microsoft.com/fwlink/p/?linkid=131012">GetOverlappedResult</a> with an expected return of <b>FALSE</b>.  

Additionally, calling <a href="http://go.microsoft.com/fwlink/p/?linkid=131013">GetLastError</a> immediately after a successful <b>PeerDistServerCancelAsyncOperation</b> will return the <b>ERROR_OPERATION_ABORTED</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/51100a8f-6652-46db-820a-8d16456d4c9a">PeerDistClientCancelAsyncOperation</a>



<a href="https://msdn.microsoft.com/bf9d4eb2-e939-42c6-8d71-669a949ca77a">PeerDistClientOpenContent</a>
 

 

