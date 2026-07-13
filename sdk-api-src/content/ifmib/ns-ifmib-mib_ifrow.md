---
UID: NS:ifmib._MIB_IFROW
title: MIB_IFROW (ifmib.h)
description: Stores information about a particular interface. (MIB_IFROW)
helpviewer_keywords: ["*PMIB_IFROW","IF_OPER_STATUS_CONNECTED","IF_OPER_STATUS_CONNECTING","IF_OPER_STATUS_DISCONNECTED","IF_OPER_STATUS_NON_OPERATIONAL","IF_OPER_STATUS_OPERATIONAL","IF_OPER_STATUS_UNREACHABLE","IF_TYPE_ATM","IF_TYPE_ETHERNET_CSMACD","IF_TYPE_FDDI","IF_TYPE_IEEE1394","IF_TYPE_IEEE80211","IF_TYPE_IEEE80216_WMAN","IF_TYPE_ISO88025_TOKENRING","IF_TYPE_OTHER","IF_TYPE_PPP","IF_TYPE_SOFTWARE_LOOPBACK","IF_TYPE_TUNNEL","IF_TYPE_WWANPP","IF_TYPE_WWANPP2","MIB_IFROW","MIB_IFROW structure [MIB]","PMIB_IFROW","PMIB_IFROW structure pointer [MIB]","_mpr_mib_ifrow","ifmib/MIB_IFROW","ifmib/PMIB_IFROW","iprtrmib/MIB_IFROW","iprtrmib/PMIB_IFROW","mib.mib_ifrow","rras.mib_ifrow"]
old-location: mib\mib_ifrow.htm
tech.root: MIB
ms.assetid: b08631e9-6036-4377-b2f2-4ea899acb787
ms.date: 12/05/2018
ms.keywords: '*PMIB_IFROW, IF_OPER_STATUS_CONNECTED, IF_OPER_STATUS_CONNECTING, IF_OPER_STATUS_DISCONNECTED, IF_OPER_STATUS_NON_OPERATIONAL, IF_OPER_STATUS_OPERATIONAL, IF_OPER_STATUS_UNREACHABLE, IF_TYPE_ATM, IF_TYPE_ETHERNET_CSMACD, IF_TYPE_FDDI, IF_TYPE_IEEE1394, IF_TYPE_IEEE80211, IF_TYPE_IEEE80216_WMAN, IF_TYPE_ISO88025_TOKENRING, IF_TYPE_OTHER, IF_TYPE_PPP, IF_TYPE_SOFTWARE_LOOPBACK, IF_TYPE_TUNNEL, IF_TYPE_WWANPP, IF_TYPE_WWANPP2, MIB_IFROW, MIB_IFROW structure [MIB], PMIB_IFROW, PMIB_IFROW structure pointer [MIB], _mpr_mib_ifrow, ifmib/MIB_IFROW, ifmib/PMIB_IFROW, iprtrmib/MIB_IFROW, iprtrmib/PMIB_IFROW, mib.mib_ifrow, rras.mib_ifrow'
req.header: ifmib.h
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
req.typenames: MIB_IFROW, *PMIB_IFROW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_IFROW
 - ifmib/_MIB_IFROW
 - PMIB_IFROW
 - ifmib/PMIB_IFROW
 - MIB_IFROW
 - ifmib/MIB_IFROW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ifmib.h
 - Iprtrmib.h
api_name:
 - MIB_IFROW
---

# MIB_IFROW structure


## -description

The 
<b>MIB_IFROW</b> structure stores information about a particular interface.

## -struct-fields

### -field wszName

Type: <b>WCHAR[MAX_INTERFACE_NAME_LEN]</b>

A pointer to a Unicode string that contains the name of the interface.

### -field dwIndex

Type: <b>DWORD</b>

The index that identifies the interface. This index value may change when a network adapter is disabled and then enabled, and should not be considered persistent.

### -field dwType

Type: <b>DWORD</b>

The interface type as defined by the Internet Assigned Names Authority (IANA). For more information, see <a href="https://www.iana.org/assignments/ianaiftype-mib">http://www.iana.org/assignments/ianaiftype-mib</a>. Possible values for the interface type are listed in the <i>Ipifcons.h</i> header file. 

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
<td width="40%"><a id="IF_TYPE_FDDI"></a><a id="if_type_fddi"></a><dl>
<dt><b>IF_TYPE_FDDI</b></dt>
<dt>15</dt>
</dl>
</td>
<td width="60%">
A Fiber Distributed Data Interface (FDDI) network interface.

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
<tr>
<td width="40%"><a id="_IF_TYPE_IEEE80216_WMAN"></a><a id="_if_type_ieee80216_wman"></a><dl>
<dt><b> IF_TYPE_IEEE80216_WMAN</b></dt>
<dt>237</dt>
</dl>
</td>
<td width="60%">
A mobile broadband interface for WiMax devices.

<div class="alert"><b>Note</b>  This interface type is supported on Windows 7,   Windows Server 2008 R2, and later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="IF_TYPE_WWANPP"></a><a id="if_type_wwanpp"></a><dl>
<dt><b>IF_TYPE_WWANPP</b></dt>
<dt>243</dt>
</dl>
</td>
<td width="60%">
A mobile broadband interface for GSM-based devices.

<div class="alert"><b>Note</b>  This interface type is supported on Windows 7,   Windows Server 2008 R2, and later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="IF_TYPE_WWANPP2"></a><a id="if_type_wwanpp2"></a><dl>
<dt><b>IF_TYPE_WWANPP2</b></dt>
<dt>244</dt>
</dl>
</td>
<td width="60%">
An mobile broadband interface for CDMA-based devices.

<div class="alert"><b>Note</b>  This interface type is supported on Windows 7,   Windows Server 2008 R2, and later.</div>
<div> </div>
</td>
</tr>
</table>

### -field dwMtu

Type: <b>DWORD</b>

The Maximum Transmission Unit (MTU) size in bytes.

### -field dwSpeed

Type: <b>DWORD</b>

The speed of the interface in bits per second.

### -field dwPhysAddrLen

Type: <b>DWORD</b>

The length, in bytes, of the physical address specified by the <b>bPhysAddr</b> member.

### -field bPhysAddr

Type: <b>BYTE[MAXLEN_PHYSADDR]</b>

The physical address of the adapter for this interface.

### -field dwAdminStatus

Type: <b>DWORD</b>

The interface is administratively enabled or disabled.

### -field dwOperStatus

Type: <b>DWORD</b>

The operational status of the interface. This member can be one of the following values defined in the INTERNAL_IF_OPER_STATUS enumeration defined in the <i>Ipifcons.h</i> header file. 
					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IF_OPER_STATUS_NON_OPERATIONAL"></a><a id="if_oper_status_non_operational"></a><dl>
<dt><b>IF_OPER_STATUS_NON_OPERATIONAL</b></dt>
</dl>
</td>
<td width="60%">
LAN adapter has been disabled, for example because of an address conflict.

</td>
</tr>
<tr>
<td width="40%"><a id="IF_OPER_STATUS_UNREACHABLE"></a><a id="if_oper_status_unreachable"></a><dl>
<dt><b>IF_OPER_STATUS_UNREACHABLE</b></dt>
</dl>
</td>
<td width="60%">
WAN adapter that is not connected.

</td>
</tr>
<tr>
<td width="40%"><a id="IF_OPER_STATUS_DISCONNECTED"></a><a id="if_oper_status_disconnected"></a><dl>
<dt><b>IF_OPER_STATUS_DISCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
For LAN adapters: network cable disconnected. For WAN adapters: no carrier.

</td>
</tr>
<tr>
<td width="40%"><a id="IF_OPER_STATUS_CONNECTING"></a><a id="if_oper_status_connecting"></a><dl>
<dt><b>IF_OPER_STATUS_CONNECTING</b></dt>
</dl>
</td>
<td width="60%">
WAN adapter that is in the process of connecting.

</td>
</tr>
<tr>
<td width="40%"><a id="IF_OPER_STATUS_CONNECTED"></a><a id="if_oper_status_connected"></a><dl>
<dt><b>IF_OPER_STATUS_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
WAN adapter that is connected to a remote peer.

</td>
</tr>
<tr>
<td width="40%"><a id="IF_OPER_STATUS_OPERATIONAL"></a><a id="if_oper_status_operational"></a><dl>
<dt><b>IF_OPER_STATUS_OPERATIONAL</b></dt>
</dl>
</td>
<td width="60%">
Default status for LAN adapters

</td>
</tr>
</table>

### -field dwLastChange

Type: <b>DWORD</b>

The  length of time, in hundredths of seconds (10^-2 sec), starting from the last computer restart, when the interface entered its current operational state. This value rolls over after 2^32 hundredths of a second. 

The <b>dwLastChange</b> member is not currently supported by NDIS. On Windows Vista and later, NDIS returns zero for this member. On earlier versions of Windows, an arbitrary value is returned in this member for the interfaces supported by NDIS. For interfaces supported by other interface providers, they might return an appropriate value.

### -field dwInOctets

Type: <b>DWORD</b>

The number of octets of data received through this interface.

### -field dwInUcastPkts

Type: <b>DWORD</b>

The number of unicast packets received through this interface.

### -field dwInNUcastPkts

Type: <b>DWORD</b>

The number of non-unicast packets received through this interface. Broadcast and multicast packets are included.

### -field dwInDiscards

Type: <b>DWORD</b>

The number of incoming packets that were discarded even though they did not have errors.

### -field dwInErrors

Type: <b>DWORD</b>

The number of incoming packets that were discarded because of errors.

### -field dwInUnknownProtos

Type: <b>DWORD</b>

The number of incoming packets that were discarded because the protocol was unknown.

### -field dwOutOctets

Type: <b>DWORD</b>

The number of octets of data sent through this interface.

### -field dwOutUcastPkts

Type: <b>DWORD</b>

The number of unicast packets sent through this interface.

### -field dwOutNUcastPkts

Type: <b>DWORD</b>

The number of non-unicast packets sent through this interface. Broadcast and multicast packets are included.

### -field dwOutDiscards

Type: <b>DWORD</b>

The number of outgoing packets that were discarded even though they did not have errors.

### -field dwOutErrors

Type: <b>DWORD</b>

The number of outgoing packets that were discarded because of errors.

### -field dwOutQLen

Type: <b>DWORD</b>

The transmit queue length. This field is not currently used.

### -field dwDescrLen

Type: <b>DWORD</b>

The length, in bytes, of the <b>bDescr</b> member.

### -field bDescr

Type: <b>BYTE[MAXLEN_IFDESCR]</b>

A description of the interface.

## -remarks

The <b>dwSpeed</b> member of the <b>MIB_IFROW</b> structure will be incorrect for very high-speed network interfaces (10 Gbit/s network adapter, for example) since the maximum value that can be store in a DWORD is 4,294,967,295. Applications should use the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2">MIB_IF_ROW2</a> structure returned by the <a href="/windows/desktop/api/netioapi/nf-netioapi-getifentry2">GetIfEntry2</a> and <a href="/windows/desktop/api/netioapi/nf-netioapi-getiftable2">GetIfTable2</a> functions or the <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_lh">IP_ADAPTER_ADDRESSES</a> structure returned by the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses">GetAdaptersAddresses</a> function for determining the speed for very high-speed network interfaces.

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>MIB_IFROW</b> structure is defined in the <i>Ifmib.h</i> header file not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ifmib.h</i> header file is automatically included in <i>Iprtrmib.h</i> which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Ifmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses">GetAdaptersAddresses</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getifentry">GetIfEntry</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getifentry2">GetIfEntry2</a>



<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_lh">IP_ADAPTER_ADDRESSES</a>



<a href="/windows/desktop/api/iprtrmib/ns-iprtrmib-mib_ifstatus">MIB_IFSTATUS</a>



<a href="/windows/desktop/api/ifmib/ns-ifmib-mib_iftable">MIB_IFTABLE</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_table2">MIB_IF_TABLE2</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_0">MPR_INTERFACE_0</a>
