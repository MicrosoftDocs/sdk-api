---
UID: NF:peerdist.PeerDistServerRetrieveContentInformation
title: PeerDistServerRetrieveContentInformation function (peerdist.h)
description: PeerDistServerRetrieveContentInformation function retrieves the encoded content information associated with a handle returned by PeerDistServerOpenContentInformation.
helpviewer_keywords: ["PeerDistServerRetrieveContentInformation","PeerDistServerRetrieveContentInformation function [Peer Networking]","p2p.peerdistserverretrievecontentinformation","peerdist/PeerDistServerRetrieveContentInformation"]
old-location: p2p\peerdistserverretrievecontentinformation.htm
tech.root: p2p
ms.assetid: 376ece5f-93ea-4650-a6d8-351ae60fc15b
ms.date: 12/05/2018
ms.keywords: PeerDistServerRetrieveContentInformation, PeerDistServerRetrieveContentInformation function [Peer Networking], p2p.peerdistserverretrievecontentinformation, peerdist/PeerDistServerRetrieveContentInformation
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
 - PeerDistServerRetrieveContentInformation
 - peerdist/PeerDistServerRetrieveContentInformation
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
 - PeerDistServerRetrieveContentInformation
---

# PeerDistServerRetrieveContentInformation function


## -description

The <b>PeerDistServerRetrieveContentInformation</b> function retrieves the encoded content information associated with a handle returned by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserveropencontentinformation">PeerDistServerOpenContentInformation</a>.

## -parameters

### -param hPeerDist [in]

A PEERDIST_INSTANCE_HANDLE returned by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>.

### -param hContentInfo [in]

The handle returned by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserveropencontentinformation">PeerDistServerOpenContentInformation</a>.

### -param cbMaxNumberOfBytes

The maximum number of bytes to read.

### -param pBuffer [in, out]

Pointer to the buffer that receives the content information data.

### -param lpOverlapped [in]

Pointer to an <a href="/windows/win32/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. This function does not allow the caller to specify the start Offset in the content. The offset is implicitly maintained per hContentInfo. The Offset and OffsetHigh are reserved and must be zero.

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
The <i>hPeerDist</i> or <i>hContentInfo</i> handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEERDIST_ERROR_NO_MORE</b></dt>
</dl>
</td>
<td width="60%">
EOF on the content information has been reached.

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

On the success of the <b>PeerDistServerRetrieveContentInformation</b> operation, the <b>Offset</b> and <b>OffsetHigh</b> fields of the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure will be populated with the <b>ULONGLONG</b> offset in the content information that was retrieved. The <b>OffsetHigh</b> member will be set to the higher 32 bits of the offset and the <b>Offset</b> member will be set to the lower 32 bits of the offset.


<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> will populate <i>lpNumberOfBytesTransferred</i> with the number of bytes transferred. In the event the caller is using a completion port to process Peer Distribution API completions, the <i>lpNumberOfBytes</i> argument of <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a> will be populated with the number of bytes transferred.

## -see-also

<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserveropencontentinformation">PeerDistServerOpenContentInformation</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>