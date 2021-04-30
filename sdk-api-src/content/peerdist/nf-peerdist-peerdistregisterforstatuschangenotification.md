---
UID: NF:peerdist.PeerDistRegisterForStatusChangeNotification
title: PeerDistRegisterForStatusChangeNotification function (peerdist.h)
description: The PeerDistRegisterForStatusChangeNotification function requests the Peer Distribution service status change notification.
helpviewer_keywords: ["PeerDistRegisterForStatusChangeNotification","PeerDistRegisterForStatusChangeNotification function [Peer Networking]","p2p.peerdistregisterforstatuschangenotification","peerdist/PeerDistRegisterForStatusChangeNotification"]
old-location: p2p\peerdistregisterforstatuschangenotification.htm
tech.root: p2p
ms.assetid: 7b01a499-534b-4c0f-9c9c-bafa066ad742
ms.date: 12/05/2018
ms.keywords: PeerDistRegisterForStatusChangeNotification, PeerDistRegisterForStatusChangeNotification function [Peer Networking], p2p.peerdistregisterforstatuschangenotification, peerdist/PeerDistRegisterForStatusChangeNotification
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
 - PeerDistRegisterForStatusChangeNotification
 - peerdist/PeerDistRegisterForStatusChangeNotification
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
 - PeerDistRegisterForStatusChangeNotification
---

# PeerDistRegisterForStatusChangeNotification function


## -description

The <b>PeerDistRegisterForStatusChangeNotification</b> function requests the Peer Distribution service status change notification.

## -parameters

### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>.

### -param hCompletionPort [in, optional]

A handle to the completion port that can be used for retrieving the completion notification of the asynchronous function. To create a completion port, use the <a href="/windows/desktop/FileIO/createiocompletionport">CreateIoCompletionPort</a> function.  This parameter can be <b>NULL</b>.

### -param ulCompletionKey [in, optional]

Value to be returned through the <i>lpCompletionKey</i> parameter of the <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a> function.  This parameter is ignored when <i>hCompletionPort</i> is <b>NULL</b>.

### -param lpOverlapped [in]

Pointer to an <a href="/windows/win32/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. If the <b>hEvent</b> member of the structure is not <b>NULL</b>, it will be signaled via SetEvent() used in order to signal the notification. This can occur  even if the completion port is specified via the <i>hCompletionPort</i> argument.

### -param pPeerDistStatus [out]

A pointer to a <a href="/windows/desktop/api/peerdist/ne-peerdist-peerdist_status">PEERDIST_STATUS</a> enumeration that indicates the current status of the Peer Distribution service.

## -returns

If the function succeeds, the return value is <b>ERROR_IO_PENDING</b>. Otherwise, the function may return one of the following values:

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

This function optionally registers a completion port and an <a href="/windows/win32/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure for status change notification. Upon successful completion, the <i>pPeerDistStatus</i> parameter will contain a valid <b>PEERDIST_STATUS</b> value.

Only one active registration for each session is allowed. The caller must register for notification each time after it signals. The notification will be sent only if the current status is changed from the previous notification. After the first call of the <b>PeerDistRegisterForStatusChangeNotification</b> function for the  Peer Distribution session, the first notification will trigger only if the status is no longer equal to <b>PEERDIST_STATUS_DISABLED</b>.

A Peer Distribution status change can result in the Peer Distribution service moving to an available, unavailable, or disabled state. If the new status is disabled or unavailable, the content, content information, or stream handles the caller has access to will no longer function.  In this case, any API that uses these handles will fail with error <b>PEERDIST_ ERROR_INVALIDATED</b>.  The caller must explicitly close the handles by calling the appropriate Peer Distribution API.

## -see-also

<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientclosecontent">PeerDistClientCloseContent</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverclosecontentinformation">PeerDistServerCloseContentInformation</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverclosestreamhandle">PeerDistServerCloseStreamHandle</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>