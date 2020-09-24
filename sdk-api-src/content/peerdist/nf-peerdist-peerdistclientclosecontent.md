---
UID: NF:peerdist.PeerDistClientCloseContent
title: PeerDistClientCloseContent function (peerdist.h)
description: PeerDistClientCloseContent function closes the content handle opened by PeerDistClientOpenContent.
helpviewer_keywords: ["PeerDistClientCloseContent","PeerDistClientCloseContent function [Peer Networking]","p2p.peerdistclientclosecontent","peerdist/PeerDistClientCloseContent"]
old-location: p2p\peerdistclientclosecontent.htm
tech.root: p2p
ms.assetid: c55300b7-13b6-42bf-b673-56a5e077416d
ms.date: 12/05/2018
ms.keywords: PeerDistClientCloseContent, PeerDistClientCloseContent function [Peer Networking], p2p.peerdistclientclosecontent, peerdist/PeerDistClientCloseContent
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
 - PeerDistClientCloseContent
 - peerdist/PeerDistClientCloseContent
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
 - PeerDistClientCloseContent
---

# PeerDistClientCloseContent function


## -description

The <b>PeerDistClientCloseContent</b> function closes the content handle opened by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientopencontent">PeerDistClientOpenContent</a>.

## -parameters

### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>.

### -param hContentHandle [in]

A <b>PEERDIST_CONTENT_HANDLE</b> opened  by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientopencontent">PeerDistClientOpenContent</a>.

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
The <i>hPeerDist</i> or <i>hContent</i> handle is invalid.

</td>
</tr>
</table>

## -remarks

This function will cancel all pending asynchronous operations associated with the provided <i>hContentHandle</i>.

 All handles opened by the <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientopencontent">PeerDistClientOpenContent</a> function must be closed by <b>PeerDistClientCloseContent</b>.

## -see-also

<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientopencontent">PeerDistClientOpenContent</a>