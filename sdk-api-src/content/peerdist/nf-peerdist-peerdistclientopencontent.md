---
UID: NF:peerdist.PeerDistClientOpenContent
title: PeerDistClientOpenContent function (peerdist.h)
description: PeerDistClientOpenContent function opens and returns a PEERDIST_CONTENT_HANDLE. The client uses the content handle to retrieve data from the Peer Distribution service.
helpviewer_keywords: ["PeerDistClientOpenContent","PeerDistClientOpenContent function [Peer Networking]","p2p.peerdistclientopencontent","peerdist/PeerDistClientOpenContent"]
old-location: p2p\peerdistclientopencontent.htm
tech.root: p2p
ms.assetid: bf9d4eb2-e939-42c6-8d71-669a949ca77a
ms.date: 12/05/2018
ms.keywords: PeerDistClientOpenContent, PeerDistClientOpenContent function [Peer Networking], p2p.peerdistclientopencontent, peerdist/PeerDistClientOpenContent
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
 - PeerDistClientOpenContent
 - peerdist/PeerDistClientOpenContent
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
 - PeerDistClientOpenContent
---

# PeerDistClientOpenContent function


## -description

The <b>PeerDistClientOpenContent</b> function opens  and returns a PEERDIST_CONTENT_HANDLE. The client uses the content handle to retrieve data from the Peer Distribution service.

## -parameters

### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>.

### -param pContentTag [in]

Pointer to a [PEERDIST_CONTENT_TAG](./ns-peerdist-peerdist_content_tag.md) structure that contains a 16 byte client specified identifier. This parameter is used in conjunction with the <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientflushcontent">PeerDistClientFlushContent</a> function.

### -param hCompletionPort [in, optional]

A handle to the completion port that can be used for retrieving the completion notification of the asynchronous function. To create a completion port, use the <a href="/windows/desktop/FileIO/createiocompletionport">CreateIoCompletionPort</a> function  This parameter can be <b>NULL</b>.

### -param ulCompletionKey [in, optional]

Value to be returned through the <i>lpCompletionKey</i> parameter of the <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a> function.  This parameter is ignored when <i>hCompletionPort</i> is <b>NULL</b>.

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
<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientaddcontentinformation">PeerDistClientAddContentInformation</a>
</li>
<li>
<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientcompletecontentinformation">PeerDistClientCompleteContentInformation</a>
</li>
<li>
<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientblockread">PeerDistClientBlockRead</a>
</li>
<li>
<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientstreamread">PeerDistClientStreamRead</a>
</li>
<li>
<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientadddata">PeerDistClientAddData</a>
</li>
</ul>
If an optional completion port handle is specified, it is used for posting the completion results of above listed asynchronous functions.

The handle returned by <b>PeerDistClientOpenContent</b> function call must be closed by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientclosecontent">PeerDistClientCloseContent</a> function.

## -see-also

<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientaddcontentinformation">PeerDistClientAddContentInformation</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientadddata">PeerDistClientAddData</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientblockread">PeerDistClientBlockRead</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientclosecontent">PeerDistClientCloseContent</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientcompletecontentinformation">PeerDistClientCompleteContentInformation</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientflushcontent">PeerDistClientFlushContent</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientstreamread">PeerDistClientStreamRead</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>