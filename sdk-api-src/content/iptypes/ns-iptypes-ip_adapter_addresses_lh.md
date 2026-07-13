---
UID: NS:iptypes._IP_ADAPTER_ADDRESSES_LH
title: IP_ADAPTER_ADDRESSES_LH (iptypes.h)
description: The IP_ADAPTER_ADDRESSES_LH structure (iptypes.h) is the header node for a linked list of addresses for a particular adapter.
old-location: iphlp\ip_adapter_addresses.htm
tech.root: IpHlp
ms.assetid: a2df3749-6c75-40c0-8952-1656bbe639a6
ms.date: 08/12/2022
ms.keywords: '*PIP_ADAPTER_ADDRESSES, *PIP_ADAPTER_ADDRESSES_LH, IF_TYPE_ATM, IF_TYPE_ETHERNET_CSMACD, IF_TYPE_IEEE1394, IF_TYPE_IEEE80211, IF_TYPE_ISO88025_TOKENRING, IF_TYPE_OTHER, IF_TYPE_PPP, IF_TYPE_SOFTWARE_LOOPBACK, IF_TYPE_TUNNEL, IP_ADAPTER_ADDRESSES, IP_ADAPTER_ADDRESSES structure [IP Helper], IP_ADAPTER_ADDRESSES_LH, IP_ADAPTER_ADDRESSES_XP, IP_ADAPTER_DDNS_ENABLED, IP_ADAPTER_DHCP_ENABLED, IP_ADAPTER_IPV4_ENABLED, IP_ADAPTER_IPV6_ENABLED, IP_ADAPTER_IPV6_MANAGE_ADDRESS_CONFIG, IP_ADAPTER_IPV6_OTHER_STATEFUL_CONFIG, IP_ADAPTER_NETBIOS_OVER_TCPIP_ENABLED, IP_ADAPTER_NO_MULTICAST, IP_ADAPTER_RECEIVE_ONLY, IP_ADAPTER_REGISTER_ADAPTER_SUFFIX, IfOperStatusDormant, IfOperStatusDown, IfOperStatusLowerLayerDown, IfOperStatusNotPresent, IfOperStatusTesting, IfOperStatusUnknown, IfOperStatusUp, NET_IF_CONNECTION_DEDICATED, NET_IF_CONNECTION_DEMAND, NET_IF_CONNECTION_MAXIMUM, NET_IF_CONNECTION_PASSIVE, PIP_ADAPTER_ADDRESSES, PIP_ADAPTER_ADDRESSES structure pointer [IP Helper], TUNNEL_TYPE_6TO4, TUNNEL_TYPE_DIRECT, TUNNEL_TYPE_IPHTTPS, TUNNEL_TYPE_ISATAP, TUNNEL_TYPE_NONE, TUNNEL_TYPE_OTHER, TUNNEL_TYPE_TEREDO, _iphlp_ip_adapter_addresses, iphlp.ip_adapter_addresses, iptypes/IP_ADAPTER_ADDRESSES, iptypes/PIP_ADAPTER_ADDRESSES'
req.header: iptypes.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: IP_ADAPTER_ADDRESSES_LH, *PIP_ADAPTER_ADDRESSES_LH
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IP_ADAPTER_ADDRESSES_LH
 - iptypes/_IP_ADAPTER_ADDRESSES_LH
 - PIP_ADAPTER_ADDRESSES_LH
 - iptypes/PIP_ADAPTER_ADDRESSES_LH
 - IP_ADAPTER_ADDRESSES_LH
 - iptypes/IP_ADAPTER_ADDRESSES_LH
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iptypes.h
api_name:
 - IP_ADAPTER_ADDRESSES
---

# IP_ADAPTER_ADDRESSES_LH structure


## -description

The <b>IP_ADAPTER_ADDRESSES</b> structure is the 
   <i>header node</i> for a linked list of addresses for a particular adapter. This structure can simultaneously 
   be used as part of a linked list of 
   <b>IP_ADAPTER_ADDRESSES</b> structures.

## -struct-fields

### -field Alignment

Type: <b>ULONGLONG</b>

Reserved. Used by the compiler to align the structure.

### -field Length

Type: <b>ULONG</b>

The length, in bytes, of this structure. Note that the length of the 
        <b>IP_ADAPTER_ADDRESSES</b> structure changed on 
        Windows XP with SP1 and later and also on Windows Vista and later.

### -field IfIndex

Type: <b>DWORD</b>

The index of the IPv4 interface with which these addresses are associated. On Windows Server 2003 and Windows XP, this member is zero if IPv4 is 
        not available on the interface.

### -field Next

Type: <b>struct _IP_ADAPTER_ADDRESSES*</b>

A pointer to the next adapter addresses structure in the list.

### -field AdapterName

Type: <b>PCHAR</b>

An array of characters that contains the name of the adapter with which these addresses are associated. 
      Unlike an adapter's friendly name, the adapter name specified in <b>AdapterName</b> is 
      permanent and cannot be modified by the user.

### -field FirstUnicastAddress

Type: <b>PIP_ADAPTER_UNICAST_ADDRESS</b>

A pointer to the first 
      <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh">IP_ADAPTER_UNICAST_ADDRESS</a> structure in a 
      linked list of IP unicast addresses for the adapter.

### -field FirstAnycastAddress

Type: <b>PIP_ADAPTER_ANYCAST_ADDRESS</b>

A pointer to the first 
      <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_anycast_address_xp">IP_ADAPTER_ANYCAST_ADDRESS</a> structure in a 
      linked list of IP anycast addresses for the adapter.

### -field FirstMulticastAddress

Type: <b>PIP_ADAPTER_MULTICAST_ADDRESS</b>

A pointer to the first 
      <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_multicast_address_xp">IP_ADAPTER_MULTICAST_ADDRESS</a> structure 
      in a list of IP multicast addresses for the adapter.

### -field FirstDnsServerAddress

Type: <b>PIP_ADAPTER_DNS_SERVER_ADDRESS</b>

A pointer to the first 
      <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_dns_server_address_xp">IP_ADAPTER_DNS_SERVER_ADDRESS</a> structure 
      in a linked list of DNS server addresses for the adapter.

### -field DnsSuffix

Type: <b>PWCHAR</b>

The Domain Name System (DNS) suffix associated with this adapter.

### -field Description

Type: <b>PWCHAR</b>

A description for the adapter. This member is read-only.

### -field FriendlyName

Type: <b>PWCHAR</b>

A user-friendly name for the adapter. For example: "Local Area Connection 1." This name appears in contexts 
      such as the <b>ipconfig</b> command line program and the Connection folder. This member is read 
      only and can't be modified using any IP Helper functions.
      

This member is the ifAlias field used by NDIS as described in 
       <a href="https://www.ietf.org/rfc/rfc2863.txt">RFC 2863</a>. The ifAlias field can be set by an 
       NDIS interface provider when the NDIS driver is installed. For NDIS miniport drivers, this field is set by 
       NDIS.

### -field PhysicalAddress

Type: <b>BYTE[MAX_ADAPTER_ADDRESS_LENGTH]</b>

The Media Access Control (MAC) address for the adapter. For example, on an Ethernet network this member 
      would specify the Ethernet hardware address.

### -field PhysicalAddressLength

Type: <b>DWORD</b>

The length, in bytes, of the address specified in the <b>PhysicalAddress</b> member. 
      For interfaces that do not have a data-link layer, this value is zero.

### -field Flags

Type: <b>DWORD</b>

A set of flags specifying various settings for the adapter. These values are defined in the 
      <i>Iptypes.h</i> header file. Combinations of these flag bits are possible.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IP_ADAPTER_DDNS_ENABLED"></a><a id="ip_adapter_ddns_enabled"></a><dl>
<dt><b>IP_ADAPTER_DDNS_ENABLED</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Dynamic DNS is enabled on this adapter.

</td>
</tr>
<tr>
<td width="40%"><a id="IP_ADAPTER_REGISTER_ADAPTER_SUFFIX"></a><a id="ip_adapter_register_adapter_suffix"></a><dl>
<dt><b>IP_ADAPTER_REGISTER_ADAPTER_SUFFIX</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Register the DNS suffix for this adapter.

</td>
</tr>
<tr>
<td width="40%"><a id="IP_ADAPTER_DHCP_ENABLED"></a><a id="ip_adapter_dhcp_enabled"></a><dl>
<dt><b>IP_ADAPTER_DHCP_ENABLED</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
The Dynamic Host Configuration Protocol (DHCP) is enabled on this adapter.

</td>
</tr>
<tr>
<td width="40%"><a id="IP_ADAPTER_RECEIVE_ONLY"></a><a id="ip_adapter_receive_only"></a><dl>
<dt><b>IP_ADAPTER_RECEIVE_ONLY</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
The adapter is a receive-only adapter.

</td>
</tr>
<tr>
<td width="40%"><a id="IP_ADAPTER_NO_MULTICAST"></a><a id="ip_adapter_no_multicast"></a><dl>
<dt><b>IP_ADAPTER_NO_MULTICAST</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
The adapter is not a multicast recipient.

</td>
</tr>
<tr>
<td width="40%"><a id="IP_ADAPTER_IPV6_OTHER_STATEFUL_CONFIG"></a><a id="ip_adapter_ipv6_other_stateful_config"></a><dl>
<dt><b>IP_ADAPTER_IPV6_OTHER_STATEFUL_CONFIG</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
The adapter contains other IPv6-specific stateful configuration information. 

</td>
</tr>
<tr>
<td width="40%"><a id="IP_ADAPTER_NETBIOS_OVER_TCPIP_ENABLED"></a><a id="ip_adapter_netbios_over_tcpip_enabled"></a><dl>
<dt><b>IP_ADAPTER_NETBIOS_OVER_TCPIP_ENABLED</b></dt>
<dt>0x0040</dt>
</dl>
</td>
<td width="60%">
The adapter is enabled for NetBIOS over TCP/IP.
        

<div class="alert"><b>Note</b>  This flag is only supported on Windows Vista and later when the application has been 
         compiled for a target platform with an NTDDI version equal or greater than 
         <b>NTDDI_LONGHORN</b>. This flag is defined in the 
         <b>IP_ADAPTER_ADDRESSES_LH</b> structure as the  
         <b>NetbiosOverTcpipEnabled</b> bitfield.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="IP_ADAPTER_IPV4_ENABLED"></a><a id="ip_adapter_ipv4_enabled"></a><dl>
<dt><b>IP_ADAPTER_IPV4_ENABLED</b></dt>
<dt>0x0080</dt>
</dl>
</td>
<td width="60%">
The adapter is enabled for IPv4.
        

<div class="alert"><b>Note</b>  This flag is only supported on Windows Vista and later when the application has been 
         compiled for a target platform with an NTDDI version equal or greater than 
         <b>NTDDI_LONGHORN</b>. This flag is defined in the 
         <b>IP_ADAPTER_ADDRESSES_LH</b> structure as the <b>Ipv4Enabled</b> 
         bitfield.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="IP_ADAPTER_IPV6_ENABLED"></a><a id="ip_adapter_ipv6_enabled"></a><dl>
<dt><b>IP_ADAPTER_IPV6_ENABLED</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
The adapter is enabled for IPv6.
        

<div class="alert"><b>Note</b>  This flag is only supported on Windows Vista and later when the application has been 
         compiled for a target platform with an NTDDI version equal or greater than 
         <b>NTDDI_LONGHORN</b>. This flag is defined in the 
         <b>IP_ADAPTER_ADDRESSES_LH</b> structure as the 
         <b>Ipv6Enabled</b> bitfield.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="IP_ADAPTER_IPV6_MANAGE_ADDRESS_CONFIG"></a><a id="ip_adapter_ipv6_manage_address_config"></a><dl>
<dt><b>IP_ADAPTER_IPV6_MANAGE_ADDRESS_CONFIG</b></dt>
<dt>0x0200</dt>
</dl>
</td>
<td width="60%">
The adapter is enabled for IPv6 managed address configuration.
        

<div class="alert"><b>Note</b>  This flag is only supported on Windows Vista and later when the application has been 
         compiled for a target platform with an NTDDI version equal or greater than 
         <b>NTDDI_LONGHORN</b>. This flag is defined in the 
         <b>IP_ADAPTER_ADDRESSES_LH</b> structure as the 
         <b>Ipv6ManagedAddressConfigurationSupported</b> bitfield.</div>
<div> </div>
</td>
</tr>
</table>

### -field DdnsEnabled

### -field RegisterAdapterSuffix

### -field Dhcpv4Enabled

### -field ReceiveOnly

### -field NoMulticast

### -field Ipv6OtherStatefulConfig

### -field NetbiosOverTcpipEnabled

### -field Ipv4Enabled

### -field Ipv6Enabled

### -field Ipv6ManagedAddressConfigurationSupported

### -field Mtu

Type: <b>DWORD</b>

The maximum transmission unit (MTU) size, in bytes.

### -field IfType

Type: <b>DWORD</b>

The interface type as defined by the Internet Assigned Names Authority (IANA). Possible values for the 
      interface type are listed in the <i>Ipifcons.h</i> header file.
      

The table below lists common values for the interface type although many other values are possible. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IF_TYPE_OTHER"></a><a id="if_type_other"></a><dl>
<dt><b>IF_TYPE_OTHER</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Some other type of network interface.

</td>
</tr>
<tr>
<td width="40%"><a id="IF_TYPE_ETHERNET_CSMACD"></a><a id="if_type_ethernet_csmacd"></a><dl>
<dt><b>IF_TYPE_ETHERNET_CSMACD</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
An Ethernet network interface.

</td>
</tr>
<tr>
<td width="40%"><a id="IF_TYPE_ISO88025_TOKENRING"></a><a id="if_type_iso88025_tokenring"></a><dl>
<dt><b>IF_TYPE_ISO88025_TOKENRING</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
A token ring network interface.

</td>
</tr>
<tr>
<td width="40%"><a id="IF_TYPE_PPP"></a><a id="if_type_ppp"></a><dl>
<dt><b>IF_TYPE_PPP</b></dt>
<dt>23</dt>
</dl>
</td>
<td width="60%">
A PPP network interface.

</td>
</tr>
<tr>
<td width="40%"><a id="IF_TYPE_SOFTWARE_LOOPBACK"></a><a id="if_type_software_loopback"></a><dl>
<dt><b>IF_TYPE_SOFTWARE_LOOPBACK</b></dt>
<dt>24</dt>
</dl>
</td>
<td width="60%">
A software loopback network interface.

</td>
</tr>
<tr>
<td width="40%"><a id="IF_TYPE_ATM"></a><a id="if_type_atm"></a><dl>
<dt><b>IF_TYPE_ATM</b></dt>
<dt>37</dt>
</dl>
</td>
<td width="60%">
An ATM network interface.

</td>
</tr>
<tr>
<td width="40%"><a id="IF_TYPE_IEEE80211"></a><a id="if_type_ieee80211"></a><dl>
<dt><b>IF_TYPE_IEEE80211</b></dt>
<dt>71</dt>
</dl>
</td>
<td width="60%">
An IEEE 802.11 wireless network interface. 

On Windows Vista and later, wireless network 
        cards are reported as <b>IF_TYPE_IEEE80211</b>. On earlier versions of  Windows, wireless 
        network cards are reported as <b>IF_TYPE_ETHERNET_CSMACD</b>. 

On Windows XP with SP3 and on Windows XP with SP2 x86 with the Wireless LAN API for Windows XP with SP2 installed, the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces">WlanEnumInterfaces</a> function can be used to enumerate wireless interfaces on the local computer. 

</td>
</tr>
<tr>
<td width="40%"><a id="IF_TYPE_TUNNEL"></a><a id="if_type_tunnel"></a><dl>
<dt><b>IF_TYPE_TUNNEL</b></dt>
<dt>131</dt>
</dl>
</td>
<td width="60%">
A tunnel type encapsulation network interface.

</td>
</tr>
<tr>
<td width="40%"><a id="IF_TYPE_IEEE1394"></a><a id="if_type_ieee1394"></a><dl>
<dt><b>IF_TYPE_IEEE1394</b></dt>
<dt>144</dt>
</dl>
</td>
<td width="60%">
An IEEE 1394 (Firewire) high performance serial bus network interface.

</td>
</tr>
</table>

### -field OperStatus

Type: <b>IF_OPER_STATUS</b>

The operational status for the interface as defined in RFC 2863.  For more information, see 
      <a href="https://www.ietf.org/rfc/rfc2863.txt">http://www.ietf.org/rfc/rfc2863.txt</a>. This 
      member can be one of the values from the <b>IF_OPER_STATUS</b> enumeration type defined in 
      the <i>Iftypes.h</i> header file. On Windows Vista and later, the header files 
      were reorganized and this enumeration is defined in the <i>Ifdef.h</i> header file.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IfOperStatusUp"></a><a id="ifoperstatusup"></a><a id="IFOPERSTATUSUP"></a><dl>
<dt><b>IfOperStatusUp</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The interface is up and able to pass packets.

</td>
</tr>
<tr>
<td width="40%"><a id="IfOperStatusDown"></a><a id="ifoperstatusdown"></a><a id="IFOPERSTATUSDOWN"></a><dl>
<dt><b>IfOperStatusDown</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The interface is down and not in a condition to pass packets. The 
        <b>IfOperStatusDown</b> state has two meanings, depending on the value of 
        <b>AdminStatus</b> member. If <b>AdminStatus</b> is not set to 
        <b>NET_IF_ADMIN_STATUS_DOWN</b> and <b>ifOperStatus</b> is set to 
        <b>IfOperStatusDown</b> then a fault condition is presumed to exist on the interface. If 
        <b>AdminStatus</b> is set to <b>IfOperStatusDown</b>, then 
        <b>ifOperStatus</b> will normally also be set to 
        <b>IfOperStatusDown</b> or <b>IfOperStatusNotPresent</b> and there 
        is not necessarily a fault condition on the interface.

</td>
</tr>
<tr>
<td width="40%"><a id="IfOperStatusTesting"></a><a id="ifoperstatustesting"></a><a id="IFOPERSTATUSTESTING"></a><dl>
<dt><b>IfOperStatusTesting</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The interface is in testing mode.

</td>
</tr>
<tr>
<td width="40%"><a id="IfOperStatusUnknown"></a><a id="ifoperstatusunknown"></a><a id="IFOPERSTATUSUNKNOWN"></a><dl>
<dt><b>IfOperStatusUnknown</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The operational status of the interface is unknown.

</td>
</tr>
<tr>
<td width="40%"><a id="IfOperStatusDormant"></a><a id="ifoperstatusdormant"></a><a id="IFOPERSTATUSDORMANT"></a><dl>
<dt><b>IfOperStatusDormant</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The interface is not actually in a condition to pass packets (it is not up), but is in a pending state, 
        waiting for some external event. For on-demand interfaces, this new state identifies the situation where the 
        interface is waiting for events to place it in the <b>IfOperStatusUp</b> state.

</td>
</tr>
<tr>
<td width="40%"><a id="IfOperStatusNotPresent"></a><a id="ifoperstatusnotpresent"></a><a id="IFOPERSTATUSNOTPRESENT"></a><dl>
<dt><b>IfOperStatusNotPresent</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
A refinement on the <b>IfOperStatusDown</b> state which indicates that the relevant 
        interface is down specifically because some component (typically, a hardware component) is not present in the 
        managed system.

</td>
</tr>
<tr>
<td width="40%"><a id="IfOperStatusLowerLayerDown"></a><a id="ifoperstatuslowerlayerdown"></a><a id="IFOPERSTATUSLOWERLAYERDOWN"></a><dl>
<dt><b>IfOperStatusLowerLayerDown</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
A refinement on the <b>IfOperStatusDown</b> state. This new state indicates that 
        this interface runs on top of one or more other interfaces and that this interface is down specifically 
        because one or more of these lower-layer interfaces are down.

</td>
</tr>
</table>

### -field Ipv6IfIndex

Type: <b>DWORD</b>

The interface index for the IPv6 IP address. This member is zero if IPv6 is not available on the interface.
      

<div class="alert"><b>Note</b>  This structure member is only available on Windows XP with SP1 and later.</div>
<div> </div>

### -field ZoneIndices

Type: <b>DWORD[16]</b>

An array of scope IDs for each scope level used for composing 
      <a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structures. The 
      <a href="/windows/desktop/api/ws2def/ne-ws2def-scope_level">SCOPE_LEVEL</a> enumeration is used to index the array. On 
      IPv6, a single interface may be assigned multiple IPv6 multicast addresses based on a scope ID.
      

<div class="alert"><b>Note</b>  This structure member is only available on Windows XP with SP1 and later.</div>
<div> </div>

### -field FirstPrefix

Type: <b>PIP_ADAPTER_PREFIX</b>

A pointer to the first <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_prefix_xp">IP_ADAPTER_PREFIX</a> 
      structure in a linked list of IP adapter prefixes  for the adapter.
      

<div class="alert"><b>Note</b>  This structure member is only available on Windows XP with SP1 and later.</div>
<div> </div>

### -field TransmitLinkSpeed

Type: <b>ULONG64</b>

The current speed in bits per second of the transmit link for the adapter.
      

<div class="alert"><b>Note</b>  This structure member is only available on Windows Vista and later.</div>
<div> </div>

### -field ReceiveLinkSpeed

Type: <b>ULONG64</b>

The current speed in bits per second of the receive link for the adapter.
      

<div class="alert"><b>Note</b>  This structure member is only available on Windows Vista and later.</div>
<div> </div>

### -field FirstWinsServerAddress

Type: <b>PIP_ADAPTER_WINS_SERVER_ADDRESS_LH</b>

A pointer to the first 
      <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_wins_server_address_lh">IP_ADAPTER_WINS_SERVER_ADDRESS</a> structure in a linked  list of Windows Internet Name Service  (WINS) server 
      addresses for the adapter.
      

<div class="alert"><b>Note</b>  This structure member is only available on Windows Vista and later.</div>
<div> </div>

### -field FirstGatewayAddress

Type: <b>PIP_ADAPTER_GATEWAY_ADDRESS_LH</b>

A pointer to the first <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_gateway_address_lh">IP_ADAPTER_GATEWAY_ADDRESS</a> structure in a linked 
      list of gateways for the adapter.
      

<div class="alert"><b>Note</b>  This structure member is only available on Windows Vista and later.</div>
<div> </div>

### -field Ipv4Metric

Type: <b>ULONG</b>

The IPv4 interface metric for the adapter address. This member is only applicable to an IPv4 adapter 
      address.

The actual route metric used to compute the route preferences for IPv4 is the summation of the route metric 
       offset specified in the <b>Metric</b> member of the 
       <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipforward_row2">MIB_IPFORWARD_ROW2</a> structure and the interface 
       metric specified in this member for IPv4.

<div class="alert"><b>Note</b>  This structure member is only available on Windows Vista and later.</div>
<div> </div>

### -field Ipv6Metric

Type: <b>ULONG</b>

The IPv6 interface metric for the adapter address. This member is only applicable to an IPv6 adapter 
      address.
      

The actual route metric used to compute the route preferences for IPv6 is the summation of the route metric 
       offset specified in the <b>Metric</b> member of the 
       <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipforward_row2">MIB_IPFORWARD_ROW2</a> structure and the interface 
       metric specified in this member for IPv4.

<div class="alert"><b>Note</b>  This structure member is only available on Windows Vista and later.</div>
<div> </div>

### -field Luid

Type: <b>IF_LUID</b>

The interface LUID for the adapter address.
      

<div class="alert"><b>Note</b>  This structure member is only available on Windows Vista and later.</div>
<div> </div>

### -field Dhcpv4Server

Type: <b><a href="/windows/desktop/api/ws2def/ns-ws2def-socket_address">SOCKET_ADDRESS</a></b>

The IPv4 address of the DHCP server for the adapter address. This member is only applicable to an IPv4 
      adapter address configured using DHCP.
      

<div class="alert"><b>Note</b>  This structure member is only available on Windows Vista and later.</div>
<div> </div>

### -field CompartmentId

Type: <b>NET_IF_COMPARTMENT_ID</b>

The routing compartment ID for the adapter address.
      

<div class="alert"><b>Note</b>  This structure member is only available on Windows Vista and later. This member is not 
       currently supported and is reserved for future use.</div>
<div> </div>

### -field NetworkGuid

Type: <b>NET_IF_NETWORK_GUID</b>

The <b>GUID</b> that is associated with the network that the interface belongs to. 

If 
      the interface provider cannot provide the network GUID, this member can be a zero <b>GUID</b>.
      In this case, the interface was registered by NDIS in the default network.

<div class="alert"><b>Note</b>  This structure member is only available on Windows Vista and later.</div>
<div> </div>

### -field ConnectionType

Type: <b>NET_IF_CONNECTION_TYPE</b>

The interface connection type for the adapter address.
      

This member can be one of the values from the <b>NET_IF_CONNECTION_TYPE</b> enumeration 
       type defined in the <i>Ifdef.h</i> header file.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NET_IF_CONNECTION_DEDICATED"></a><a id="net_if_connection_dedicated"></a><dl>
<dt><b>NET_IF_CONNECTION_DEDICATED</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The connection type is dedicated. The connection comes up automatically when media sense is <b>TRUE</b>. For 
        example, an Ethernet connection is dedicated.

</td>
</tr>
<tr>
<td width="40%"><a id="NET_IF_CONNECTION_PASSIVE"></a><a id="net_if_connection_passive"></a><dl>
<dt><b>NET_IF_CONNECTION_PASSIVE</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The connection type is passive. The remote end must bring up the connection to the local station. For 
        example, a RAS interface is passive.

</td>
</tr>
<tr>
<td width="40%"><a id="NET_IF_CONNECTION_DEMAND"></a><a id="net_if_connection_demand"></a><dl>
<dt><b>NET_IF_CONNECTION_DEMAND</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The connection type is demand-dial. A connection of this type comes up in response to a local action 
        (sending a packet, for example).

</td>
</tr>
<tr>
<td width="40%"><a id="NET_IF_CONNECTION_MAXIMUM"></a><a id="net_if_connection_maximum"></a><dl>
<dt><b>NET_IF_CONNECTION_MAXIMUM</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The maximum possible value for the <b>NET_IF_CONNECTION_TYPE</b> enumeration type. 
        This is not a legal value for <b>ConnectionType</b> member.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  This structure member is only available on Windows Vista and later.</div>
<div> </div>

### -field TunnelType

Type: <b>TUNNEL_TYPE</b>

The encapsulation method used by a tunnel if the adapter address is a tunnel.
      

<div class="alert"><b>Note</b>  This structure member is only available on Windows Vista and later.</div>
<div> </div>
The tunnel type is defined by the Internet Assigned Names Authority (IANA). For more information, see 
      <a href="https://www.iana.org/assignments/ianaiftype-mib">http://www.iana.org/assignments/ianaiftype-mib</a>. 
      This member can be one of the values from the <b>TUNNEL_TYPE</b> enumeration type defined 
      in the <i>Ifdef.h</i> header file.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TUNNEL_TYPE_NONE"></a><a id="tunnel_type_none"></a><dl>
<dt><b>TUNNEL_TYPE_NONE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Not a tunnel.

</td>
</tr>
<tr>
<td width="40%"><a id="TUNNEL_TYPE_OTHER"></a><a id="tunnel_type_other"></a><dl>
<dt><b>TUNNEL_TYPE_OTHER</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
None of the following tunnel types.

</td>
</tr>
<tr>
<td width="40%"><a id="TUNNEL_TYPE_DIRECT"></a><a id="tunnel_type_direct"></a><dl>
<dt><b>TUNNEL_TYPE_DIRECT</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
A packet is encapsulated directly within a normal IP header, with no intermediate header, and unicast to 
        the remote tunnel endpoint.

</td>
</tr>
<tr>
<td width="40%"><a id="TUNNEL_TYPE_6TO4"></a><a id="tunnel_type_6to4"></a><dl>
<dt><b>TUNNEL_TYPE_6TO4</b></dt>
<dt>11</dt>
</dl>
</td>
<td width="60%">
An IPv6 packet is encapsulated directly within an IPv4 header, with no intermediate header, and unicast 
        to the destination determined by the 6to4 protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="TUNNEL_TYPE_ISATAP"></a><a id="tunnel_type_isatap"></a><dl>
<dt><b>TUNNEL_TYPE_ISATAP</b></dt>
<dt>13</dt>
</dl>
</td>
<td width="60%">
An IPv6 packet is encapsulated directly within an IPv4 header, with no intermediate header, and unicast 
        to the destination determined by the ISATAP protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="TUNNEL_TYPE_TEREDO"></a><a id="tunnel_type_teredo"></a><dl>
<dt><b>TUNNEL_TYPE_TEREDO</b></dt>
<dt>14</dt>
</dl>
</td>
<td width="60%">
Teredo encapsulation for IPv6 packets.

</td>
</tr>
<tr>
<td width="40%"><a id="TUNNEL_TYPE_IPHTTPS"></a><a id="tunnel_type_iphttps"></a><dl>
<dt><b>TUNNEL_TYPE_IPHTTPS</b></dt>
<dt>15</dt>
</dl>
</td>
<td width="60%">
IP over HTTPS encapsulation for IPv6 packets.

<div class="alert"><b>Note</b>  This enumeration value is only available on Windows 7,  Windows Server 2008 R2, and later.</div>
<div> </div>
</td>
</tr>
</table>

### -field Dhcpv6Server

Type: <b><a href="/windows/desktop/api/ws2def/ns-ws2def-socket_address">SOCKET_ADDRESS</a></b>

The IPv6 address of the DHCPv6 server for the adapter address. This member is only applicable to an IPv6 
      adapter address configured using DHCPv6. This structure member is not currently supported and is reserved for future use.

<div class="alert"><b>Note</b>  This structure member is only available on Windows Vista and later.</div>
<div> </div>

### -field Dhcpv6ClientDuid

Type: <b>BYTE[MAX_DHCPV6_DUID_LENGTH]</b>

The DHCP unique identifier (DUID) for the DHCPv6 client. This member is only applicable to an IPv6 adapter 
      address configured using DHCPv6.
      

<div class="alert"><b>Note</b>  This structure member is only available on Windows Vista and later.</div>
<div> </div>

### -field Dhcpv6ClientDuidLength

Type: <b>ULONG</b>

The length, in bytes, of the DHCP unique identifier (DUID) for the DHCPv6 client. This member is only 
      applicable to an IPv6 adapter address configured using DHCPv6.
      

<div class="alert"><b>Note</b>  This structure member is only available on Windows Vista and later.</div>
<div> </div>

### -field Dhcpv6Iaid

Type: <b>ULONG</b>

The identifier for an identity association chosen by the DHCPv6 client. This member is only applicable to 
      an IPv6 adapter address configured using DHCPv6.

<div class="alert"><b>Note</b>  This structure member is only available on Windows Vista and later.</div>
<div> </div>

### -field FirstDnsSuffix

Type: <b>PIP_ADAPTER_DNS_SUFFIX</b>

A pointer to the first <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_dns_suffix">IP_ADAPTER_DNS_SUFFIX</a> structure in a linked list of 
      DNS suffixes for the adapter.

<div class="alert"><b>Note</b>  This structure member is only available on Windows Vista with SP1and later and on Windows Server 2008  and later.</div>
<div> </div>

## -remarks

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses">GetAdaptersAddresses</a> function retrieves 
     information for IPv4 and IPv6 addresses and returns this information as a linked list of 
     <b>IP_ADAPTER_ADDRESSES</b> structures

The adapter index values specified in the <b>IfIndex</b> and <b>Ipv6IfIndex</b> members may change when an adapter is 
     disabled and then enabled, or under other circumstances, and should not be considered persistent.

The values for the <b>IfType</b> member are defined in the 
     <i>Ipifcons.h</i> header file. Only the possible values listed in the description of the 
     <b>IfType</b> member are currently supported.

The size of the <b>IP_ADAPTER_ADDRESSES</b> structure 
     changed on Windows XP with SP1 and later. The size of the 
     <b>IP_ADAPTER_ADDRESSES</b> structure also changed on 
     Windows Vista and later. The size of the 
     <b>IP_ADAPTER_ADDRESSES</b> structure also changed on 
     Windows Vista with SP1and later and onWindows Server 2008 and later. The <b>Length</b> member should be used to determine 
     which version of the <b>IP_ADAPTER_ADDRESSES</b> 
     structure is being used.

The version of the <b>IP_ADAPTER_ADDRESSES</b> 
     structure on Windows XP with SP1 and later has the following new members added: 
     <b>Ipv6IfIndex</b>, <b>ZoneIndices</b>, and 
     <b>FirstPrefix</b>.

The version of the <b>IP_ADAPTER_ADDRESSES</b> 
     structure on Windows Vista and later has the following new members added: 
     <b>TransmitLinkSpeed</b>, <b>ReceiveLinkSpeed</b>, 
     <b>FirstWinsServerAddress</b>, <b>FirstGatewayAddress</b>, 
     <b>Ipv4Metric</b>, <b>Ipv6Metric</b>, <b>Luid</b>, 
     <b>Dhcpv4Server</b>, <b>CompartmentId</b>, 
     <b>NetworkGuid</b>, <b>ConnectionType</b>, 
     <b>TunnelType</b>, <b>Dhcpv6Server</b>, 
     <b>Dhcpv6ClientDuid</b>, <b>Dhcpv6ClientDuidLength</b>, and 
     <b>Dhcpv6Iaid</b>.

The version of the <b>IP_ADAPTER_ADDRESSES</b> 
     structure on Windows Vista with SP1and later and on Windows Server 2008 and later has the following new member added:
     <b>FirstDnsSuffix</b>.

The <b>Ipv4Metric</b> and <b>Ipv6Metric</b> members are used to 
     prioritize route metrics for routes connected to multiple interfaces on the local computer.

The order of  linked <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh">IP_ADAPTER_UNICAST_ADDRESS</a> structures pointed to by the <b>FirstUnicastAddress</b> 
    member that are returned by the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses">GetAdaptersAddresses</a> function does not reflect the order that IP addresses were added to an adapter and may vary between versions of Windows. Similarly, the order of linked <b>IP_ADAPTER_ANYCAST_ADDRESS</b> structures pointed to by the <b>FirstAnycastAddress</b> 
    member and the order of linked <b>IP_ADAPTER_MULTICAST_ADDRESS</b> structures pointed to by the <b>FirstMulticastAddress 
</b> 
    member do not reflect the order that IP addresses were added to an adapter and may vary between versions of Windows. 

 In addition, the linked <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh">IP_ADAPTER_UNICAST_ADDRESS</a> structures pointed to by the <b>FirstUnicastAddress</b> 
    member and the linked <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_prefix_xp">IP_ADAPTER_PREFIX</a> structures pointed to by the <b>FirstPrefix</b> 
    member are maintained as separate internal linked lists by the operating system. As a result, the order of linked <b>IP_ADAPTER_UNICAST_ADDRESS</b> structures pointed to by the <b>FirstUnicastAddress</b> 
    member does not have any relationship with the order of linked <b>IP_ADAPTER_PREFIX</b> structures pointed to by the <b>FirstPrefix</b> 
    member. 

On Windows Vista and later, the linked <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_prefix_xp">IP_ADAPTER_PREFIX</a> structures pointed to by the <b>FirstPrefix</b> 
    member include three IP adapter prefixes for each IP address assigned to the adapter. These include the host IP address prefix, the subnet IP address prefix, and the subnet broadcast IP address prefix. In addition, for each adapter there is a multicast address prefix and a broadcast address prefix.

On Windows XP with SP1 and later prior to Windows Vista, the linked <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_prefix_xp">IP_ADAPTER_PREFIX</a> structures pointed to by the <b>FirstPrefix</b> 
    member include only a single IP adapter prefix for each IP address assigned to the adapter. 

In the Windows SDK, the version of the structure for use on Windows Vista and later is  defined as 
     <b>IP_ADAPTER_ADDRESSES_LH</b>. In the 
     Microsoft Windows Software Development Kit (SDK), the version of this structure to be used on earlier systems including 
     Windows XP with SP1 and later is defined as 
     <b>IP_ADAPTER_ADDRESSES_XP</b>. When compiling an 
     application if the target platform is Windows Vista and later 
     (<code>NTDDI_VERSION &gt;= NTDDI_LONGHORN</code>, 
     <code>_WIN32_WINNT &gt;= 0x0600</code>, or 
     <code>WINVER &gt;= 0x0600</code>), the 
     <b>IP_ADAPTER_ADDRESSES_LH</b> structure is typedefed to 
     the <b>IP_ADAPTER_ADDRESSES</b> structure. When compiling an application if the target 
     platform is not Windows Vista and later, the 
     <b>IP_ADAPTER_ADDRESSES_XP</b> structure is typedefed to 
     the <b>IP_ADAPTER_ADDRESSES</b> structure.

The <a href="/windows/desktop/api/ws2def/ns-ws2def-socket_address">SOCKET_ADDRESS</a> structure is used in the 
     <b>IP_ADAPTER_ADDRESSES</b> structure. On the 
     Windows SDK released for Windows Vista and later, the organization of header files has 
     changed and the <b>SOCKET_ADDRESS</b> structure is defined 
     in the <i>Ws2def.h</i> header file which is automatically included by the 
     <i>Winsock2.h</i> header file. On the Platform Software Development Kit (SDK) released for 
     Windows Server 2003 and Windows XP, the 
     <b>SOCKET_ADDRESS</b> structure is declared in the 
     <i>Winsock2.h</i> header file. In order to use the 
     <b>IP_ADAPTER_ADDRESSES</b> structure, the 
     <i>Winsock2.h</i> header file must be included before the 
     <i>Iphlpapi.h</i> header file.


#### Examples

This example retrieves the <b>IP_ADAPTER_ADDRESSES</b> structure for the adapters associated with the system and prints some members  for each adapter interface.


```cpp
#include <winsock2.h>
#include <iphlpapi.h>
#include <stdio.h>
#pragma comment(lib, "IPHLPAPI.lib")

#define MALLOC(x) HeapAlloc(GetProcessHeap(), 0, (x))
#define FREE(x) HeapFree(GetProcessHeap(), 0, (x))

/* Note: could also use malloc() and free() */

int __cdecl main(int argc, char **argv)
{

    /* Declare and initialize variables */

    DWORD dwSize = 0;
    DWORD dwRetVal = 0;

    unsigned int i = 0;

    // Set the flags to pass to GetAdaptersAddresses
    ULONG flags = GAA_FLAG_INCLUDE_PREFIX;

    // default to unspecified address family (both)
    ULONG family = AF_UNSPEC;

    LPVOID lpMsgBuf = NULL;

    PIP_ADAPTER_ADDRESSES pAddresses = NULL;
    ULONG outBufLen = 0;

    PIP_ADAPTER_ADDRESSES pCurrAddresses = NULL;
    PIP_ADAPTER_UNICAST_ADDRESS pUnicast = NULL;
    PIP_ADAPTER_ANYCAST_ADDRESS pAnycast = NULL;
    PIP_ADAPTER_MULTICAST_ADDRESS pMulticast = NULL;
    IP_ADAPTER_DNS_SERVER_ADDRESS *pDnServer = NULL;
    IP_ADAPTER_PREFIX *pPrefix = NULL;

    if (argc != 2) {
        printf(" Usage: getadapteraddresses family\n");
        printf("        getadapteraddresses 4 (for IPv4)\n");
        printf("        getadapteraddresses 6 (for IPv6)\n");
        printf("        getadapteraddresses A (for both IPv4 and IPv6)\n");
        exit(1);
    }

    if (atoi(argv[1]) == 4)
        family = AF_INET;
    else if (atoi(argv[1]) == 6)
        family = AF_INET6;

    outBufLen = sizeof (IP_ADAPTER_ADDRESSES);
    pAddresses = (IP_ADAPTER_ADDRESSES *) MALLOC(outBufLen);

    // Make an initial call to GetAdaptersAddresses to get the 
    // size needed into the outBufLen variable
    if (GetAdaptersAddresses(family, flags, NULL, pAddresses, &outBufLen)
        == ERROR_BUFFER_OVERFLOW) {
        FREE(pAddresses);
        pAddresses = (IP_ADAPTER_ADDRESSES *) MALLOC(outBufLen);
    }

    if (pAddresses == NULL) {
        printf("Memory allocation failed for IP_ADAPTER_ADDRESSES struct\n");
        exit(1);
    }
    // Make a second call to GetAdaptersAddresses to get the
    // actual data we want
    printf("Memory allocated for GetAdapterAddresses = %d bytes\n", outBufLen);
    printf("Calling GetAdaptersAddresses function with family = ");
    if (family == AF_INET)
        printf("AF_INET\n");
    if (family == AF_INET6)
        printf("AF_INET6\n");
    if (family == AF_UNSPEC)
        printf("AF_UNSPEC\n\n");

    dwRetVal =
        GetAdaptersAddresses(family, flags, NULL, pAddresses, &outBufLen);

    if (dwRetVal == NO_ERROR) {
        // If successful, output some information from the data we received
        pCurrAddresses = pAddresses;
        while (pCurrAddresses) {
            printf("\tLength of the IP_ADAPTER_ADDRESS struct: %ld\n",
                   pCurrAddresses->Length);
            printf("\tIfIndex (IPv4 interface): %u\n", pCurrAddresses->IfIndex);
            printf("\tAdapter name: %s\n", pCurrAddresses->AdapterName);

            pUnicast = pCurrAddresses->FirstUnicastAddress;
            if (pUnicast != NULL) {
                for (i = 0; pUnicast != NULL; i++)
                    pUnicast = pUnicast->Next;
                printf("\tNumber of Unicast Addresses: %d\n", i);
            } else
                printf("\tNo Unicast Addresses\n");

            pAnycast = pCurrAddresses->FirstAnycastAddress;
            if (pAnycast) {
                for (i = 0; pAnycast != NULL; i++)
                    pAnycast = pAnycast->Next;
                printf("\tNumber of Anycast Addresses: %d\n", i);
            } else
                printf("\tNo Anycast Addresses\n");

            pMulticast = pCurrAddresses->FirstMulticastAddress;
            if (pMulticast) {
                for (i = 0; pMulticast != NULL; i++)
                    pMulticast = pMulticast->Next;
                printf("\tNumber of Multicast Addresses: %d\n", i);
            } else
                printf("\tNo Multicast Addresses\n");

            pDnServer = pCurrAddresses->FirstDnsServerAddress;
            if (pDnServer) {
                for (i = 0; pDnServer != NULL; i++)
                    pDnServer = pDnServer->Next;
                printf("\tNumber of DNS Server Addresses: %d\n", i);
            } else
                printf("\tNo DNS Server Addresses\n");

            printf("\tDNS Suffix: %wS\n", pCurrAddresses->DnsSuffix);
            printf("\tDescription: %wS\n", pCurrAddresses->Description);
            printf("\tFriendly name: %wS\n", pCurrAddresses->FriendlyName);

            if (pCurrAddresses->PhysicalAddressLength != 0) {
                printf("\tPhysical address: ");
                for (i = 0; i < pCurrAddresses->PhysicalAddressLength;
                     i++) {
                    if (i == (pCurrAddresses->PhysicalAddressLength - 1))
                        printf("%.2X\n",
                               (int) pCurrAddresses->PhysicalAddress[i]);
                    else
                        printf("%.2X-",
                               (int) pCurrAddresses->PhysicalAddress[i]);
                }
            }
            printf("\tFlags: %ld\n", pCurrAddresses->Flags);
            printf("\tMtu: %lu\n", pCurrAddresses->Mtu);
            printf("\tIfType: %ld\n", pCurrAddresses->IfType);
            printf("\tOperStatus: %ld\n", pCurrAddresses->OperStatus);
            printf("\tIpv6IfIndex (IPv6 interface): %u\n",
                   pCurrAddresses->Ipv6IfIndex);
            printf("\tZoneIndices (hex): ");
            for (i = 0; i < 16; i++)
                printf("%lx ", pCurrAddresses->ZoneIndices[i]);
            printf("\n");

            pPrefix = pCurrAddresses->FirstPrefix;
            if (pPrefix) {
                for (i = 0; pPrefix != NULL; i++)
                    pPrefix = pPrefix->Next;
                printf("\tNumber of IP Adapter Prefix entries: %d\n", i);
            } else
                printf("\tNo IP Adapter Prefix entries\n");

            printf("\n");

            pCurrAddresses = pCurrAddresses->Next;
        }
    } else {
        printf("Call to GetAdaptersAddresses failed with error: %d\n",
               dwRetVal);
        if (dwRetVal == ERROR_NO_DATA)
            printf("\tNo addresses were found for the requested parameters\n");
        else {

            if (FormatMessage(FORMAT_MESSAGE_ALLOCATE_BUFFER | FORMAT_MESSAGE_FROM_SYSTEM | FORMAT_MESSAGE_IGNORE_INSERTS, NULL, dwRetVal, MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),   // Default language
                              (LPTSTR) & lpMsgBuf, 0, NULL)) {
                printf("\tError: %s", lpMsgBuf);
                LocalFree(lpMsgBuf);
                FREE(pAddresses);
                exit(1);
            }
        }
    }
    FREE(pAddresses);
    return 0;
}

```

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses">GetAdaptersAddresses</a>



<a href="/windows/desktop/api/ifdef/ne-ifdef-if_oper_status">IF_OPER_STATUS</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/IpHlp/ip-helper-structures">IP Helper Structures</a>



<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_anycast_address_xp">IP_ADAPTER_ANYCAST_ADDRESS</a>



<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_dns_server_address_xp">IP_ADAPTER_DNS_SERVER_ADDRESS</a>



<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_dns_suffix">IP_ADAPTER_DNS_SUFFIX</a>



<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_gateway_address_lh">IP_ADAPTER_GATEWAY_ADDRESS</a>



<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_multicast_address_xp">IP_ADAPTER_MULTICAST_ADDRESS</a>



<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_prefix_xp">IP_ADAPTER_PREFIX</a>



<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh">IP_ADAPTER_UNICAST_ADDRESS</a>



<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_wins_server_address_lh">IP_ADAPTER_WINS_SERVER_ADDRESS</a>



<a href="/windows/desktop/api/ws2def/ne-ws2def-scope_level">SCOPE_LEVEL</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-socket_address">SOCKET_ADDRESS</a>



<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a>
