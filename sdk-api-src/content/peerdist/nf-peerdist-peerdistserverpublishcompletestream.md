---
UID: NF:peerdist.PeerDistServerPublishCompleteStream
title: PeerDistServerPublishCompleteStream function (peerdist.h)
description: PeerDistServerPublishCompleteStream function completes the process of adding data to the stream.
helpviewer_keywords: ["PeerDistServerPublishCompleteStream","PeerDistServerPublishCompleteStream function [Peer Networking]","p2p.peerdistserverpublishcompletestream","peerdist/PeerDistServerPublishCompleteStream"]
old-location: p2p\peerdistserverpublishcompletestream.htm
tech.root: p2p
ms.assetid: ad66025e-cc4f-49b7-9749-de97f4a55078
ms.date: 12/05/2018
ms.keywords: PeerDistServerPublishCompleteStream, PeerDistServerPublishCompleteStream function [Peer Networking], p2p.peerdistserverpublishcompletestream, peerdist/PeerDistServerPublishCompleteStream
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
 - PeerDistServerPublishCompleteStream
 - peerdist/PeerDistServerPublishCompleteStream
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
 - PeerDistServerPublishCompleteStream
---

# PeerDistServerPublishCompleteStream function


## -description

The <b>PeerDistServerPublishCompleteStream</b> function completes the process of adding data to the stream.

## -parameters

### -param hPeerDist [in]

A PEERDIST_INSTANCE_HANDLE returned by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>.

### -param hStream [in]

A PEERDIST_STREAM_HANDLE returned  by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverpublishstream">PeerDistServerPublishStream</a>.

### -param lpOverlapped [in]

Pointer to an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. The <b>Offset</b> and <b>OffsetHigh</b> are reserved and must be zero.

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
The <i>hPeerDist</i> or <i>hStream</i> handle is invalid

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OPERATION_ABORTED</b></dt>
</dl>
</td>
<td width="60%">
The operation was canceled.

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
The service  is unavailable.

</td>
</tr>
</table>

## -remarks

Once this API completes successfully, <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserveropencontentinformation">PeerDistServerOpenContentInformation</a> and <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverretrievecontentinformation">PeerDistServerRetrieveContentInformation</a> can be used to retrieve content information.

<b>PeerDistServerPublishCompleteStream</b> does not close <i>hStream</i>. In order to close <i>hStream</i>, call <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverclosestreamhandle">PeerDistServerCloseStreamHandle</a>.

## -see-also

<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverclosestreamhandle">PeerDistServerCloseStreamHandle</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserveropencontentinformation">PeerDistServerOpenContentInformation</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverpublishaddtostream">PeerDistServerPublishAddToStream</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverpublishstream">PeerDistServerPublishStream</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverretrievecontentinformation">PeerDistServerRetrieveContentInformation</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverunpublish">PeerDistServerUnpublish</a>