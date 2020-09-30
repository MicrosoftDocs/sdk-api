---
UID: NF:peerdist.PeerDistClientCancelAsyncOperation
title: PeerDistClientCancelAsyncOperation function (peerdist.h)
description: PeerDistClientCancelAsyncOperation function cancels asynchronous operation associated with an OVERLAPPED structure and the content handle returned by PeerDistClientOpenContent.
helpviewer_keywords: ["PeerDistClientCancelAsyncOperation","PeerDistClientCancelAsyncOperation function [Peer Networking]","p2p.peerdistclientcancelasyncoperation","peerdist/PeerDistClientCancelAsyncOperation"]
old-location: p2p\peerdistclientcancelasyncoperation.htm
tech.root: p2p
ms.assetid: 51100a8f-6652-46db-820a-8d16456d4c9a
ms.date: 12/05/2018
ms.keywords: PeerDistClientCancelAsyncOperation, PeerDistClientCancelAsyncOperation function [Peer Networking], p2p.peerdistclientcancelasyncoperation, peerdist/PeerDistClientCancelAsyncOperation
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PeerDistClientCancelAsyncOperation
 - peerdist/PeerDistClientCancelAsyncOperation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - PeerDist.dll
api_name:
 - PeerDistClientCancelAsyncOperation
---

# PeerDistClientCancelAsyncOperation function


## -description

The <b>PeerDistClientCancelAsyncOperation</b> function cancels asynchronous operation associated with an <a href="/windows/win32/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure and the content handle returned by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientopencontent">PeerDistClientOpenContent</a>.

## -parameters

### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>.

### -param hContentHandle [in]

A content handle opened by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientopencontent">PeerDistClientOpenContent</a> function call.

### -param pOverlapped [in, optional]

Pointer to an <a href="/windows/win32/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure that contains the canceling asynchronous operation data. If the pointer is <b>NULL</b> all asynchronous operations for specified content handle will be canceled.

## -returns

The function will return <b>ERROR_SUCCESS</b> value if the operation associated with the specified <a href="/windows/win32/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure is successfully canceled. Otherwise, the function may return one of the following values:

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
The operation associated with the specified <a href="/windows/win32/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure cannot be found.

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

This function will synchronously cancel the operation, but will not return until the cancellation result is posted to the completion port or wait event is set to the signaled state. Any threads in waiting can receive the completion notice for the operation before or after the <b>PeerDistClientCancelAsyncOperation</b> function returns.

This function  does not guarantee that the operation will complete as canceled. The cancellation result will be posted only if no other results have been posted. 

To confirm successfully canceled operations, a call should be made to <a href="/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> with an expected return of <b>FALSE</b>.

Additionally, calling <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> immediately after a successful <b>PeerDistClientCancelAsyncOperation</b> will return the <b>ERROR_OPERATION_ABORTED</b> error code.

## -see-also

<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistservercancelasyncoperation">PeerDistServerCancelAsyncOperation</a>