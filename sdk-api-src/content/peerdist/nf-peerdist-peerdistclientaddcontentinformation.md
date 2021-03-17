---
UID: NF:peerdist.PeerDistClientAddContentInformation
title: PeerDistClientAddContentInformation function (peerdist.h)
description: PeerDistClientAddContentInformation function adds the content information associated with a content handle opened by PeerDistClientOpenContent.
helpviewer_keywords: ["PeerDistClientAddContentInformation","PeerDistClientAddContentInformation function [Peer Networking]","p2p.peerdistclientaddcontentinformation","peerdist/PeerDistClientAddContentInformation"]
old-location: p2p\peerdistclientaddcontentinformation.htm
tech.root: p2p
ms.assetid: 933ca20c-8a28-4b6a-9ec8-85608fd02990
ms.date: 12/05/2018
ms.keywords: PeerDistClientAddContentInformation, PeerDistClientAddContentInformation function [Peer Networking], p2p.peerdistclientaddcontentinformation, peerdist/PeerDistClientAddContentInformation
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
 - PeerDistClientAddContentInformation
 - peerdist/PeerDistClientAddContentInformation
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
 - PeerDistClientAddContentInformation
---

# PeerDistClientAddContentInformation function


## -description

The <b>PeerDistClientAddContentInformation</b> function adds the content information associated with a content handle opened by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientopencontent">PeerDistClientOpenContent</a>.

## -parameters

### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>.

### -param hContentHandle [in]

A <b>PEERDIST_CONTENT_HANDLE</b> opened by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientopencontent">PeerDistClientOpenContent</a>.

### -param cbNumberOfBytes

Number of bytes in the <i>pBuffer</i> array.

### -param pBuffer [in]

Pointer to the buffer that contains the content information. This buffer must remain valid for the duration of the add operation. The caller must not use this buffer until the add operation is completed.

### -param lpOverlapped [in]

Pointer to an <a href="/windows/win32/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. The Internal member of <a href="/windows/win32/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure contains the completion status of the asynchronous operation. The Offset and OffsetHigh are reserved and must be 0.

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

In order to retrieve content data from Peer Distribution service the client must add content information that it received from the content server by calling the <b>PeerDistClientAddContentInformation</b> function. When all content information data has been added, the <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientcompletecontentinformation">PeerDistClientCompleteContentInformation</a> function must be called. Once <b>PeerDistClientCompleteContentInformation</b> is complete, the client can call <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientstreamread">PeerDistClientStreamRead</a> or <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientblockread">PeerDistClientBlockRead</a> to retrieve the data from the Peer Distribution system.

When calling this function multiple times on a single content handle, the caller must wait for each operation to complete before the next call is made.

An application is  not limited  to adding  content information with a single <b>PeerDistClientAddContentInformation</b> API call, as it is possible to add portions of that content information as it is made available. When more content information is available, the application can again call <b>PeerDistClientAddContentInformation</b>. When the application is done adding the entire content information, it must then call <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientcompletecontentinformation">PeerDistClientCompleteContentInformation</a>.

## -see-also

<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientcompletecontentinformation">PeerDistClientCompleteContentInformation</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientopencontent">PeerDistClientOpenContent</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>