---
UID: NS:netioapi._MIB_IPNET_ROW2
title: MIB_IPNET_ROW2 (netioapi.h)
description: Stores information about a neighbor IP address.
helpviewer_keywords: ["*PMIB_IPNET_ROW2","MIB_IPNET_ROW2","MIB_IPNET_ROW2 structure [MIB]","NlnsDelay","NlnsIncomplete","NlnsMaximum","NlnsPermanent","NlnsProbe","NlnsReachable","NlnsStale","NlnsUnreachable","PMIB_IPNET_ROW2","PMIB_IPNET_ROW2 structure pointer [MIB]","_MIB_IPNET_ROW2","mib.mib_ipnet_row2","netioapi/MIB_IPNET_ROW2","netioapi/PMIB_IPNET_ROW2"]
old-location: mib\mib_ipnet_row2.htm
tech.root: MIB
ms.assetid: 164dbd93-4464-40f9-989a-17597102b1d8
ms.date: 12/05/2018
ms.keywords: '*PMIB_IPNET_ROW2, MIB_IPNET_ROW2, MIB_IPNET_ROW2 structure [MIB], NlnsDelay, NlnsIncomplete, NlnsMaximum, NlnsPermanent, NlnsProbe, NlnsReachable, NlnsStale, NlnsUnreachable, PMIB_IPNET_ROW2, PMIB_IPNET_ROW2 structure pointer [MIB], _MIB_IPNET_ROW2, mib.mib_ipnet_row2, netioapi/MIB_IPNET_ROW2, netioapi/PMIB_IPNET_ROW2'
req.header: netioapi.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MIB_IPNET_ROW2, *PMIB_IPNET_ROW2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_IPNET_ROW2
 - netioapi/_MIB_IPNET_ROW2
 - PMIB_IPNET_ROW2
 - netioapi/PMIB_IPNET_ROW2
 - MIB_IPNET_ROW2
 - netioapi/MIB_IPNET_ROW2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Netioapi.h
api_name:
 - MIB_IPNET_ROW2
---

# MIB_IPNET_ROW2 structure


## -description

The 
<b>MIB_IPNET_ROW2</b> structure stores information about a neighbor IP address.

## -struct-fields

### -field Address

Type: <b><a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-sockaddr_inet">SOCKADDR_INET</a></b>

The neighbor IP address. This member can be an IPv6 address or an IPv4 address.

### -field InterfaceIndex

Type: <b>NET_IFINDEX</b>

The local index value for the network interface associated with this IP address. This index value may change when a network adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.

### -field InterfaceLuid

Type: <b>NET_LUID</b>

The locally unique identifier (LUID) for the network interface associated with this IP address.

### -field PhysicalAddress

Type: <b> UCHAR[IF_MAX_PHYS_ADDRESS_LENGTH]</b>

The physical hardware address of the adapter for the network interface associated with this IP address.

### -field PhysicalAddressLength

Type: <b>ULONG</b>

The length, in bytes, of the physical hardware address specified by the <b>PhysicalAddress</b> member. The maximum value supported is 32 bytes.

### -field State

Type: <b>NL_NEIGHBOR_STATE</b>

The state of a network neighbor IP address as defined in RFC 2461, section 7.3.2. For more information, see <a href="https://www.ietf.org/rfc/rfc2461.txt">http://www.ietf.org/rfc/rfc2461.txt</a>. This member can be one of the values from the <b>NL_NEIGHBOR_STATE</b> enumeration type defined in the <i>Nldef.h</i> header file. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NlnsUnreachable"></a><a id="nlnsunreachable"></a><a id="NLNSUNREACHABLE"></a><dl>
<dt><b>NlnsUnreachable</b></dt>
</dl>
</td>
<td width="60%">
The IP address is unreachable.

</td>
</tr>
<tr>
<td width="40%"><a id="NlnsIncomplete"></a><a id="nlnsincomplete"></a><a id="NLNSINCOMPLETE"></a><dl>
<dt><b>NlnsIncomplete</b></dt>
</dl>
</td>
<td width="60%">
Address resolution is in progress and the link-layer
                  address of the neighbor has not yet been determined. Specifically for IPv6, a Neighbor Solicitation has been sent to the solicited-node multicast IP address of the target, but the corresponding neighbor advertisement has not yet been received.

</td>
</tr>
<tr>
<td width="40%"><a id="NlnsProbe"></a><a id="nlnsprobe"></a><a id="NLNSPROBE"></a><dl>
<dt><b>NlnsProbe</b></dt>
</dl>
</td>
<td width="60%">
The neighbor is no longer known to be reachable, and
                  probes are being sent to
                  verify reachability.
For IPv6, a reachability confirmation is actively being sought by retransmitting unicast Neighbor Solicitation probes at regular intervals until a reachability confirmation is received.



</td>
</tr>
<tr>
<td width="40%"><a id="NlnsDelay"></a><a id="nlnsdelay"></a><a id="NLNSDELAY"></a><dl>
<dt><b>NlnsDelay</b></dt>
</dl>
</td>
<td width="60%">
The neighbor is no longer known to be reachable, and
                  traffic has recently been sent to the neighbor.
                  Rather than probe the neighbor immediately, however,
                  delay sending probes for a short while in order to
                  give upper layer protocols a chance to provide
                  reachability confirmation. For IPv6, more time has elapsed than is specified in  the <b>ReachabilityTime.ReachableTime</b> member since the last positive confirmation was received that the forward path was functioning properly and a  packet was sent.  If no  reachability confirmation is received within a period of time (used to delay the first probe) of entering the <b>NlnsDelay</b> state, then a neighbor solicitation is sent and the <b>State</b>  member is changed to  <b>NlnsProbe</b>.


</td>
</tr>
<tr>
<td width="40%"><a id="NlnsStale"></a><a id="nlnsstale"></a><a id="NLNSSTALE"></a><dl>
<dt><b>NlnsStale</b></dt>
</dl>
</td>
<td width="60%">
The neighbor is no longer known to be reachable but
                  until traffic is sent to the neighbor, no attempt
                  should be made to verify its reachability. For IPv6, more time has elapsed than is specified in  the <b>ReachabilityTime.ReachableTime</b> member since the last positive confirmation was received that the forward path was functioning properly. 
While the <b>State</b> is <b>NlnsStale</b>, no action takes place until a packet is sent.

The <b>NlnsStale</b> state is entered upon receiving an unsolicited neighbor discovery message that updates the cached IP address. Receipt of such a message does not confirm reachability, and entering the <b>NlnsStale</b> state insures reachability is verified quickly if the entry is actually being used. However,
reachability is not actually verified until the entry is actually used.

</td>
</tr>
<tr>
<td width="40%"><a id="NlnsReachable"></a><a id="nlnsreachable"></a><a id="NLNSREACHABLE"></a><dl>
<dt><b>NlnsReachable</b></dt>
</dl>
</td>
<td width="60%">
The neighbor is known to have been
                  reachable recently (within tens of seconds ago). For IPv6, a positive confirmation was received within the time specified in  the <b>ReachabilityTime.ReachableTime</b> member that the forward path to the neighbor was functioning properly. While the <b>State</b> is <b>NlnsReachable</b>, no special action takes place as packets are sent.

</td>
</tr>
<tr>
<td width="40%"><a id="NlnsPermanent"></a><a id="nlnspermanent"></a><a id="NLNSPERMANENT"></a><dl>
<dt><b>NlnsPermanent</b></dt>
</dl>
</td>
<td width="60%">
The IP address is a permanent address.

</td>
</tr>
<tr>
<td width="40%"><a id="NlnsMaximum"></a><a id="nlnsmaximum"></a><a id="NLNSMAXIMUM"></a><dl>
<dt><b>NlnsMaximum</b></dt>
</dl>
</td>
<td width="60%">
The maximum possible value for the <b>NL_NEIGHBOR_STATE</b> enumeration type. This is not a legal value for the <b>State</b> member.

</td>
</tr>
</table>

### -field IsRouter

Type: <b>BOOLEAN</b>

A value that indicates if this IP address is a router.

### -field IsUnreachable

Type: <b>BOOLEAN</b>

A value that indicates if this IP address is unreachable.

### -field Flags

Type: <b>UCHAR</b>

A set of flags that indicate whether the IP address is a router and whether the IP address is unreachable.

### -field ReachabilityTime

### -field ReachabilityTime.LastReachable

Type: <b>ULONG</b>

The time, in
                     milliseconds, that a node assumes a neighbor is
                     reachable after having received a reachability
                     confirmation.

### -field ReachabilityTime.LastUnreachable

Type: <b>ULONG</b>

The time, in
                     milliseconds, that a node assumes a neighbor is
                     unreachable after not having received a reachability
                     confirmation.

## -remarks

The <b>MIB_IPNET_ROW2</b> structure is defined on Windows Vista and later. 

The <b>GetIpNetTable2</b> function enumerates the neighbor IP addresses on a local system and returns this information in an <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipnet_table2">MIB_IPNET_TABLE2</a> structure. 

For IPv4, this includes addresses determined used the Address Resolution Protocol (ARP). For IPv6, this includes addresses determined using the Neighbor Discovery (ND) protocol for IPv6 as specified in RFC 2461. For more information, see <a href="https://www.ietf.org/rfc/rfc2461.txt">http://www.ietf.org/rfc/rfc2461.txt</a>. 

The <a href="/windows/desktop/api/netioapi/nf-netioapi-getipnetentry2">GetIpNetEntry2</a> function retrieves a single neighbor IP address and returns this information in a <b>MIB_IPNET_ROW2</b> structure.

Note that the <i>Netioapi.h</i> header file is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Netioapi.h</i> header file should never be used directly.

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-createipnetentry2">CreateIpNetEntry2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getipnetentry2">GetIpNetEntry2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getipnettable2">GetIpNetTable2</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipnet_table2">MIB_IPNET_TABLE2</a>



<a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-sockaddr_inet">SOCKADDR_INET</a>