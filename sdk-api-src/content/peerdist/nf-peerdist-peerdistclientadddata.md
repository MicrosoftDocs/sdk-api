---
UID: NF:peerdist.PeerDistClientAddData
title: PeerDistClientAddData function (peerdist.h)
description: The PeerDistClientAddData function is used to supply content to the local cache.
helpviewer_keywords: ["PeerDistClientAddData","PeerDistClientAddData function [Peer Networking]","p2p.peerdistclientadddata","peerdist/PeerDistClientAddData"]
old-location: p2p\peerdistclientadddata.htm
tech.root: p2p
ms.assetid: f1fdd398-ed84-4819-b0e8-e9b653bd6848
ms.date: 12/05/2018
ms.keywords: PeerDistClientAddData, PeerDistClientAddData function [Peer Networking], p2p.peerdistclientadddata, peerdist/PeerDistClientAddData
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
 - PeerDistClientAddData
 - peerdist/PeerDistClientAddData
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
 - PeerDistClientAddData
---

# PeerDistClientAddData function


## -description

The <b>PeerDistClientAddData</b> function is used to supply content to the local cache.  Typically this is done when data could not be found on the local network as indicated when either <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientblockread">PeerDistClientBlockRead</a> or <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientstreamread">PeerDistClientStreamRead</a> complete with <b>ERROR_TIMEOUT</b> or <b>PEERDIST_ERROR_MISSING_DATA</b>.

## -parameters

### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>.

### -param hContentHandle [in]

A <b>PEERDIST_CONTENT_HANDLE</b> returned by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientopencontent">PeerDistClientOpenContent</a>.

### -param cbNumberOfBytes

The number of bytes to be added to the local cache.

### -param pBuffer [in]

Pointer to the buffer that contains the data to be added to the local cache. This buffer must remain valid for the duration of the add operation. The caller must not use this buffer until the add operation is completed.

### -param lpOverlapped [in]

Pointer to an <a href="/windows/win32/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. The byte offset from the beginning of content, at which this data is being added, is specified by setting the <b>Offset</b> and <b>OffsetHigh</b> members of the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure.  The <b>OffsetHigh</b> member MUST be set to the higher 32 bits of the byte offset and the <b>Offset</b> member MUST be set to the lower 32 bits of the byte offset.

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
The <i>hPeerDist</i> or <i>hContent</i> handle is invalid.

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

The data that has been added with this function and passed verification is available to other peers or hosted cache for download. The Peer Distribution service stores this data in its local cache.

If the API completes with <b>PEERDIST_ERROR_OUT_OF_BOUNDS</b>, this indicates that the offset specified in the overlapped structure is beyond the end of the content.

## -see-also

<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientblockread">PeerDistClientBlockRead</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientstreamread">PeerDistClientStreamRead</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>