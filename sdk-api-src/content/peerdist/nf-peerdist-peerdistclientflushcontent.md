---
UID: NF:peerdist.PeerDistClientFlushContent
title: PeerDistClientFlushContent function
author: windows-sdk-content
description: The PeerDistClientFlushContent function allows a client to remove content added to the local cache with the PeerDistClientAddData function using the associated PEERDIST_CONTENT_TAG.
old-location: p2p\peerdistclientflushcontent.htm
old-project: p2psdk
ms.assetid: bb77499b-520b-4def-97d8-504983953d4b
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: PeerDistClientFlushContent, PeerDistClientFlushContent function [Peer Networking], p2p.peerdistclientflushcontent, peerdist/PeerDistClientFlushContent
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
 - PeerDistClientFlushContent
product: Windows
targetos: Windows
req.lib: PeerDist.lib
req.dll: PeerDist.dll
req.irql: 
req.product: ADAM
---

# PeerDistClientFlushContent function


## -description


The <b>PeerDistClientFlushContent</b> function allows a client to remove content  added to the local cache with the <a href="https://msdn.microsoft.com/f1fdd398-ed84-4819-b0e8-e9b653bd6848">PeerDistClientAddData</a> function using the associated <a href="https://msdn.microsoft.com/09eab22b-0534-44db-9954-ff5a9c5667f9">PEERDIST_CONTENT_TAG</a>.


## -parameters




### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>.


### -param pContentTag [in]

Pointer to a <a href="https://msdn.microsoft.com/09eab22b-0534-44db-9954-ff5a9c5667f9">PEERDIST_CONTENT_TAG</a> structure that contains the tag supplied when <a href="https://msdn.microsoft.com/bf9d4eb2-e939-42c6-8d71-669a949ca77a">PeerDistClientOpenContent</a> is called.


### -param hCompletionPort [in, optional]

A handle to the completion port that can be used for retrieving the completion notification of the asynchronous function. To create a completion port, use the <a href="https://msdn.microsoft.com/40cb47fc-7b15-47f6-bee2-2611d4686053">CreateIoCompletionPort</a> function. This parameter can be <b>NULL</b>.


### -param ulCompletionKey [in, optional]

Value to be returned through the <i>lpCompletionKey</i> parameter of the <a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a> function. This parameter is ignored when <i>hCompletionPort</i> is <b>NULL</b>.


### -param lpOverlapped [in]

Pointer to an <a href="http://go.microsoft.com/fwlink/p/?linkid=131007">OVERLAPPED</a> structure. <b>Offset</b> and <b>OffsetHigh</b> are reserved and must be zero.


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



The <i>pContentTag</i> is a client supplied tag passed to <a href="https://msdn.microsoft.com/bf9d4eb2-e939-42c6-8d71-669a949ca77a">PeerDistClientOpenContent</a>, which labels the content added by the client. This tag is used by the API to selectively flush content from the Peer Distribution cache.




## -see-also




<a href="https://msdn.microsoft.com/09eab22b-0534-44db-9954-ff5a9c5667f9">PEERDIST_CONTENT_TAG</a>



<a href="https://msdn.microsoft.com/bf9d4eb2-e939-42c6-8d71-669a949ca77a">PeerDistClientOpenContent</a>



<a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>
 

 

