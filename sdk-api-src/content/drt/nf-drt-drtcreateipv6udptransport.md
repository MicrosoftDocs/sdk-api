---
UID: NF:drt.DrtCreateIpv6UdpTransport
title: DrtCreateIpv6UdpTransport function (drt.h)
description: DrtCreateIpv6UdpTransport function creates a transport based on the IPv6 UDP protocol.
helpviewer_keywords: ["DrtCreateIpv6UdpTransport","DrtCreateIpv6UdpTransport function [Peer Networking]","drt/DrtCreateIpv6UdpTransport","p2p.drtcreateipv6udptransport"]
old-location: p2p\drtcreateipv6udptransport.htm
tech.root: p2p
ms.assetid: def3120b-98b6-4e31-8166-822cea7fea69
ms.date: 12/05/2018
ms.keywords: DrtCreateIpv6UdpTransport, DrtCreateIpv6UdpTransport function [Peer Networking], drt/DrtCreateIpv6UdpTransport, p2p.drtcreateipv6udptransport
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
 - DrtCreateIpv6UdpTransport
 - drt/DrtCreateIpv6UdpTransport
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
 - DrtCreateIpv6UdpTransport
---

# DrtCreateIpv6UdpTransport function


## -description

The <b>DrtCreateIpv6UdpTransport</b> function creates a  transport based on the IPv6 UDP protocol.

## -parameters

### -param scope

The <b>DRT_SCOPE</b> enumeration that specifies the IPv6 scope in which the DRT is to  operate.

### -param dwScopeId

The identifier that uniquely specifies the interface the scope is associated with.

For the Global scope this parameter is always the "GLOBAL_" ID and is optional when using only the global scope.
For the link local scope, this parameter represents the interface associated with the Network Interface Card on which the link local scope exists.

### -param dwLocalityThreshold

The identifier that specifies how Locality information based on IpV6 addresses is used when caching neighbors.  By default, the DRT gives preference to neighbors that have an IPv6 address with a prefix in common with the local machine.

### -param pwPort [in, out]

Pointer to the port utilized by the local DRT instance.

### -param phTransport [out]

Pointer to a DRT transport handle specified in the <a href="/windows/desktop/api/drt/ns-drt-drt_settings">DRT_SETTINGS</a> structure.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system cannot allocate memory for the provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INVALID_PORT</b></dt>
</dl>
</td>
<td width="60%">
<i>pwPort</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INVALID_TRANSPORT_PROVIDER</b></dt>
</dl>
</td>
<td width="60%">
<i>hTransport</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INVALID_SCOPE</b></dt>
</dl>
</td>
<td width="60%">
The specified scope is not DRT_GLOBAL_SCOPE, DRT_SITE_LOCAL_SCOPE  or DRT_LINK_LOCAL_SCOPE.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_TRANSPORT_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.  See TraceError for reason.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  This function may also return errors from underlying calls to <a href="/windows/desktop/api/netioapi/nf-netioapi-notifyunicastipaddresschange">NotifyUnicastIpAddressChange</a>,<a href="/windows/desktop/api/winsock/nf-winsock-wsastartup">WSAStartup</a>, <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses">GetAdaptersAddresses</a>, <a href="/windows/desktop/api/winsock/nf-winsock-setsockopt">setsockopt</a>, <a href="/windows/desktop/api/winsock2/nf-winsock2-wsasocketa">WSASocket</a>, <a href="/previous-versions/windows/hardware/network/ff566268(v=vs.85)">Bind</a>, <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a>, <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolio">CreateThreadpoolIo</a>, <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolcleanupgroup">CreateThreadpoolCleanupGroup</a> and <a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue">CreateTimerQueue</a>.</div>
<div> </div>

## -remarks

The default IPv6 UDP Transport  created by this function is specific to the DRT it is created for. As a result it cannot be re-used across multiple DRTs.

When using the Distributed Routing Table API in Windows XP with Service Pack 2 (SP2), support of the IPv6 protocol must be enabled for the creation of a transport using <b>DrtCreateIpv6UdpTransport</b> to be successful.

## -see-also

<a href="/windows/desktop/api/drt/ns-drt-drt_settings">DRT_SETTINGS</a>



<a href="/windows/desktop/api/drt/nf-drt-drtdeleteipv6udptransport">DrtDeleteIpv6UdpTransport</a>