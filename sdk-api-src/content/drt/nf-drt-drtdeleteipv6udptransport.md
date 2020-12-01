---
UID: NF:drt.DrtDeleteIpv6UdpTransport
title: DrtDeleteIpv6UdpTransport function (drt.h)
description: DrtDeleteIpv6UdpTransport function deletes a transport based on the IPv6 UDP protocol.
helpviewer_keywords: ["DrtDeleteIpv6UdpTransport","DrtDeleteIpv6UdpTransport function [Peer Networking]","drt/DrtDeleteIpv6UdpTransport","p2p.drtdeleteipv6udptransport"]
old-location: p2p\drtdeleteipv6udptransport.htm
tech.root: p2p
ms.assetid: 9b078f63-36b1-448b-b0c2-d452699157d8
ms.date: 12/05/2018
ms.keywords: DrtDeleteIpv6UdpTransport, DrtDeleteIpv6UdpTransport function [Peer Networking], drt/DrtDeleteIpv6UdpTransport, p2p.drtdeleteipv6udptransport
req.header: drt.h
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
req.lib: Drttransport.lib
req.dll: Drt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrtDeleteIpv6UdpTransport
 - drt/DrtDeleteIpv6UdpTransport
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - drt.dll
api_name:
 - DrtDeleteIpv6UdpTransport
---

# DrtDeleteIpv6UdpTransport function


## -description

The <b>DrtDeleteIpv6UdpTransport</b> function deletes a  transport based on the IPv6 UDP protocol.

## -parameters

### -param hTransport [in]

The DRT transport handle specifying the transport to delete.

## -returns

This function returns S_OK on success. Other possible values include:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INVALID_TRANSPORT_PROVIDER</b></dt>
</dl>
</td>
<td width="60%">
<i>hTransport</i> is <b>NULL</b> or invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_TRANSPORT_EXECUTING_CALLBACK</b></dt>
</dl>
</td>
<td width="60%">
The transport provider is currently executing a method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_TRANSPORT_STILL_BOUND</b></dt>
</dl>
</td>
<td width="60%">
The transport is still bound.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_TRANSPORTPROVIDER_IN_USE</b></dt>
</dl>
</td>
<td width="60%">
All clients have not called <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the transport.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  This function may also surface errors returned by underlying calls to <a href="/windows/desktop/api/p2p/nf-p2p-peerpnrpstartup">PeerPnrpStartup</a> or <a href="/windows/desktop/api/p2p/nf-p2p-peeridentitygetcryptkey">PeerIdentityGetCryptKey</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport">DrtCreateIpv6UdpTransport</a>