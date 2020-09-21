---
UID: NF:peerdist.PeerDistClientCompleteContentInformation
title: PeerDistClientCompleteContentInformation function (peerdist.h)
description: PeerDistClientCompleteContentInformation function completes the process of adding the content information.
helpviewer_keywords: ["PeerDistClientCompleteContentInformation","PeerDistClientCompleteContentInformation function [Peer Networking]","p2p.peerdistclientcompletecontentinformation","peerdist/PeerDistClientCompleteContentInformation"]
old-location: p2p\peerdistclientcompletecontentinformation.htm
tech.root: p2p
ms.assetid: 0951e5e5-ad00-463e-8aa8-21b11a8acedc
ms.date: 12/05/2018
ms.keywords: PeerDistClientCompleteContentInformation, PeerDistClientCompleteContentInformation function [Peer Networking], p2p.peerdistclientcompletecontentinformation, peerdist/PeerDistClientCompleteContentInformation
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
 - PeerDistClientCompleteContentInformation
 - peerdist/PeerDistClientCompleteContentInformation
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
 - PeerDistClientCompleteContentInformation
---

# PeerDistClientCompleteContentInformation function


## -description

The <b>PeerDistClientCompleteContentInformation</b> function  completes the process of adding the content information.

## -parameters

### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>.

### -param hContentHandle [in]

A <b>PEERDIST_CONTENT_HANDLE</b> returned by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientopencontent">PeerDistClientOpenContent</a>.

### -param lpOverlapped [in]

Pointer to an <a href="/windows/win32/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure.

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

Upon completion of this function, a client can call <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientstreamread">PeerDistClientStreamRead</a> or <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientblockread">PeerDistClientBlockRead</a> to retrieve the data from the Peer Distribution system.

## -see-also

<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientaddcontentinformation">PeerDistClientAddContentInformation</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientopencontent">PeerDistClientOpenContent</a>



<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>