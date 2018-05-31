---
UID: NF:peerdist.PeerDistRegisterForStatusChangeNotification
title: PeerDistRegisterForStatusChangeNotification function
author: windows-sdk-content
description: The PeerDistRegisterForStatusChangeNotification function requests the Peer Distribution service status change notification.
old-location: p2p\peerdistregisterforstatuschangenotification.htm
old-project: P2PSdk
ms.assetid: 7b01a499-534b-4c0f-9c9c-bafa066ad742
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PeerDistRegisterForStatusChangeNotification, PeerDistRegisterForStatusChangeNotification function [Peer Networking], p2p.peerdistregisterforstatuschangenotification, peerdist/PeerDistRegisterForStatusChangeNotification
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
req.typenames: PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS, *PPEERDIST_CLIENT_INFO_BY_HANDLE_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	PeerDist.dll
api_name:
-	PeerDistRegisterForStatusChangeNotification
product: Windows
targetos: Windows
req.lib: PeerDist.lib
req.dll: PeerDist.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PeerDistRegisterForStatusChangeNotification function


## -description


The <b>PeerDistRegisterForStatusChangeNotification</b> function requests the Peer Distribution service status change notification.


## -parameters




### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>.


### -param hCompletionPort [in, optional]

A handle to the completion port that can be used for retrieving the completion notification of the asynchronous function. To create a completion port, use the <a href="https://msdn.microsoft.com/40cb47fc-7b15-47f6-bee2-2611d4686053">CreateIoCompletionPort</a> function.  This parameter can be <b>NULL</b>.


### -param ulCompletionKey [in, optional]

Value to be returned through the <i>lpCompletionKey</i> parameter of the <a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a> function.  This parameter is ignored when <i>hCompletionPort</i> is <b>NULL</b>.


### -param lpOverlapped [in]

Pointer to an <a href="http://go.microsoft.com/fwlink/p/?linkid=131007">OVERLAPPED</a> structure. If the <b>hEvent</b> member of the structure is not <b>NULL</b>, it will be signaled via SetEvent() used in order to signal the notification. This can occur  even if the completion port is specified via the <i>hCompletionPort</i> argument.


### -param pPeerDistStatus [out]

A pointer to a <a href="https://msdn.microsoft.com/d693dc1c-39ce-4a2b-b769-9d370abc3d3c">PEERDIST_STATUS</a> enumeration that indicates the current status of the Peer Distribution service.


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



This function optionally registers a completion port and an <a href="http://go.microsoft.com/fwlink/p/?linkid=131007">OVERLAPPED</a> structure for status change notification. Upon successful completion, the <i>pPeerDistStatus</i> parameter will contain a valid <b>PEERDIST_STATUS</b> value.

Only one active registration for each session is allowed. The caller must register for notification each time after it signals. The notification will be sent only if the current status is changed from the previous notification. After the first call of the <b>PeerDistRegisterForStatusChangeNotification</b> function for the  Peer Distribution session, the first notification will trigger only if the status is no longer equal to <b>PEERDIST_STATUS_DISABLED</b>.

A Peer Distribution status change can result in the Peer Distribution service moving to an available, unavailable, or disabled state. If the new status is disabled or unavailable, the content, content information, or stream handles the caller has access to will no longer function.  In this case, any API that uses these handles will fail with error <b>PEERDIST_ ERROR_INVALIDATED</b>.  The caller must explicitly close the handles by calling the appropriate Peer Distribution API.




## -see-also




<a href="https://msdn.microsoft.com/c55300b7-13b6-42bf-b673-56a5e077416d">PeerDistClientCloseContent</a>



<a href="https://msdn.microsoft.com/066f1856-0617-40c7-a444-9765c01b4563">PeerDistServerCloseContentInformation</a>



<a href="https://msdn.microsoft.com/599b4694-3d03-4d25-9d02-313599aaaf0b">PeerDistServerCloseStreamHandle</a>



<a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>
 

 

