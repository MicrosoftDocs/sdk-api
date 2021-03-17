---
UID: NF:peerdist.PeerDistUnregisterForStatusChangeNotification
title: PeerDistUnregisterForStatusChangeNotification function (peerdist.h)
description: PeerDistUnregisterForStatusChangeNotification function unregisters the status change notification for the session associated with the specified handle.
helpviewer_keywords: ["PeerDistUnregisterForStatusChangeNotification","PeerDistUnregisterForStatusChangeNotification function [Peer Networking]","p2p.peerdistunregisterforstatuschangenotification","peerdist/PeerDistUnregisterForStatusChangeNotification"]
old-location: p2p\peerdistunregisterforstatuschangenotification.htm
tech.root: p2p
ms.assetid: cb18c8bb-92b3-4d4e-9ce8-77c5628a9a1a
ms.date: 12/05/2018
ms.keywords: PeerDistUnregisterForStatusChangeNotification, PeerDistUnregisterForStatusChangeNotification function [Peer Networking], p2p.peerdistunregisterforstatuschangenotification, peerdist/PeerDistUnregisterForStatusChangeNotification
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
 - PeerDistUnregisterForStatusChangeNotification
 - peerdist/PeerDistUnregisterForStatusChangeNotification
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
 - PeerDistUnregisterForStatusChangeNotification
---

# PeerDistUnregisterForStatusChangeNotification function


## -description

The <b>PeerDistUnregisterForStatusChangeNotification</b> function unregisters the status change notification for the session associated with the specified handle.

## -parameters

### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>.

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

This function cancels any registered notification  previously set by a <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistregisterforstatuschangenotification">PeerDistRegisterForStatusChangeNotification</a> function call.

To confirm successfully canceled operations, a call should be made to <a href="/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> using the <b>OVERLAPPED</b> structure returned by <a href="/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a> with an expected return of <b>FALSE</b>.

Additionally, calling <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> immediately after a successful <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistregisterforstatuschangenotification">PeerDistRegisterForStatusChangeNotification</a> will return the <b>ERROR_OPERATION_ABORTED</b> error code.

## -see-also

<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistregisterforstatuschangenotification">PeerDistRegisterForStatusChangeNotification</a>