---
UID: NF:peerdist.PeerDistClientFlushContent
title: PeerDistClientFlushContent function (peerdist.h)
description: The PeerDistClientFlushContent function allows a client to remove content added to the local cache with the PeerDistClientAddData function using the associated PEERDIST_CONTENT_TAG.
helpviewer_keywords: ["PeerDistClientFlushContent","PeerDistClientFlushContent function [Peer Networking]","p2p.peerdistclientflushcontent","peerdist/PeerDistClientFlushContent"]
old-location: p2p\peerdistclientflushcontent.htm
tech.root: p2p
ms.assetid: bb77499b-520b-4def-97d8-504983953d4b
ms.date: 12/05/2018
ms.keywords: PeerDistClientFlushContent, PeerDistClientFlushContent function [Peer Networking], p2p.peerdistclientflushcontent, peerdist/PeerDistClientFlushContent
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
 - PeerDistClientFlushContent
 - peerdist/PeerDistClientFlushContent
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
 - PeerDistClientFlushContent
---

# PeerDistClientFlushContent function


## -description

The [PEERDIST_CONTENT_TAG](./ns-peerdist-peerdist_content_tag.md).

## -parameters

### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>.

### -param pContentTag [in]

Pointer to a [PEERDIST_CONTENT_TAG](./ns-peerdist-peerdist_content_tag.md) structure that contains the tag supplied when <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientopencontent">PeerDistClientOpenContent</a> is called.

### -param hCompletionPort [in, optional]

A handle to the completion port that can be used for retrieving the completion notification of the asynchronous function. To create a completion port, use the <a href="/windows/desktop/FileIO/createiocompletionport">CreateIoCompletionPort</a> function. This parameter can be <b>NULL</b>.

### -param ulCompletionKey [in, optional]

Value to be returned through the <i>lpCompletionKey</i> parameter of the <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a> function. This parameter is ignored when <i>hCompletionPort</i> is <b>NULL</b>.

### -param lpOverlapped [in]

Pointer to an <a href="/windows/win32/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. <b>Offset</b> and <b>OffsetHigh</b> are reserved and must be zero.

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

The <i>pContentTag</i> is a client supplied tag passed to <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientopencontent">PeerDistClientOpenContent</a>, which labels the content added by the client. This tag is used by the API to selectively flush content from the Peer Distribution cache.

## -see-also

[PEERDIST_CONTENT_TAG](./ns-peerdist-peerdist_content_tag.md)



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientopencontent">PeerDistClientOpenContent</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>