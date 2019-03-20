---
UID: NF:peerdist.PeerDistClientOpenContent
title: PeerDistClientOpenContent function (peerdist.h)
author: windows-sdk-content
description: PeerDistClientOpenContent function opens and returns a PEERDIST_CONTENT_HANDLE. The client uses the content handle to retrieve data from the Peer Distribution service.
old-location: p2p\peerdistclientopencontent.htm
tech.root: P2PSdk
ms.assetid: bf9d4eb2-e939-42c6-8d71-669a949ca77a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PeerDistClientOpenContent, PeerDistClientOpenContent function [Peer Networking], p2p.peerdistclientopencontent, peerdist/PeerDistClientOpenContent
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
 - PeerDistClientOpenContent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PeerDistClientOpenContent function


## -description


The <b>PeerDistClientOpenContent</b> function opens  and returns a PEERDIST_CONTENT_HANDLE. The client uses the content handle to retrieve data from the Peer Distribution service.


## -parameters




### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>.



### -param pContentTag [in]

Pointer to a <a href="https://msdn.microsoft.com/09eab22b-0534-44db-9954-ff5a9c5667f9">PEERDIST_CONTENT_TAG</a> structure that contains a 16 byte client specified identifier. This parameter is used in conjunction with the <a href="https://msdn.microsoft.com/bb77499b-520b-4def-97d8-504983953d4b">PeerDistClientFlushContent</a> function.  


### -param hCompletionPort [in, optional]

A handle to the completion port that can be used for retrieving the completion notification of the asynchronous function. To create a completion port, use the <a href="https://msdn.microsoft.com/40cb47fc-7b15-47f6-bee2-2611d4686053">CreateIoCompletionPort</a> function  This parameter can be <b>NULL</b>.


### -param ulCompletionKey [in, optional]

Value to be returned through the <i>lpCompletionKey</i> parameter of the <a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a> function.  This parameter is ignored when <i>hCompletionPort</i> is <b>NULL</b>.


### -param phContentHandle [out]

A pointer to a variable that receives the <b>PEERDIST_CONTENT_HANDLE</b> used to retrieve or add data.


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



Client must call the <b>PeerDistClientOpenContent</b> function to obtain a <b>PEERDIST_CONTENT_HANDLE</b> handle that later can be used in the following functions:

<ul>
<li>
<a href="https://msdn.microsoft.com/933ca20c-8a28-4b6a-9ec8-85608fd02990">PeerDistClientAddContentInformation</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0951e5e5-ad00-463e-8aa8-21b11a8acedc">PeerDistClientCompleteContentInformation</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ee64c0a8-7a07-4045-96fa-855b31c2e5b1">PeerDistClientBlockRead</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7c73e9e2-c723-4472-84e5-b0d25eb3b283">PeerDistClientStreamRead</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f1fdd398-ed84-4819-b0e8-e9b653bd6848">PeerDistClientAddData</a>
</li>
</ul>
If an optional completion port handle is specified, it is used for posting the completion results of above listed asynchronous functions.

The handle returned by <b>PeerDistClientOpenContent</b> function call must be closed by <a href="https://msdn.microsoft.com/c55300b7-13b6-42bf-b673-56a5e077416d">PeerDistClientCloseContent</a> function.




## -see-also




<a href="https://msdn.microsoft.com/933ca20c-8a28-4b6a-9ec8-85608fd02990">PeerDistClientAddContentInformation</a>



<a href="https://msdn.microsoft.com/f1fdd398-ed84-4819-b0e8-e9b653bd6848">PeerDistClientAddData</a>



<a href="https://msdn.microsoft.com/ee64c0a8-7a07-4045-96fa-855b31c2e5b1">PeerDistClientBlockRead</a>



<a href="https://msdn.microsoft.com/c55300b7-13b6-42bf-b673-56a5e077416d">PeerDistClientCloseContent</a>



<a href="https://msdn.microsoft.com/0951e5e5-ad00-463e-8aa8-21b11a8acedc">PeerDistClientCompleteContentInformation</a>



<a href="https://msdn.microsoft.com/bb77499b-520b-4def-97d8-504983953d4b">PeerDistClientFlushContent</a>



<a href="https://msdn.microsoft.com/7c73e9e2-c723-4472-84e5-b0d25eb3b283">PeerDistClientStreamRead</a>



<a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>
 

 

