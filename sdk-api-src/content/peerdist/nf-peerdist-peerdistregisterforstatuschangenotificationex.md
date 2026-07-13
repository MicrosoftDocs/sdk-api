---
UID: NF:peerdist.PeerDistRegisterForStatusChangeNotificationEx
title: PeerDistRegisterForStatusChangeNotificationEx function (peerdist.h)
description: The PeerDistRegisterForStatusChangeNotificationEx function requests the Peer Distribution service status change notification.
helpviewer_keywords: ["PeerDistRegisterForStatusChangeNotificationEx","PeerDistRegisterForStatusChangeNotificationEx function [Peer Networking]","p2p.peerdistregisterforstatuschangenotificationex","peerdist/PeerDistRegisterForStatusChangeNotificationEx"]
old-location: p2p\peerdistregisterforstatuschangenotificationex.htm
tech.root: p2p
ms.assetid: 84de2b23-5536-43e9-9336-0c1d3b70891d
ms.date: 12/05/2018
ms.keywords: PeerDistRegisterForStatusChangeNotificationEx, PeerDistRegisterForStatusChangeNotificationEx function [Peer Networking], p2p.peerdistregisterforstatuschangenotificationex, peerdist/PeerDistRegisterForStatusChangeNotificationEx
req.header: peerdist.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PeerDistRegisterForStatusChangeNotificationEx
 - peerdist/PeerDistRegisterForStatusChangeNotificationEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - peerdist.h
api_name:
 - PeerDistRegisterForStatusChangeNotificationEx
---

# PeerDistRegisterForStatusChangeNotificationEx function


## -description

The <b>PeerDistRegisterForStatusChangeNotificationEx</b> function requests the Peer Distribution service status change notification.

## -parameters

### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>.

### -param hCompletionPort [in, optional]

A handle to the completion port that can be used for retrieving the completion notification of the asynchronous function. To create a completion port, use the <a href="/windows/desktop/FileIO/createiocompletionport">CreateIoCompletionPort</a> function.  This parameter can be <b>NULL</b>.

### -param ulCompletionKey [in, optional]

Value to be returned through the <i>lpCompletionKey</i> parameter of the <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a> function.  This parameter is ignored when <i>hCompletionPort</i> is <b>NULL</b>.

### -param lpOverlapped [in]

Pointer to an <a href="/windows/win32/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. If the <b>hEvent</b> member of the structure is not <b>NULL</b>, it will be signaled via SetEvent() used in order to signal the notification. This can occur  even if the completion port is specified via the <i>hCompletionPort</i> argument.

### -param pPeerDistStatus [in, out]

A pointer to a <a href="/windows/desktop/api/peerdist/ns-peerdist-peerdist_status_info">PEERDIST_STATUS_INFO</a> structure that contains the current status and capabilities of the Peer Distribution service.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

## -remarks

This function optionally registers a completion port and an <a href="/windows/win32/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure for status change notification. Upon successful completion, the <i>pPeerDistStatus</i> parameter will contain a valid <b>PEERDIST_STATUS</b> value.

Only one active registration for each session is allowed. The caller must register for notification each time after it signals. The notification will be sent only if the current status is changed from the previous notification. After the first call of the <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistregisterforstatuschangenotification">PeerDistRegisterForStatusChangeNotification</a> function for the  Peer Distribution session, the first notification will trigger only if the status is no longer equal to <b>PEERDIST_STATUS_DISABLED</b>.

A Peer Distribution status change can result in the Peer Distribution service moving to an available, unavailable, or disabled state. If the new status is disabled or unavailable, the content, content information, or stream handles the caller has access to will no longer function.  In this case, any API that uses these handles will fail with error <b>PEERDIST_ ERROR_INVALIDATED</b>.  The caller must explicitly close the handles by calling the appropriate Peer Distribution API.

## -see-also

<a href="/windows/desktop/FileIO/createiocompletionport">CreateIoCompletionPort</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a>



<a href="/windows/desktop/api/peerdist/ne-peerdist-peerdist_status">PEERDIST_STATUS</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverclosecontentinformation">PeerDistServerCloseContentInformation</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverretrievecontentinformation">PeerDistServerRetrieveContentInformation</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>