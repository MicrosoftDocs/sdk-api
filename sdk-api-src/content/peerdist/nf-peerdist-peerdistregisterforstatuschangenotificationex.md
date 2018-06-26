---
UID: NF:peerdist.PeerDistRegisterForStatusChangeNotificationEx
title: PeerDistRegisterForStatusChangeNotificationEx function
author: windows-sdk-content
description: The PeerDistRegisterForStatusChangeNotificationEx function requests the Peer Distribution service status change notification.
old-location: p2p\peerdistregisterforstatuschangenotificationex.htm
old-project: P2PSdk
ms.assetid: 84de2b23-5536-43e9-9336-0c1d3b70891d
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PeerDistRegisterForStatusChangeNotificationEx, PeerDistRegisterForStatusChangeNotificationEx function [Peer Networking], p2p.peerdistregisterforstatuschangenotificationex, peerdist/PeerDistRegisterForStatusChangeNotificationEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS, *PPEERDIST_CLIENT_INFO_BY_HANDLE_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - peerdist.h
api_name:
 - PeerDistRegisterForStatusChangeNotificationEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PeerDistRegisterForStatusChangeNotificationEx function


## -description


The <b>PeerDistRegisterForStatusChangeNotificationEx</b> function requests the Peer Distribution service status change notification.


## -parameters




### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>.


### -param hCompletionPort [in, optional]

A handle to the completion port that can be used for retrieving the completion notification of the asynchronous function. To create a completion port, use the <a href="https://msdn.microsoft.com/40cb47fc-7b15-47f6-bee2-2611d4686053">CreateIoCompletionPort</a> function.  This parameter can be <b>NULL</b>.


### -param ulCompletionKey [in, optional]

Value to be returned through the <i>lpCompletionKey</i> parameter of the <a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a> function.  This parameter is ignored when <i>hCompletionPort</i> is <b>NULL</b>.


### -param lpOverlapped [in]

Pointer to an <a href="http://go.microsoft.com/fwlink/p/?linkid=131007">OVERLAPPED</a> structure. If the <b>hEvent</b> member of the structure is not <b>NULL</b>, it will be signaled via SetEvent() used in order to signal the notification. This can occur  even if the completion port is specified via the <i>hCompletionPort</i> argument.


### -param pPeerDistStatus [in, out]

A pointer to a <a href="https://msdn.microsoft.com/6EE58EA9-BA0A-4A96-9F9C-EFAF2ABA37C6">PEERDIST_STATUS_INFO</a> structure that contains the current status and capabilities of the Peer Distribution service.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.




## -remarks



This function optionally registers a completion port and an <a href="http://go.microsoft.com/fwlink/p/?linkid=131007">OVERLAPPED</a> structure for status change notification. Upon successful completion, the <i>pPeerDistStatus</i> parameter will contain a valid <b>PEERDIST_STATUS</b> value.

Only one active registration for each session is allowed. The caller must register for notification each time after it signals. The notification will be sent only if the current status is changed from the previous notification. After the first call of the <a href="https://msdn.microsoft.com/7b01a499-534b-4c0f-9c9c-bafa066ad742">PeerDistRegisterForStatusChangeNotification</a> function for the  Peer Distribution session, the first notification will trigger only if the status is no longer equal to <b>PEERDIST_STATUS_DISABLED</b>.

A Peer Distribution status change can result in the Peer Distribution service moving to an available, unavailable, or disabled state. If the new status is disabled or unavailable, the content, content information, or stream handles the caller has access to will no longer function.  In this case, any API that uses these handles will fail with error <b>PEERDIST_ ERROR_INVALIDATED</b>.  The caller must explicitly close the handles by calling the appropriate Peer Distribution API.




## -see-also




<a href="https://msdn.microsoft.com/40cb47fc-7b15-47f6-bee2-2611d4686053">CreateIoCompletionPort</a>



<a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a>



<a href="https://msdn.microsoft.com/d693dc1c-39ce-4a2b-b769-9d370abc3d3c">PEERDIST_STATUS</a>



<a href="https://msdn.microsoft.com/066f1856-0617-40c7-a444-9765c01b4563">PeerDistServerCloseContentInformation</a>



<a href="https://msdn.microsoft.com/376ece5f-93ea-4650-a6d8-351ae60fc15b">PeerDistServerRetrieveContentInformation</a>



<a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>
 

 

