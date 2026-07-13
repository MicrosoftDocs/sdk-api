---
UID: NS:ifdef._NET_LUID_LH
title: NET_LUID_LH (ifdef.h)
description: The locally unique identifier (LUID) for a network interface.
helpviewer_keywords: ["*PIF_LUID","*PNET_LUID","*PNET_LUID_LH","IF_LUID","IF_TYPE_ATM","IF_TYPE_ETHERNET_CSMACD","IF_TYPE_IEEE1394","IF_TYPE_IEEE80211","IF_TYPE_ISO88025_TOKENRING","IF_TYPE_OTHER","IF_TYPE_PPP","IF_TYPE_SOFTWARE_LOOPBACK","IF_TYPE_TUNNEL","NET_LUID","NET_LUID union [IP Helper]","NET_LUID_LH","PNET_LUID","PNET_LUID union pointer [IP Helper]","ifdef/NET_LUID","ifdef/PNET_LUID","iphlp.net_luid"]
old-location: iphlp\net_luid.htm
tech.root: IpHlp
ms.assetid: c4956c5a-3c6c-4f1c-b9d7-2e377b66f197
ms.date: 12/05/2018
ms.keywords: '*PIF_LUID, *PNET_LUID, *PNET_LUID_LH, IF_LUID, IF_TYPE_ATM, IF_TYPE_ETHERNET_CSMACD, IF_TYPE_IEEE1394, IF_TYPE_IEEE80211, IF_TYPE_ISO88025_TOKENRING, IF_TYPE_OTHER, IF_TYPE_PPP, IF_TYPE_SOFTWARE_LOOPBACK, IF_TYPE_TUNNEL, NET_LUID, NET_LUID union [IP Helper], NET_LUID_LH, PNET_LUID, PNET_LUID union pointer [IP Helper], ifdef/NET_LUID, ifdef/PNET_LUID, iphlp.net_luid'
req.header: ifdef.h
req.include-header: 
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
req.typenames: NET_LUID_LH, *PNET_LUID_LH
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NET_LUID_LH
 - ifdef/_NET_LUID_LH
 - PNET_LUID_LH
 - ifdef/PNET_LUID_LH
 - NET_LUID_LH
 - ifdef/NET_LUID_LH
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ifdef.h
api_name:
 - NET_LUID
---

# NET_LUID_LH structure


## -description

The <b>NET_LUID</b> union is the locally unique identifier (LUID) for a network interface.

## -struct-fields

### -field Value

Type: <b>ULONG64</b>

A 64-bit value that represents the LUID.

### -field Info

A named union containing the component fields in the 64-bit LUID  <b>Value</b> member.

### -field Info.Reserved

Type: <b>ULONG64</b>

This field is reserved.

### -field Info.NetLuidIndex

Type: <b>ULONG64</b>

The network interface LUID index.

### -field Info.IfType

Type: <b>ULONG64</b>

The interface type as defined by the Internet Assigned Names Authority (IANA). Possible values for the interface type are listed in the <i>Ipifcons.h</i> include file. 

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

## -remarks

The <b>NET_LUID</b> structure is protocol independent and works with network interfaces for both the IPv6 and IPv4 protocol. The <b>NET_LUID</b> structure is defined on Windows Vista and later. 

The <b>IF_LUID</b> and <b>NET_LUID_LH</b> structures are other names that can be used for the <b>NET_LUID</b> union.

The values for the <b>IfType</b> bitfield are defined in the <i>Ipifcons.h</i> include file. Only the possible values listed in the description of the <b>IfType</b> member are currently supported.

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfacealiastoluid">ConvertInterfaceAliasToLuid</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceguidtoluid">ConvertInterfaceGuidToLuid</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceindextoluid">ConvertInterfaceIndexToLuid</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtoguid">ConvertInterfaceLuidToGuid</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtoindex">ConvertInterfaceLuidToIndex</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtonamea">ConvertInterfaceLuidToNameA</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfaceluidtonamew">ConvertInterfaceLuidToNameW</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfacenametoluida">ConvertInterfaceNameToLuidA</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-convertinterfacenametoluidw">ConvertInterfaceNameToLuidW</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2">MIB_IF_ROW2</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipinterface_row">MIB_IPINTERFACE_ROW</a>