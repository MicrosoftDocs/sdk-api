---
UID: NF:peerdist.PeerDistServerPublishStream
title: PeerDistServerPublishStream function
author: windows-sdk-content
description: PeerDistServerPublishStream function initializes a new stream to be published to the Peer Distribution service.
old-location: p2p\peerdistserverpublishstream.htm
old-project: p2psdk
ms.assetid: 2133e578-f89d-4cfd-a522-12c2531babaa
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PeerDistServerPublishStream, PeerDistServerPublishStream function [Peer Networking], p2p.peerdistserverpublishstream, peerdist/PeerDistServerPublishStream
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
 - PeerDistServerPublishStream
product: Windows
targetos: Windows
req.lib: PeerDist.lib
req.dll: PeerDist.dll
req.irql: 
req.product: ADAM
---

# PeerDistServerPublishStream function


## -description


The <b>PeerDistServerPublishStream</b> function initializes a new stream to be published to the Peer Distribution service.


## -parameters




### -param hPeerDist [in]

A PEERDIST_INSTANCE_HANDLE returned by <a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>.


### -param cbContentIdentifier

The length, in bytes, of the buffer that contains content identifier data.


### -param pContentIdentifier [in]

A pointer to an array that contains a content identifier data.


### -param cbContentLength

The length, in bytes, of the content to be published. This value can be 0 if the content length is not yet known.  If a non-zero argument is provided then it must match to the total data length added by <a href="https://msdn.microsoft.com/296e21b9-9488-408a-b470-bbde1a18e6f0">PeerDistServerPublishAddToStream</a> function calls. 


### -param pPublishOptions [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/990b6551-eaf6-47f7-bc35-ea91820f917b">PEERDIST_PUBLICATION_OPTIONS</a> structure that specifies content publishing rules.


### -param hCompletionPort [in, optional]

A handle to the completion port that can be used for retrieving the completion notification of the asynchronous function. To create a completion port, use the <a href="https://msdn.microsoft.com/40cb47fc-7b15-47f6-bee2-2611d4686053">CreateIoCompletionPort</a> function. This parameter can be <b>NULL</b>.


### -param ulCompletionKey [in, optional]

Value  returned through the <i>lpCompletionKey</i> parameter of the <a href="http://go.microsoft.com/fwlink/p/?linkid=131008">GetQueuedCompletionStatus</a> function. This parameter is ignored when <i>hCompletionPort</i> is <b>NULL</b>.


### -param phStream [out]

A pointer that receives a handle to the stream that is used to publish data into the Peer Distribution service.


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
The specified <i>hPeerDist</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEERDIST_ERROR_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The content identifier used for publication is already published.

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



A content identifier is a user defined label for the content being published. This content identifier is used for <a href="https://msdn.microsoft.com/17b07141-2786-4192-ba7b-f3210c10aad4">PeerDistServerOpenContentInformation</a>, <a href="https://msdn.microsoft.com/880927c4-f7d7-4c75-b371-2fe401a50b20">PeerDistServerUnpublish</a>, and <a href="https://msdn.microsoft.com/b8daa90a-f184-40cb-a62b-b1d122eb7781">PeerDistServerCancelAsyncOperation</a> calls.

The handle received by phStream can be used in <a href="https://msdn.microsoft.com/296e21b9-9488-408a-b470-bbde1a18e6f0">PeerDistServerPublishAddToStream</a> and <a href="https://msdn.microsoft.com/ad66025e-cc4f-49b7-9749-de97f4a55078">PeerDistServerPublishCompleteStream</a> to publish data into the Peer Distribution service. This handle should be closed by <a href="https://msdn.microsoft.com/599b4694-3d03-4d25-9d02-313599aaaf0b">PeerDistServerCloseStreamHandle</a>.

A publication is accessible only to the User Account that originally published the content. If a different user calls <b>PeerDistServerPublishStream</b> with the same content identifier, a separate publication will be created under the context of that user.




## -see-also




<a href="https://msdn.microsoft.com/b8daa90a-f184-40cb-a62b-b1d122eb7781">PeerDistServerCancelAsyncOperation</a>



<a href="https://msdn.microsoft.com/599b4694-3d03-4d25-9d02-313599aaaf0b">PeerDistServerCloseStreamHandle</a>



<a href="https://msdn.microsoft.com/17b07141-2786-4192-ba7b-f3210c10aad4">PeerDistServerOpenContentInformation</a>



<a href="https://msdn.microsoft.com/296e21b9-9488-408a-b470-bbde1a18e6f0">PeerDistServerPublishAddToStream</a>



<a href="https://msdn.microsoft.com/ad66025e-cc4f-49b7-9749-de97f4a55078">PeerDistServerPublishCompleteStream</a>



<a href="https://msdn.microsoft.com/880927c4-f7d7-4c75-b371-2fe401a50b20">PeerDistServerUnpublish</a>
 

 

