---
UID: NS:ipmib._MIB_IPFORWARDROW
title: MIB_IPFORWARDROW (ipmib.h)
description: Contains information that describes an IPv4 network route.
helpviewer_keywords: ["*PMIB_IPFORWARDROW","MIB_IPFORWARDROW","MIB_IPFORWARDROW structure [MIB]","MIB_IPPROTO_BBN","MIB_IPPROTO_BGP","MIB_IPPROTO_CISCO","MIB_IPPROTO_EGP","MIB_IPPROTO_ES_IS","MIB_IPPROTO_GGP","MIB_IPPROTO_HELLO","MIB_IPPROTO_ICMP","MIB_IPPROTO_IS_IS","MIB_IPPROTO_LOCAL","MIB_IPPROTO_NETMGMT","MIB_IPPROTO_NT_AUTOSTATIC","MIB_IPPROTO_NT_STATIC","MIB_IPPROTO_NT_STATIC_NON_DOD","MIB_IPPROTO_OSPF","MIB_IPPROTO_OTHER","MIB_IPPROTO_RIP","MIB_IPROUTE_TYPE_DIRECT","MIB_IPROUTE_TYPE_INDIRECT","MIB_IPROUTE_TYPE_INVALID","MIB_IPROUTE_TYPE_OTHER","PMIB_IPFORWARDROW","PMIB_IPFORWARDROW structure pointer [MIB]","_mpr_mib_ipforwardrow","ipmib/MIB_IPFORWARDROW","ipmib/PMIB_IPFORWARDROW","iprtrmib/MIB_IPFORWARDROW","iprtrmib/PMIB_IPFORWARDROW","mib.mib_ipforwardrow","rras.mib_ipforwardrow"]
old-location: mib\mib_ipforwardrow.htm
tech.root: MIB
ms.assetid: ff451481-3e9d-4add-94e2-846d67002a38
ms.date: 12/05/2018
ms.keywords: '*PMIB_IPFORWARDROW, MIB_IPFORWARDROW, MIB_IPFORWARDROW structure [MIB], MIB_IPPROTO_BBN, MIB_IPPROTO_BGP, MIB_IPPROTO_CISCO, MIB_IPPROTO_EGP, MIB_IPPROTO_ES_IS, MIB_IPPROTO_GGP, MIB_IPPROTO_HELLO, MIB_IPPROTO_ICMP, MIB_IPPROTO_IS_IS, MIB_IPPROTO_LOCAL, MIB_IPPROTO_NETMGMT, MIB_IPPROTO_NT_AUTOSTATIC, MIB_IPPROTO_NT_STATIC, MIB_IPPROTO_NT_STATIC_NON_DOD, MIB_IPPROTO_OSPF, MIB_IPPROTO_OTHER, MIB_IPPROTO_RIP, MIB_IPROUTE_TYPE_DIRECT, MIB_IPROUTE_TYPE_INDIRECT, MIB_IPROUTE_TYPE_INVALID, MIB_IPROUTE_TYPE_OTHER, PMIB_IPFORWARDROW, PMIB_IPFORWARDROW structure pointer [MIB], _mpr_mib_ipforwardrow, ipmib/MIB_IPFORWARDROW, ipmib/PMIB_IPFORWARDROW, iprtrmib/MIB_IPFORWARDROW, iprtrmib/PMIB_IPFORWARDROW, mib.mib_ipforwardrow, rras.mib_ipforwardrow'
req.header: ipmib.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: MIB_IPFORWARDROW, *PMIB_IPFORWARDROW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_IPFORWARDROW
 - ipmib/_MIB_IPFORWARDROW
 - PMIB_IPFORWARDROW
 - ipmib/PMIB_IPFORWARDROW
 - MIB_IPFORWARDROW
 - ipmib/MIB_IPFORWARDROW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipmib.h
 - Iprtrmib.h
api_name:
 - MIB_IPFORWARDROW
---

# MIB_IPFORWARDROW structure


## -description

The 
<b>MIB_IPFORWARDROW</b> structure contains information that describes an IPv4 network route.

## -struct-fields

### -field dwForwardDest

Type: <b>DWORD</b>

The destination IPv4 address of the route. An
                entry  with  a IPv4 address of 0.0.0.0 is considered a
                default route.
This member cannot be set to a multicast (class D) IPv4 address.

### -field dwForwardMask

Type: <b>DWORD</b>

The IPv4 subnet mask to use with the
                destination  IPv4 address  before  being compared to
                the value  in  the  <b>dwForwardDest</b>  member. 

The <b>dwForwardMask</b> value should be applied to the destination  IPv4 address (logical and operation) before a comparison with the  value  in  the  <b>dwForwardDest</b> member.

### -field dwForwardPolicy

Type: <b>DWORD</b>

The set of conditions that would cause the selection of a multi-path route (the set of
                next hops for a given destination). This member is typically in IP TOS format. This encoding of this member is described in 
RFC 1354. For more information, see 
<a href="https://www.ietf.org/rfc/rfc1354.txt">http://www.ietf.org/rfc/rfc1354.txt</a>.

### -field dwForwardNextHop

Type: <b>DWORD</b>

For remote routes, the IPv4 address of the next system en route. Otherwise, this member should be an IPv4 address of 0.0.0.0.

### -field dwForwardIfIndex

Type: <b>DWORD</b>

The index of the local interface through  which  the next hop of this
                route should be reached.

### -field dwForwardType

Type: <b>DWORD</b>

The route type as described in 
RFC 1354. For more information, see <a href="https://www.ietf.org/rfc/rfc1354.txt">http://www.ietf.org/rfc/rfc1354.txt</a>.

This member can be one of the values defined in the <i>Iprtmib.h</i> header file. 

On Windows Vista and later, the header files were reorganized and this member can be one of the values from  the <b>MIB_IPFORWARD_TYPE</b> enumeration type defined in the <i>Ipmib.h</i> header file. Note that the <i>Ipmib.h</i> header is automatically included by the <i>Iprtrmib.h</i> header file which is automatically included by the <i>Iphlpapi.h</i> header. The  <i>Iprtrmib.h</i> and  <i>Ipmib.h</i> header files should never be used directly.  

The following list shows the possible values for this member. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MIB_IPROUTE_TYPE_OTHER_"></a><a id="mib_iproute_type_other_"></a><dl>
<dt><b>MIB_IPROUTE_TYPE_OTHER </b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Some other type not specified in RFC 1354.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IPROUTE_TYPE_INVALID"></a><a id="mib_iproute_type_invalid"></a><dl>
<dt><b>MIB_IPROUTE_TYPE_INVALID</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
An invalid route.  This value can result from a route added by an ICMP redirect.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IPROUTE_TYPE_DIRECT"></a><a id="mib_iproute_type_direct"></a><dl>
<dt><b>MIB_IPROUTE_TYPE_DIRECT</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
A local route where the next hop is the final destination (a local interface).

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IPROUTE_TYPE_INDIRECT"></a><a id="mib_iproute_type_indirect"></a><dl>
<dt><b>MIB_IPROUTE_TYPE_INDIRECT</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The remote route where the next hop is not the final destination (a remote destination).

</td>
</tr>
</table>

### -field ForwardType

### -field dwForwardProto

Type: <b>DWORD</b>

The protocol or routing mechanism that generated the route as described in 
RFC 1354. For more information, see <a href="https://www.ietf.org/rfc/rfc1354.txt">http://www.ietf.org/rfc/rfc1354.txt</a>. See 
<a href="/windows/desktop/RRAS/protocol-identifiers">Protocol Identifiers</a> for a list of possible protocol identifiers used by routing protocols.  

This member can be one of the values defined in the <i>Iprtmib.h</i> header file. The values for this member can be one of the  MIB_IPPROTO_xxx values defined in  the <i>Iprtmib.h</i> header file or one of the PROTO_IP_xxx values defined in the <i>routprot.h</i> header file since these values are the same. 

On Windows Vista and later, the header files were reorganized and this member can be one of the values defined in the <i>Nldef.h</i> header file. Note that the <i>Nldef.h</i> header is automatically included by the <i>Ipmib.h</i> header file which is automatically included by the <i>Iprtrmib.h</i> header. The <i>Iphlpapi.h</i> header  automatically includes the <i>Iprtrmib.h</i> header file. The  <i>Iprtrmib.h</i>, <i>Ipmib.h</i>, and <i>Nldef.h</i> header files should never be used directly.  

The following list shows the possible values for this member. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MIB_IPPROTO_OTHER_"></a><a id="mib_ipproto_other_"></a><dl>
<dt><b>MIB_IPPROTO_OTHER </b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Some other protocol not specified in RFC 1354.

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
A static route. This value is used to identify route information for IP  routing set through network management such as the Dynamic Host Configuration Protocol (DCHP), the Simple Network Management Protocol (SNMP), or by calls to the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createipforwardentry">CreateIpForwardEntry</a>,  <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deleteipforwardentry">DeleteIpForwardEntry</a>, or <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setipforwardentry">SetIpForwardEntry</a> functions.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IPPROTO_ICMP"></a><a id="mib_ipproto_icmp"></a><dl>
<dt><b>MIB_IPPROTO_ICMP</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The result of ICMP redirect.

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

### -field ForwardProto

### -field dwForwardAge

Type: <b>DWORD</b>

The number of seconds  since  the  route  was
                added or modified in the network routing table.

### -field dwForwardNextHopAS

Type: <b>DWORD</b>

The autonomous system number of the next hop. When  this  member is  unknown  or not relevant to the
                protocol or routing mechanism specified in <b>dwForwardProto</b>, this value  should be set to zero. This value is documented in 
RFC 1354. For more information, see <a href="https://www.ietf.org/rfc/rfc1354.txt">http://www.ietf.org/rfc/rfc1354.txt</a>

### -field dwForwardMetric1

Type: <b>DWORD</b>

The primary routing metric value for this route. The  semantics of this metric are determined by
                the routing protocol specified in  the  <b>dwForwardProto</b>  member. If  this metric is not
                used, its value should be set to -1. This value is documented in 
in 
RFC 1354. For more information, see <a href="https://www.ietf.org/rfc/rfc1354.txt">http://www.ietf.org/rfc/rfc1354.txt</a>

### -field dwForwardMetric2

Type: <b>DWORD</b>

An alternate  routing metric value for this route. The  semantics of this metric are determined by
                the routing protocol specified in  the  <b>dwForwardProto</b>  member. If  this metric is not
                used, its value should be set to -1. This value is documented in 
RFC 1354. For more information, see <a href="https://www.ietf.org/rfc/rfc1354.txt">http://www.ietf.org/rfc/rfc1354.txt</a>

### -field dwForwardMetric3

Type: <b>DWORD</b>

An alternate  routing metric value for this route. The  semantics of this metric are determined by
                the routing protocol specified in  the  <b>dwForwardProto</b>  member. If  this metric is not
                used, its value should be set to -1. This value is documented in 
RFC 1354. For more information, see <a href="https://www.ietf.org/rfc/rfc1354.txt">http://www.ietf.org/rfc/rfc1354.txt</a>

### -field dwForwardMetric4

Type: <b>DWORD</b>

An alternate  routing metric value for this route. The  semantics of this metric are determined by
                the routing protocol specified in  the  <b>dwForwardProto</b>  member. If  this metric is not
                used, its value should be set to -1. This value is documented in 
RFC 1354. For more information, see <a href="https://www.ietf.org/rfc/rfc1354.txt">http://www.ietf.org/rfc/rfc1354.txt</a>

### -field dwForwardMetric5

Type: <b>DWORD</b>

An alternate  routing metric value for this route. The  semantics of this metric are determined by
                the routing protocol specified in  the  <b>dwForwardProto</b>  member. If  this metric is not
                used, its value should be set to -1. This value is documented in 
RFC 1354. For more information, see <a href="https://www.ietf.org/rfc/rfc1354.txt">http://www.ietf.org/rfc/rfc1354.txt</a>

## -remarks

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipforwardtable">GetIpForwardTable</a> function enumerates the IPv4 route entries on a local system and returns this information in a <a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipforwardtable">MIB_IPFORWARDTABLE</a> structure that contains an array of <b>MIB_IPFORWARDROW</b> structure entries. 



The  <b>dwForwardDest</b>, <b>dwForwardMask</b>, and <b>dwForwardNextHop</b> members of the 
<b>MIB_IPFORWARDROW</b> structure represent  IPv4 addresses in network byte order. 

The  <b>dwForwardProto</b> member of the 
<b>MIB_IPFORWARDROW</b> structure specifies the protocol or routing mechanism that generated the route. Routing protocol identifiers are used to identify route information for the specified routing protocol. For example, <b>MIB_IPPROTO_NETMGMT</b> is used to identify route information for IP  routing set through network management such as the Dynamic Host Configuration Protocol (DCHP), the Simple Network Management Protocol (SNMP), or by calls to the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createipforwardentry">CreateIpForwardEntry</a>,  <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deleteipforwardentry">DeleteIpForwardEntry</a> 
		, or <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setipforwardentry">SetIpForwardEntry</a> functions. See 
<a href="/windows/desktop/RRAS/protocol-identifiers">Protocol Identifiers</a> for a list of possible protocols and routing mechanisms.

An IPv4 address of 0.0.0.0 in the  <b>dwForwardDest</b> member of the 
<b>MIB_IPFORWARDROW</b> structure is considered a
                default route. The <a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipforwardtable">MIB_IPFORWARDTABLE</a> may contain multiple <b>MIB_IPFORWARDROW</b> entries with the <b>dwForwardDest</b> member set to 0.0.0.0 when there are multiple network adapters installed.

When <b>dwForwardAge</b> is set to <b>INFINITE</b>, the route will not be removed based on a timeout
 
value. Any other value for <b>dwForwardAge</b> specifies the number of seconds since the route was added or modified in the network routing table.



On Windows Server 2003 or
  Windows 2000 Server when the Routing and Remote Access Service (RRAS) is running, the  <b>MIB_IPFORWARDROW</b> entries returned have the <b>dwForwardType</b> and <b>dwForwardAge</b> members set to zero. 

On Windows Vista and Windows Server 2008, the route metric specified in the <b>dwForwardMetric1</b> member of the  <b>MIB_IPFORWARDROW</b> structure represents a combination of the route metric added to the interface metric specified in the <b>Metric</b> member of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipinterface_row">MIB_IPINTERFACE_ROW</a> structure of the associated interface.  So the <b>dwForwardMetric1</b> member of the  <b>MIB_IPFORWARDROW</b> structure should be equal to or greater than <b>Metric</b> member of the associated <b>MIB_IPINTERFACE_ROW</b> structure. If an application would like to set the route metric to 0, then the <b>dwForwardMetric1</b> member of the <b>MIB_IPFORWARDROW</b> structure  should be set equal to the value of the interface metric specified in the <b>Metric</b> member of the associated <b>MIB_IPINTERFACE_ROW</b> structure. An application can retrieve the interface metric by calling the <a href="/windows/desktop/api/netioapi/nf-netioapi-getipinterfaceentry">GetIpInterfaceEntry</a> function.

A number of members of the <b>MIB_IPFORWARDROW</b> structure  are not currently used by IPv4 routing. These members include <b>dwForwardPolicy</b>, <b>dwForwardNextHopAS</b>, <b>dwForwardMetric2</b>, <b>dwForwardMetric3</b>, <b>dwForwardMetric4</b>, and <b>dwForwardMetric5</b>. 

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed. This  structure is defined in the <i>Ipmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.


#### Examples

To view an example that retrieves the <a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipforwardtable">MIB_IPFORWARDTABLE</a> structure and then prints out the <b>MIB_IPFORWARDROW</b> structure entries in this table, see the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipforwardtable">GetIpForwardTable</a> function.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createipforwardentry">CreateIpForwardEntry</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deleteipforwardentry">DeleteIpForwardEntry</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipforwardtable">GetIpForwardTable</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getipinterfaceentry">GetIpInterfaceEntry</a>



<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipforwardtable">MIB_IPFORWARDTABLE</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipinterface_row">MIB_IPINTERFACE_ROW</a>



<a href="/windows/desktop/RRAS/protocol-identifiers">Protocol Identifiers</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setipforwardentry">SetIpForwardEntry</a>