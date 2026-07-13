---
UID: NS:netioapi._MIB_IPFORWARD_ROW2
title: MIB_IPFORWARD_ROW2 (netioapi.h)
description: Stores information about an IP route entry.
helpviewer_keywords: ["*PMIB_IPFORWARD_ROW2","MIB_IPFORWARD_ROW2","MIB_IPFORWARD_ROW2 structure [MIB]","MIB_IPPROTO_BBN","MIB_IPPROTO_BGP","MIB_IPPROTO_CISCO","MIB_IPPROTO_EGP","MIB_IPPROTO_ES_IS","MIB_IPPROTO_GGP","MIB_IPPROTO_HELLO","MIB_IPPROTO_ICMP","MIB_IPPROTO_IS_IS","MIB_IPPROTO_LOCAL","MIB_IPPROTO_NETMGMT","MIB_IPPROTO_NT_AUTOSTATIC","MIB_IPPROTO_NT_STATIC","MIB_IPPROTO_NT_STATIC_NON_DOD","MIB_IPPROTO_OSPF","MIB_IPPROTO_OTHER","MIB_IPPROTO_RIP","Nlro6to4","NlroDHCP","NlroManual","NlroRouterAdvertisement","NlroWellKnown","PMIB_IPFORWARD_ROW2","PMIB_IPFORWARD_ROW2 structure pointer [MIB]","_MIB_IPFORWARD_ROW2","mib.mib_ipforward_row2","netioapi/MIB_IPFORWARD_ROW2","netioapi/PMIB_IPFORWARD_ROW2"]
old-location: mib\mib_ipforward_row2.htm
tech.root: MIB
ms.assetid: 3678315d-b6ab-48c8-8522-a57deb63f8c9
ms.date: 12/05/2018
ms.keywords: '*PMIB_IPFORWARD_ROW2, MIB_IPFORWARD_ROW2, MIB_IPFORWARD_ROW2 structure [MIB], MIB_IPPROTO_BBN, MIB_IPPROTO_BGP, MIB_IPPROTO_CISCO, MIB_IPPROTO_EGP, MIB_IPPROTO_ES_IS, MIB_IPPROTO_GGP, MIB_IPPROTO_HELLO, MIB_IPPROTO_ICMP, MIB_IPPROTO_IS_IS, MIB_IPPROTO_LOCAL, MIB_IPPROTO_NETMGMT, MIB_IPPROTO_NT_AUTOSTATIC, MIB_IPPROTO_NT_STATIC, MIB_IPPROTO_NT_STATIC_NON_DOD, MIB_IPPROTO_OSPF, MIB_IPPROTO_OTHER, MIB_IPPROTO_RIP, Nlro6to4, NlroDHCP, NlroManual, NlroRouterAdvertisement, NlroWellKnown, PMIB_IPFORWARD_ROW2, PMIB_IPFORWARD_ROW2 structure pointer [MIB], _MIB_IPFORWARD_ROW2, mib.mib_ipforward_row2, netioapi/MIB_IPFORWARD_ROW2, netioapi/PMIB_IPFORWARD_ROW2'
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
req.typenames: MIB_IPFORWARD_ROW2, *PMIB_IPFORWARD_ROW2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_IPFORWARD_ROW2
 - netioapi/_MIB_IPFORWARD_ROW2
 - PMIB_IPFORWARD_ROW2
 - netioapi/PMIB_IPFORWARD_ROW2
 - MIB_IPFORWARD_ROW2
 - netioapi/MIB_IPFORWARD_ROW2
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
 - MIB_IPFORWARD_ROW2
---

# MIB_IPFORWARD_ROW2 structure


## -description

The 
<b>MIB_IPFORWARD_ROW2</b> structure stores information about an IP route entry.

## -struct-fields

### -field InterfaceLuid

Type: <b>NET_LUID</b>

The locally unique identifier (LUID) for the network interface associated with this IP route entry.

### -field InterfaceIndex

Type: <b>NET_IFINDEX</b>

The local index value for the network interface associated with this IP route entry. This index value may change when a network adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.

### -field DestinationPrefix

Type: <b><a href="/windows/desktop/api/netioapi/ns-netioapi-ip_address_prefix">IP_ADDRESS_PREFIX</a></b>

The IP address prefix for the destination IP address for this route.

### -field NextHop

Type: <b><a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-sockaddr_inet">SOCKADDR_INET</a></b>

For a remote route, the IP address of the next system or gateway en route. If the route is to a local loopback address or an IP address on the local link, the next hop is unspecified (all zeros). For a local loopback route, this member should be an IPv4 address of 0.0.0.0 for an IPv4 route entry or an IPv6 address of 0::0 for an IPv6 route entry.

### -field SitePrefixLength

Type: <b>UCHAR</b>

The length, in bits, of the site prefix or network part of the IP address for this route. For an IPv4 route entry, any value greater than 32 is an illegal value. For an IPv6 route entry, any value greater than 128 is an illegal value. 
A value of 255 is commonly used to represent an illegal value.

### -field ValidLifetime

Type: <b>ULONG</b>

The maximum time, in seconds, that the IP route entry is valid. A value of 0xffffffff  is considered to be infinite.

### -field PreferredLifetime

Type: <b>ULONG</b>

The preferred time, in seconds, that the IP route entry is valid. A value of 0xffffffff is considered to be infinite.

### -field Metric

Type: <b>ULONG</b>

The route metric offset value for this IP route entry. Note the actual route metric used to compute the route preference is the summation of interface metric specified in the <b>Metric</b> member of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipinterface_row">MIB_IPINTERFACE_ROW</a> structure and the route metric offset specified in this member. The semantics of this metric are determined by the routing protocol specified in the <b>Protocol</b> member. If this metric is not used, its value should be set to -1. This value is documented in RFC 4292. 
For more information, see <a href="https://www.ietf.org/rfc/rfc4292.txt">http://www.ietf.org/rfc/rfc4292.txt</a>.

### -field Protocol

Type: <b>NL_ROUTE_PROTOCOL</b>

The routing mechanism how this IP route was added. This member can be one of the values from the <b>NL_ROUTE_PROTOCOL</b> enumeration type defined in the <i>Nldef.h</i> header file. The member is described in RFC 4292. For more information, see <a href="https://www.ietf.org/rfc/rfc4292.txt">http://www.ietf.org/rfc/rfc4292.txt</a>. 

Note that the <i>Nldef.h</i> header is automatically included by the <i>Ipmib.h</i> header file which is automatically included by the <i>Iprtrmib.h</i> header. The <i>Iphlpapi.h</i> header  automatically includes the <i>Iprtrmib.h</i> header file. The  <i>Iprtrmib.h</i>, <i>Ipmib.h</i>, and <i>Nldef.h</i> header files should never be used directly.  

The following list shows the possible values for this member. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MIB_IPPROTO_OTHER"></a><a id="mib_ipproto_other"></a><dl>
<dt><b>MIB_IPPROTO_OTHER</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The routing mechanism was  not specified. 

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IPPROTO_LOCAL"></a><a id="mib_ipproto_local"></a><dl>
<dt><b>MIB_IPPROTO_LOCAL</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
A local interface.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IPPROTO_NETMGMT"></a><a id="mib_ipproto_netmgmt"></a><dl>
<dt><b>MIB_IPPROTO_NETMGMT</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
A static route. This value is used to identify route information for IP  routing set through network management such as the Dynamic Host Configuration Protocol (DCHP), the Simple Network Management Protocol (SNMP), or by calls to the <a href="/windows/desktop/api/netioapi/nf-netioapi-createipforwardentry2">CreateIpForwardEntry2</a>,  <a href="/windows/desktop/api/netioapi/nf-netioapi-deleteipforwardentry2">DeleteIpForwardEntry2</a>, or <a href="/windows/desktop/api/netioapi/nf-netioapi-setipforwardentry2">SetIpForwardEntry2</a> functions.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IPPROTO_ICMP"></a><a id="mib_ipproto_icmp"></a><dl>
<dt><b>MIB_IPPROTO_ICMP</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The result of an ICMP redirect.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IPPROTO_EGP"></a><a id="mib_ipproto_egp"></a><dl>
<dt><b>MIB_IPPROTO_EGP</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The Exterior Gateway Protocol (EGP), a dynamic routing protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IPPROTO_GGP"></a><a id="mib_ipproto_ggp"></a><dl>
<dt><b>MIB_IPPROTO_GGP</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The Gateway-to-Gateway Protocol (GGP), a dynamic routing protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IPPROTO_HELLO"></a><a id="mib_ipproto_hello"></a><dl>
<dt><b>MIB_IPPROTO_HELLO</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
The Hellospeak protocol, a dynamic routing protocol. This is a historical entry no longer in use and was an early routing protocol used by the original ARPANET routers that ran special software called the Fuzzball routing protocol, sometimes called Hellospeak, as described in 
RFC 891 and RFC 1305. For more information, see <a href="https://www.ietf.org/rfc/rfc891.txt">http://www.ietf.org/rfc/rfc891.txt</a> and <a href="http://tools.ietf.org/html/rfc1305">http://www.ietf.org/rfc/rfc1305.txt</a>. 

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IPPROTO_RIP"></a><a id="mib_ipproto_rip"></a><dl>
<dt><b>MIB_IPPROTO_RIP</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
The Berkeley Routing Information Protocol (RIP) or RIP-II, a dynamic routing protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IPPROTO_IS_IS"></a><a id="mib_ipproto_is_is"></a><dl>
<dt><b>MIB_IPPROTO_IS_IS</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
The Intermediate System-to-Intermediate System (IS-IS) protocol, a dynamic routing protocol. The IS-IS protocol was developed for use in  the Open Systems Interconnection (OSI) protocol suite. 

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IPPROTO_ES_IS"></a><a id="mib_ipproto_es_is"></a><dl>
<dt><b>MIB_IPPROTO_ES_IS</b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
The End System-to-Intermediate System (ES-IS) protocol, a dynamic routing protocol. The ES-IS protocol was developed for use in  the Open Systems Interconnection (OSI) protocol suite. 

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IPPROTO_CISCO"></a><a id="mib_ipproto_cisco"></a><dl>
<dt><b>MIB_IPPROTO_CISCO</b></dt>
<dt>11</dt>
</dl>
</td>
<td width="60%">
The Cisco Interior Gateway Routing Protocol (IGRP), a dynamic routing protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IPPROTO_BBN"></a><a id="mib_ipproto_bbn"></a><dl>
<dt><b>MIB_IPPROTO_BBN</b></dt>
<dt>12</dt>
</dl>
</td>
<td width="60%">
The Bolt, Beranek, and Newman (BBN) Interior Gateway Protocol (IGP) that used the Shortest Path First (SPF) algorithm. This was an early dynamic routing protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IPPROTO_OSPF"></a><a id="mib_ipproto_ospf"></a><dl>
<dt><b>MIB_IPPROTO_OSPF</b></dt>
<dt>13</dt>
</dl>
</td>
<td width="60%">
The Open Shortest Path First (OSPF) protocol, a dynamic routing protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IPPROTO_BGP"></a><a id="mib_ipproto_bgp"></a><dl>
<dt><b>MIB_IPPROTO_BGP</b></dt>
<dt>14</dt>
</dl>
</td>
<td width="60%">
The Border Gateway Protocol (BGP), a dynamic routing protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IPPROTO_NT_AUTOSTATIC"></a><a id="mib_ipproto_nt_autostatic"></a><dl>
<dt><b>MIB_IPPROTO_NT_AUTOSTATIC</b></dt>
<dt>10002</dt>
</dl>
</td>
<td width="60%">
A Windows specific entry added originally by a routing protocol, but which is now static.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IPPROTO_NT_STATIC"></a><a id="mib_ipproto_nt_static"></a><dl>
<dt><b>MIB_IPPROTO_NT_STATIC</b></dt>
<dt>10006</dt>
</dl>
</td>
<td width="60%">
A Windows specific entry added as a static route from the routing user interface or a routing command. 

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IPPROTO_NT_STATIC_NON_DOD"></a><a id="mib_ipproto_nt_static_non_dod"></a><dl>
<dt><b>MIB_IPPROTO_NT_STATIC_NON_DOD</b></dt>
<dt>10007</dt>
</dl>
</td>
<td width="60%">
A Windows specific entry added as a static route from the routing user interface or a routing command, except these routes do not cause Dial On Demand (DOD).

</td>
</tr>
</table>

### -field Loopback

Type: <b>BOOLEAN</b>

A value that specifies if the route is a loopback route (the gateway is on the local host).

### -field AutoconfigureAddress

Type: <b>BOOLEAN</b>

A value that specifies if the IP address is autoconfigured.

### -field Publish

Type: <b>BOOLEAN</b>

A value that specifies if the route is published.

### -field Immortal

Type: <b>BOOLEAN</b>

A value that specifies if the route is immortal.

### -field Age

Type: <b>ULONG</b>

The number of seconds  since  the  route  was
                added or modified in the network routing table.

### -field Origin

Type: <b>NL_ROUTE_ORIGIN</b>

The origin of the route. This member can be one of the values from the <b>NL_ROUTE_ORIGIN</b> enumeration type defined in the <i>Nldef.h</i> header file. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NlroManual"></a><a id="nlromanual"></a><a id="NLROMANUAL"></a><dl>
<dt><b>NlroManual</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
A result of manual configuration. 

</td>
</tr>
<tr>
<td width="40%"><a id="NlroWellKnown"></a><a id="nlrowellknown"></a><a id="NLROWELLKNOWN"></a><dl>
<dt><b>NlroWellKnown</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
A well-known route.

</td>
</tr>
<tr>
<td width="40%"><a id="NlroDHCP"></a><a id="nlrodhcp"></a><a id="NLRODHCP"></a><dl>
<dt><b>NlroDHCP</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
A result of DHCP configuration.

</td>
</tr>
<tr>
<td width="40%"><a id="NlroRouterAdvertisement"></a><a id="nlrorouteradvertisement"></a><a id="NLROROUTERADVERTISEMENT"></a><dl>
<dt><b>NlroRouterAdvertisement</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The result of router advertisement.

</td>
</tr>
<tr>
<td width="40%"><a id="Nlro6to4"></a><a id="nlro6to4"></a><a id="NLRO6TO4"></a><dl>
<dt><b>Nlro6to4</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
A result of 6to4 tunneling.

</td>
</tr>
</table>

## -remarks

The <b>MIB_IPFORWARD_ROW2</b> structure is defined on Windows Vista and later. 

The <b>GetIpForwardTable2</b> function enumerates the IP route entries on a local system and returns this information in a <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipforward_table2">MIB_IPFORWARD_TABLE2</a> structure as an array of <b>MIB_IPFORWARD_ROW2</b> entries. 



The <b>GetIpForwardEntry2</b> function retrieves a single IP route entry and returns this information in a <b>MIB_IPFORWARD_ROW2</b> structure.

An entry with the <b>Prefix</b> and the <b>PrefixLength</b> members of the <a href="/windows/desktop/api/netioapi/ns-netioapi-ip_address_prefix">IP_ADDRESS_PREFIX</a> set to zero in the <b>DestinationPrefix</b> member in the 
<b>MIB_IPFORWARD_ROW2</b> structure is considered a
                default route. The <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipforward_table2">MIB_IPFORWARD_TABLE2</a> may contain multiple <b>MIB_IPFORWARD_ROW2</b> entries with the <b>Prefix</b> and the <b>PrefixLength</b> members of the <b>IP_ADDRESS_PREFIX</b> set to zero in the <b>DestinationPrefix</b> member when there are multiple network adapters installed.

The <b>Metric</b> member of a <b>MIB_IPFORWARD_ROW2</b> entry is a value that is assigned to an IP route for a particular network interface that identifies the cost that is associated with using that route. For example, the metric can be valued in terms of link speed, hop count, or time delay. Automatic metric is a feature on Windows XP and later that automatically configures the metric for the local routes that are based on link speed. The automatic metric feature is enabled by default (the <b>UseAutomaticMetric</b> member of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipinterface_row">MIB_IPINTERFACE_ROW</a> structure is set to <b>TRUE</b>) on Windows XP and later. It can also be manually configured to assign a specific metric to an IP route.



The route metric specified in the <b>Metric</b> member of the  <b>MIB_IPFORWARD_ROW2</b> structure represents just the route metric offset. The complete metric is a combination of this route metric  offset added to the interface metric specified in the <b>Metric</b> member of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipinterface_row">MIB_IPINTERFACE_ROW</a> structure of the associated interface.  An application can retrieve the interface metric by calling the <a href="/windows/desktop/api/netioapi/nf-netioapi-getipinterfaceentry">GetIpInterfaceEntry</a> function.

Note that the <i>Netioapi.h</i> header file is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Netioapi.h</i> header file should never be used directly.

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-createipforwardentry2">CreateIpForwardEntry2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-deleteipforwardentry2">DeleteIpForwardEntry2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getipforwardentry2">GetIpForwardEntry2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getipforwardtable2">GetIpForwardTable2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getipinterfaceentry">GetIpInterfaceEntry</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-ip_address_prefix">IP_ADDRESS_PREFIX</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipforward_table2">MIB_IPFORWARD_TABLE2</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipinterface_row">MIB_IPINTERFACE_ROW</a>



<a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-sockaddr_inet">SOCKADDR_INET</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-setipforwardentry2">SetIpForwardEntry2</a>