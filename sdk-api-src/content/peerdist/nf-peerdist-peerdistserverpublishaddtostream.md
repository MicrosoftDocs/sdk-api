---
UID: NF:peerdist.PeerDistServerPublishAddToStream
title: PeerDistServerPublishAddToStream function (peerdist.h)
description: PeerDistServerPublishAddToStream function adds data to the publishing stream.
helpviewer_keywords: ["PeerDistServerPublishAddToStream","PeerDistServerPublishAddToStream function [Peer Networking]","p2p.peerdistserverpublishaddtostream","peerdist/PeerDistServerPublishAddToStream"]
old-location: p2p\peerdistserverpublishaddtostream.htm
tech.root: p2p
ms.assetid: 296e21b9-9488-408a-b470-bbde1a18e6f0
ms.date: 12/05/2018
ms.keywords: PeerDistServerPublishAddToStream, PeerDistServerPublishAddToStream function [Peer Networking], p2p.peerdistserverpublishaddtostream, peerdist/PeerDistServerPublishAddToStream
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
 - PeerDistServerPublishAddToStream
 - peerdist/PeerDistServerPublishAddToStream
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
 - PeerDistServerPublishAddToStream
---

# PeerDistServerPublishAddToStream function


## -description

The <b>PeerDistServerPublishAddToStream</b> function adds data to the publishing stream.

## -parameters

### -param hPeerDist [in]

A PEERDIST_INSTANCE_HANDLE returned by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>.

### -param hStream [in]

A PEERDIST_STREAM_HANDLE created by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverpublishstream">PeerDistServerPublishStream</a>.

### -param cbNumberOfBytes [in]

Number of bytes to be published.

### -param pBuffer [in]

Pointer to the buffer that contains the data to be published. This buffer must remain valid for the duration of the add operation. The caller must not use this buffer until the add operation is completed.

### -param lpOverlapped [in]

Pointer to an <a href="/windows/win32/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. The <b>Offset</b> and <b>OffsetHigh</b> members are reserved and must be zero.

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
The <i>hPeerDist</i> or <i>hStream</i> handle is invalid.

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
The service is unavailable.

</td>
</tr>
</table>

## -remarks

When calling this function multiple times on a single stream handle, the caller must wait for each operation to complete before the next call is made.

## -see-also

<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverpublishstream">PeerDistServerPublishStream</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>