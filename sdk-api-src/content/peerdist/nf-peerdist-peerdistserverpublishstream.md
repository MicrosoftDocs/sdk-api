---
UID: NF:peerdist.PeerDistServerPublishStream
title: PeerDistServerPublishStream function (peerdist.h)
description: PeerDistServerPublishStream function initializes a new stream to be published to the Peer Distribution service.
helpviewer_keywords: ["PeerDistServerPublishStream","PeerDistServerPublishStream function [Peer Networking]","p2p.peerdistserverpublishstream","peerdist/PeerDistServerPublishStream"]
old-location: p2p\peerdistserverpublishstream.htm
tech.root: p2p
ms.assetid: 2133e578-f89d-4cfd-a522-12c2531babaa
ms.date: 12/05/2018
ms.keywords: PeerDistServerPublishStream, PeerDistServerPublishStream function [Peer Networking], p2p.peerdistserverpublishstream, peerdist/PeerDistServerPublishStream
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
 - PeerDistServerPublishStream
 - peerdist/PeerDistServerPublishStream
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
 - PeerDistServerPublishStream
---

# PeerDistServerPublishStream function


## -description

The <b>PeerDistServerPublishStream</b> function initializes a new stream to be published to the Peer Distribution service.

## -parameters

### -param hPeerDist [in]

A PEERDIST_INSTANCE_HANDLE returned by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>.

### -param cbContentIdentifier

The length, in bytes, of the buffer that contains content identifier data.

### -param pContentIdentifier [in]

A pointer to an array that contains a content identifier data.

### -param cbContentLength

The length, in bytes, of the content to be published. This value can be 0 if the content length is not yet known.  If a non-zero argument is provided then it must match to the total data length added by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverpublishaddtostream">PeerDistServerPublishAddToStream</a> function calls.

### -param pPublishOptions [in, optional]

Pointer to a [PEERDIST_PUBLICATION_OPTIONS](./ns-peerdist-peerdist_publication_options.md) structure that specifies content publishing rules.

### -param hCompletionPort [in, optional]

A handle to the completion port that can be used for retrieving the completion notification of the asynchronous function. To create a completion port, use the <a href="/windows/desktop/FileIO/createiocompletionport">CreateIoCompletionPort</a> function. This parameter can be <b>NULL</b>.

### -param ulCompletionKey [in, optional]

Value  returned through the <i>lpCompletionKey</i> parameter of the <a href="/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a> function. This parameter is ignored when <i>hCompletionPort</i> is <b>NULL</b>.

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

A content identifier is a user defined label for the content being published. This content identifier is used for <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserveropencontentinformation">PeerDistServerOpenContentInformation</a>, <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverunpublish">PeerDistServerUnpublish</a>, and <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistservercancelasyncoperation">PeerDistServerCancelAsyncOperation</a> calls.

The handle received by phStream can be used in <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverpublishaddtostream">PeerDistServerPublishAddToStream</a> and <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverpublishcompletestream">PeerDistServerPublishCompleteStream</a> to publish data into the Peer Distribution service. This handle should be closed by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverclosestreamhandle">PeerDistServerCloseStreamHandle</a>.

A publication is accessible only to the User Account that originally published the content. If a different user calls <b>PeerDistServerPublishStream</b> with the same content identifier, a separate publication will be created under the context of that user.

## -see-also

<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistservercancelasyncoperation">PeerDistServerCancelAsyncOperation</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverclosestreamhandle">PeerDistServerCloseStreamHandle</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserveropencontentinformation">PeerDistServerOpenContentInformation</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverpublishaddtostream">PeerDistServerPublishAddToStream</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverpublishcompletestream">PeerDistServerPublishCompleteStream</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverunpublish">PeerDistServerUnpublish</a>