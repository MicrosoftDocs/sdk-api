---
UID: NS:netioapi._MIB_IPINTERFACE_ROW
title: MIB_IPINTERFACE_ROW (netioapi.h)
description: Stores interface management information for a particular IP address family on a network interface.
helpviewer_keywords: ["*PMIB_IPINTERFACE_ROW","AF_INET","AF_INET6","AF_UNSPEC","LinkLocalAlwaysOff","LinkLocalAlwaysOn","LinkLocalDelayed","LinkLocalUnchanged","MIB_IPINTERFACE_ROW","MIB_IPINTERFACE_ROW structure [MIB]","PMIB_IPINTERFACE_ROW","PMIB_IPINTERFACE_ROW structure pointer [MIB]","RouterDiscoveryDhcp","RouterDiscoveryDisabled","RouterDiscoveryEnabled","RouterDiscoveryUnchanged","_MIB_IPINTERFACE_ROW","mib.mib_ipinterface_row","netioapi/MIB_IPINTERFACE_ROW","netioapi/PMIB_IPINTERFACE_ROW"]
old-location: mib\mib_ipinterface_row.htm
tech.root: MIB
ms.assetid: 28265037-f7a3-40a4-b386-20f43f32a8b3
ms.date: 12/05/2018
ms.keywords: '*PMIB_IPINTERFACE_ROW, AF_INET, AF_INET6, AF_UNSPEC, LinkLocalAlwaysOff, LinkLocalAlwaysOn, LinkLocalDelayed, LinkLocalUnchanged, MIB_IPINTERFACE_ROW, MIB_IPINTERFACE_ROW structure [MIB], PMIB_IPINTERFACE_ROW, PMIB_IPINTERFACE_ROW structure pointer [MIB], RouterDiscoveryDhcp, RouterDiscoveryDisabled, RouterDiscoveryEnabled, RouterDiscoveryUnchanged, _MIB_IPINTERFACE_ROW, mib.mib_ipinterface_row, netioapi/MIB_IPINTERFACE_ROW, netioapi/PMIB_IPINTERFACE_ROW'
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
req.typenames: MIB_IPINTERFACE_ROW, *PMIB_IPINTERFACE_ROW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_IPINTERFACE_ROW
 - netioapi/_MIB_IPINTERFACE_ROW
 - PMIB_IPINTERFACE_ROW
 - netioapi/PMIB_IPINTERFACE_ROW
 - MIB_IPINTERFACE_ROW
 - netioapi/MIB_IPINTERFACE_ROW
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
 - MIB_IPINTERFACE_ROW
---

# MIB_IPINTERFACE_ROW structure


## -description

The 
<b>MIB_IPINTERFACE_ROW</b> structure stores interface management information for a particular IP address family on a network interface.

## -struct-fields

### -field Family

Type: <b>ADDRESS_FAMILY</b>

The address family. Possible values for the address family are listed in the <i>Winsock2.h</i> header file. Note that the values for the AF_ address family and PF_ protocol family constants  are identical (for example, <b>AF_INET</b> and <b>PF_INET</b>), so either constant can be used.

On Windows Vista and later as well as on the Windows SDK, the organization of header files has changed and possible values for this member are defined in the <i>Ws2def.h</i> header file. Note that the <i>Ws2def.h</i> header file is automatically included in <i>Winsock2.h</i>, and should never be used directly.

The values currently supported are <b>AF_INET</b> or <b>AF_INET6</b>, which are the Internet
                     address family formats for IPv4 and IPv6. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AF_UNSPEC"></a><a id="af_unspec"></a><dl>
<dt><b>AF_UNSPEC</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The address family is unspecified.

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET"></a><a id="af_inet"></a><dl>
<dt><b>AF_INET</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The Internet Protocol version 4 (IPv4) address family.

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET6"></a><a id="af_inet6"></a><dl>
<dt><b>AF_INET6</b></dt>
<dt>23</dt>
</dl>
</td>
<td width="60%">
The Internet Protocol version 6 (IPv6) address family.

</td>
</tr>
</table>

### -field InterfaceLuid

Type: <b><a href="/windows/desktop/api/ifdef/ns-ifdef-net_luid_lh">NET_LUID</a></b>

The locally unique identifier (LUID) for the network interface.

### -field InterfaceIndex

Type: <b>NET_IFINDEX</b>

The local index value for the network interface. This index value may change when a network adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.

### -field MaxReassemblySize

Type: <b>ULONG</b>

The maximum reassembly size, in bytes, of a fragmented IP packet. This member is currently set to zero and reserved for future use.

### -field InterfaceIdentifier

Type: <b>ULONG64</b>

Reserved for future use. This member is currently set to zero.

### -field MinRouterAdvertisementInterval

Type: <b>ULONG</b>

The minimum router advertisement interval, in milliseconds, on this IP interface. This member defaults to 200 for IPv6. This member is only applicable if the <b>AdvertisingEnabled</b> member is set to <b>TRUE</b>.

### -field MaxRouterAdvertisementInterval

Type: <b>ULONG</b>

The maximum router advertisement interval, in milliseconds, on this IP interface. This member defaults  to 600 for IPv6. This member is only applicable if the <b>AdvertisingEnabled</b> member is set to <b>TRUE</b>.

### -field AdvertisingEnabled

Type: <b>BOOLEAN</b>

A value that indicates if router advertising is enabled on this IP interface. The default for IPv6 is that  router advertisement is enabled only if the interface is configured to act as a router.  The default for IPv4 is that router advertisement is disabled.

### -field ForwardingEnabled

Type: <b>BOOLEAN</b>

A value that indicates if IP forwarding is enabled on this IP interface.

### -field WeakHostSend

Type: <b>BOOLEAN</b>

A value that indicates if weak host send mode is enabled  on this IP interface.

### -field WeakHostReceive

Type: <b>BOOLEAN</b>

A value that indicates if weak host receive mode is enabled  on this IP interface.

### -field UseAutomaticMetric

Type: <b>BOOLEAN</b>

A value that indicates if the IP interface uses automatic metric.

### -field UseNeighborUnreachabilityDetection

Type: <b>BOOLEAN</b>

A value that indicates if neighbor unreachability detection is enabled on this IP interface.

### -field ManagedAddressConfigurationSupported

Type: <b>BOOLEAN</b>

A value that indicates if the IP interface supports managed address configuration using DHCP.

### -field OtherStatefulConfigurationSupported

Type: <b>BOOLEAN</b>

A value that indicates if the IP interface supports other stateful configuration (route configuration, for example).

### -field AdvertiseDefaultRoute

Type: <b>BOOLEAN</b>

A value that indicates if the IP interface advertises the default route. This member is only applicable if the <b>AdvertisingEnabled</b> member is set to <b>TRUE</b>.

### -field RouterDiscoveryBehavior

Type: <b>NL_ROUTER_DISCOVERY_BEHAVIOR</b>

The router discovery behavior. This member can be one of the values from the <b>NL_ROUTER_DISCOVERY_BEHAVIOR</b> enumeration type defined in the <i>Nldef.h</i> header file. The member is described in RFC 2461. For more information, see <a href="https://www.ietf.org/rfc/rfc2461.txt">http://www.ietf.org/rfc/rfc2461.txt</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RouterDiscoveryDisabled"></a><a id="routerdiscoverydisabled"></a><a id="ROUTERDISCOVERYDISABLED"></a><dl>
<dt><b>RouterDiscoveryDisabled</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Router discovery is disabled. 

</td>
</tr>
<tr>
<td width="40%"><a id="RouterDiscoveryEnabled"></a><a id="routerdiscoveryenabled"></a><a id="ROUTERDISCOVERYENABLED"></a><dl>
<dt><b>RouterDiscoveryEnabled</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Router discovery is enabled. This is the default value for IPv6.

</td>
</tr>
<tr>
<td width="40%"><a id="RouterDiscoveryDhcp"></a><a id="routerdiscoverydhcp"></a><a id="ROUTERDISCOVERYDHCP"></a><dl>
<dt><b>RouterDiscoveryDhcp</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Router discovery is configured based on DHCP. This is the default value for IPv4.

</td>
</tr>
<tr>
<td width="40%"><a id="RouterDiscoveryUnchanged_"></a><a id="routerdiscoveryunchanged_"></a><a id="ROUTERDISCOVERYUNCHANGED_"></a><dl>
<dt><b>RouterDiscoveryUnchanged </b></dt>
<dt>-1</dt>
</dl>
</td>
<td width="60%">
This value is used when setting the properties for an IP interface when the value for router discovery should be unchanged.

</td>
</tr>
</table>

### -field DadTransmits

Type: <b>ULONG</b>

The number of consecutive messages sent while performing duplicate address
                     detection on a tentative IP unicast address. A value of zero
                     indicates that duplicate address detection is not
                     performed on tentative IP addresses. A value of one
                     indicates a single transmission with no follow up
                     retransmissions. For IPv4, the default for this member is 3. For IPv6, the default for this member is 1. For IPv6, these messages will sent as neighbor solicitation requests.
                     This member is defined as DupAddrDetectTransmits in RFC 2462. For more information, see <a href="https://www.ietf.org/rfc/rfc2462.txt">http://www.ietf.org/rfc/rfc2462.txt</a>.

### -field BaseReachableTime

Type: <b>ULONG</b>

The base for random reachable time,  in milliseconds. The member is described in RFC 2461. For more information, see <a href="https://www.ietf.org/rfc/rfc2461.txt">http://www.ietf.org/rfc/rfc2461.txt</a>.

### -field RetransmitTime

Type: <b>ULONG</b>

The neighbor solicitation timeout,  in milliseconds. The member is described in RFC 2461. For more information, see <a href="https://www.ietf.org/rfc/rfc2461.txt">http://www.ietf.org/rfc/rfc2461.txt</a>.

### -field PathMtuDiscoveryTimeout

Type: <b>ULONG</b>

The path MTU discovery timeout,  in milliseconds.

### -field LinkLocalAddressBehavior

Type: <b>NL_LINK_LOCAL_ADDRESS_BEHAVIOR</b>

The link local address behavior. This member can be one of the values from the <b>NL_LINK_LOCAL_ADDRESS_BEHAVIOR</b> enumeration type defined in the <i>Nldef.h</i> header file.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LinkLocalAlwaysOff"></a><a id="linklocalalwaysoff"></a><a id="LINKLOCALALWAYSOFF"></a><dl>
<dt><b>LinkLocalAlwaysOff</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Never use a link local IP address.

</td>
</tr>
<tr>
<td width="40%"><a id="LinkLocalDelayed"></a><a id="linklocaldelayed"></a><a id="LINKLOCALDELAYED"></a><dl>
<dt><b>LinkLocalDelayed</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Use a link local IP address only if no other address is available. This is the default setting for an IPv4 interface.

</td>
</tr>
<tr>
<td width="40%"><a id="LinkLocalAlwaysOn"></a><a id="linklocalalwayson"></a><a id="LINKLOCALALWAYSON"></a><dl>
<dt><b>LinkLocalAlwaysOn</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Always use a link local IP address. This is the default setting for an IPv6 interface. 


</td>
</tr>
<tr>
<td width="40%"><a id="LinkLocalUnchanged"></a><a id="linklocalunchanged"></a><a id="LINKLOCALUNCHANGED"></a><dl>
<dt><b>LinkLocalUnchanged</b></dt>
<dt>-1</dt>
</dl>
</td>
<td width="60%">
This value is used when setting the properties for an IP interface when the value for link local address behavior should be unchanged.

</td>
</tr>
</table>

### -field LinkLocalAddressTimeout

Type: <b>ULONG</b>

The link local IP address timeout, in milliseconds.

### -field ZoneIndices

Type: <b>ULONG[ScopeLevelCount]</b>

An array that specifies the zone part of scope IDs.

### -field SitePrefixLength

Type: <b>ULONG</b>

The site prefix length, in bits, of the IP interface address. The length, in bits, of the site prefix or network part of the IP interface address. For an IPv4 address, any value greater than 32 is an illegal value. For an IPv6 address, any value greater than 128 is an illegal value. 
A value of 255 is commonly used to represent an illegal value.

### -field Metric

Type: <b>ULONG</b>

The interface metric. Note the actual route metric used to compute the route preference is the summation of the route metric offset specified in the <b>Metric</b> member of the  <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipforward_row2">MIB_IPFORWARD_ROW2</a> structure and the interface metric specified in this member.

### -field NlMtu

Type: <b>ULONG</b>

The network layer MTU size, in bytes.

### -field Connected

Type: <b>BOOLEAN</b>

A value that indicates if the interface is connected to a network access point.

### -field SupportsWakeUpPatterns

Type: <b>BOOLEAN</b>

A value that specifies if the network interface supports Wake on LAN.

### -field SupportsNeighborDiscovery

Type: <b>BOOLEAN</b>

A value that specifies if the IP interface support neighbor discovery.

### -field SupportsRouterDiscovery

Type: <b>BOOLEAN</b>

A value that specifies if the IP interface support router discovery.

### -field ReachableTime

Type: <b>ULONG</b>

The reachable timeout, in milliseconds.

### -field TransmitOffload

Type: <b>NL_INTERFACE_OFFLOAD_ROD</b>

A set of flags that indicate the transmit offload capabilities for the IP interface. The <a href="/windows/desktop/api/nldef/ns-nldef-nl_interface_offload_rod">NL_INTERFACE_OFFLOAD_ROD</a> structure is defined in the <i>Nldef.h</i> header file.

### -field ReceiveOffload

Type: <b>NL_INTERFACE_OFFLOAD_ROD</b>

A set of flags that indicate the receive offload capabilities for the IP interface. The <a href="/windows/desktop/api/nldef/ns-nldef-nl_interface_offload_rod">NL_INTERFACE_OFFLOAD_ROD</a> structure is defined in the <i>Nldef.h</i> header file.

### -field DisableDefaultRoutes

Type: <b>BOOLEAN</b>

A value that indicates if using default route on the interface should be disabled. This member can be used by VPN clients to restrict split tunneling.

## -remarks

The <b>MIB_IPINTERFACE_ROW</b> structure is defined on Windows Vista and later. 

The <b>Family</b>, <b>InterfaceLuid</b>, and <b>InterfaceIndex</b> members uniquely identify a <b>MIB_IPINTERFACE_ROW</b> entry.

When a unicast packet arrives at a host, IP must determine whether the packet is locally destined (its destination matches an address that is assigned to an interface of the host). IP implementations that follow a weak host model accept any locally destined packet, regardless of the interface on which the packet was received. IP implementations that follow the strong host model only accept locally destined packets if the destination address in the packet matches an address assigned to the interface on which the packet was received. The weak host model provides better network connectivity. However, it also makes hosts susceptible to multihome-based network attacks.


The current IPv4 implementation in Windows Server 2003 and Windows XP uses the weak host model. In this case, all unicast packets are sent out the  interface with the lowest metric for a route. 

The TCP/IP stack on Windows Vista and later supports the strong host model for both IPv4 and IPv6 and is configured to use the strong host mode by default (the <b>WeakHostReceive</b> and <b>WeakHostSend</b> members are set to <b>FALSE</b>). With the strong host mode, a unicast packet can be sent out a specific interface that does not have the lowest metric for a route by binding the socket  to the source address of the specific interface. 

The TCP/IP stack on Windows Vista and later can be configured to use a weak host model. 

A metric is a value that is assigned to an IP route for a particular network interface that identifies the cost that is associated with using that route. For example, the metric can be valued in terms of link speed, hop count, or time delay. Automatic metric is a feature on Windows XP and later that automatically configures the metric for the local routes that are based on link speed. The automatic metric feature is enabled by default (the <b>UseAutomaticMetric</b> is set to <b>TRUE</b>) on Windows XP and later. It can also be manually configured to assign a specific metric to an IP route.



The automatic metric feature can be useful when the routing table contains multiple routes for the same destination. For example, a computer with a 10 megabit network interface and a 100 megabit network interface has a default gateway that is configured on both network interfaces. When <b>UseAutomaticMetric</b> is <b>TRUE</b>, this feature can force all of the traffic that is destined for the Internet, for example, to use the fastest network interface that is available.


The interface metric specified in the <b>Metric</b> member represents just the metric for the interface. The complete routing metric is a combination of this interface metric  added to the route metric offset specified in the <b>Metric</b> member of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipforward_row2">MIB_IPFORWARD_ROW2</a> structure of a route entry specified on this interface.  

Unprivileged simultaneous access to multiple networks of different security requirements creates a security hole and allows an unprivileged application to accidentally relay data between the two networks. A typical example is simultaneous access to a virtual private network (VPN) and the internet. Windows Server 2003 and Windows XP use a weak host model, where RAS prevents such simultaneous access by increasing the route metric of all default routes over other interfaces. Thus all traffic is routed through the VPN interface, disrupting other network connectivity. 

On Windows Vista and later, a strong host model is used by default. If a source IP address is specified in the route lookup using <a href="/windows/desktop/api/netioapi/nf-netioapi-getbestroute2">GetBestRoute2</a> or <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getbestroute">GetBestRoute</a>, the route lookup is restricted to the interface of the source IP address. The route metric modification by RAS has no effect as the list of potential routes does not even have the route for the VPN interface thereby allowing traffic to the internet. The <b>DisableDefaultRoutes</b> member of the <b>MIB_IPINTERFACE_ROW</b> structure can be used to disable using the default route on an interface. This member can be used as a security measure by VPN clients to restrict split tunneling when split tunneling is not required by the VPN client. A VPN client can call the <a href="/windows/desktop/api/netioapi/nf-netioapi-setipinterfaceentry">SetIpInterfaceEntry</a> function to set the <b>DisableDefaultRoutes</b> member to <b>TRUE</b> when required. A VPN client can query the current state of the <b>DisableDefaultRoutes</b> member by calling  the <a href="/windows/desktop/api/netioapi/nf-netioapi-getipinterfaceentry">GetIpInterfaceEntry</a> function. 

Note that the <i>Netioapi.h</i> header file is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Netioapi.h</i> header file should never be used directly.


#### Examples

To view an example that retrieves the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipinterface_table">MIB_IPINTERFACE_TABLE</a> structure and then prints out a few members of the <b>MIB_IPINTERFACE_ROW</b> structure entries in this table, see the <a href="/windows/desktop/api/netioapi/nf-netioapi-getipinterfacetable">GetIpInterfaceTable</a> function.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getbestroute">GetBestRoute</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getbestroute2">GetBestRoute2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getipinterfaceentry">GetIpInterfaceEntry</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getipinterfacetable">GetIpInterfaceTable</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipforward_row2">MIB_IPFORWARD_ROW2</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipinterface_table">MIB_IPINTERFACE_TABLE</a>



<a href="/windows/desktop/api/ifdef/ns-ifdef-net_luid_lh">NET_LUID</a>



<a href="/windows/desktop/api/nldef/ns-nldef-nl_interface_offload_rod">NL_INTERFACE_OFFLOAD_ROD</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-setipinterfaceentry">SetIpInterfaceEntry</a>