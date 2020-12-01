---
UID: NF:peerdist.PeerDistServerUnpublish
title: PeerDistServerUnpublish function (peerdist.h)
description: PeerDistServerUnpublish function removes a publication created via PeerDistServerPublishStream.
helpviewer_keywords: ["PeerDistServerUnpublish","PeerDistServerUnpublish function [Peer Networking]","p2p.peerdistserverunpublish","peerdist/PeerDistServerUnpublish"]
old-location: p2p\peerdistserverunpublish.htm
tech.root: p2p
ms.assetid: 880927c4-f7d7-4c75-b371-2fe401a50b20
ms.date: 12/05/2018
ms.keywords: PeerDistServerUnpublish, PeerDistServerUnpublish function [Peer Networking], p2p.peerdistserverunpublish, peerdist/PeerDistServerUnpublish
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
 - PeerDistServerUnpublish
 - peerdist/PeerDistServerUnpublish
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
 - PeerDistServerUnpublish
---

# PeerDistServerUnpublish function


## -description

The <b>PeerDistServerUnpublish</b> function removes a publication created via <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverpublishstream">PeerDistServerPublishStream</a>.

## -parameters

### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdiststartup">PeerDistStartup</a>.

### -param cbContentIdentifier

The length, in bytes, of the content identifier.

### -param pContentIdentifier [in]

Pointer to a buffer that contains the content identifier.

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

The <b>PeerDistServerUnpublish</b> function cancels all pending operations on unpublished content within the Peer Distribution session that is associated with the specified <i>hPeerDist</i>. The client is still required  to close previously opened handles on that content with a call to <a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistclientclosecontent">PeerDistClientCloseContent</a>.

A publication is accessible only to the User Account that originally published the content.

## -see-also

<a href="/windows/desktop/api/peerdist/nf-peerdist-peerdistserverpublishstream">PeerDistServerPublishStream</a>