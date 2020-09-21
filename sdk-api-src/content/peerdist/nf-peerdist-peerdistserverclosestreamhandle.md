---
UID: NF:peerdist.PeerDistServerCloseStreamHandle
title: PeerDistServerCloseStreamHandle function (peerdist.h)
description: PeerDistServerCloseStreamHandle function closes a handle returned by PeerDistServerPublishStream.
helpviewer_keywords: ["PeerDistServerCloseStreamHandle","PeerDistServerCloseStreamHandle function [Peer Networking]","p2p.peerdistserverclosestreamhandle","peerdist/PeerDistServerCloseStreamHandle"]
old-location: p2p\peerdistserverclosestreamhandle.htm
tech.root: p2p
ms.assetid: 599b4694-3d03-4d25-9d02-313599aaaf0b
ms.date: 12/05/2018
ms.keywords: PeerDistServerCloseStreamHandle, PeerDistServerCloseStreamHandle function [Peer Networking], p2p.peerdistserverclosestreamhandle, peerdist/PeerDistServerCloseStreamHandle
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
 - PeerDistServerCloseStreamHandle
 - peerdist/PeerDistServerCloseStreamHandle
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
 - PeerDistServerCloseStreamHandle
---

# PeerDistServerCloseStreamHandle function


## -description

The <b>PeerDistServerCloseStreamHandle</b> function  closes a handle returned by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverpublishstream">PeerDistServerPublishStream</a>.

## -parameters

### -param hPeerDist [in]

A PEERDIST_INSTANCE_HANDLE returned by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>.

### -param hStream [in]

A PEERDIST_STREAM_HANDLE returned by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverpublishstream">PeerDistServerPublishStream</a>.

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
The <i>hPeerDist</i> or <i>hStream</i> handle is invalid

</td>
</tr>
</table>

## -remarks

The <b>PeerDistServerCloseStreamHandle</b> function call cancels all pending operations associated with <i>hStream</i>. To prevent unintended cancellation of publication and closure of the stream handle, this function should be called after the completion of <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverpublishcompletestream">PeerDistServerPublishCompleteStream</a>.

<b>PeerDistServerCloseStreamHandle</b> does not remove the publication. In order to remove the publication, call <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverunpublish">PeerDistServerUnpublish</a>.

## -see-also

<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverpublishcompletestream">PeerDistServerPublishCompleteStream</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverpublishstream">PeerDistServerPublishStream</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverunpublish">PeerDistServerUnpublish</a>