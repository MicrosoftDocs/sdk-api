---
UID: NS:ifdef._NET_LUID_LH
title: "_NET_LUID_LH"
author: windows-sdk-content
description: The locally unique identifier (LUID) for a network interface.
old-location: iphlp\net_luid.htm
tech.root: IpHlp
ms.assetid: c4956c5a-3c6c-4f1c-b9d7-2e377b66f197
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PIF_LUID, *PNET_LUID, *PNET_LUID_LH, IF_LUID, IF_TYPE_ATM, IF_TYPE_ETHERNET_CSMACD, IF_TYPE_IEEE1394, IF_TYPE_IEEE80211, IF_TYPE_ISO88025_TOKENRING, IF_TYPE_OTHER, IF_TYPE_PPP, IF_TYPE_SOFTWARE_LOOPBACK, IF_TYPE_TUNNEL, NET_LUID, NET_LUID union [IP Helper], NET_LUID_LH, PNET_LUID, PNET_LUID union pointer [IP Helper], _NET_LUID_LH, ifdef/NET_LUID, ifdef/PNET_LUID, iphlp.net_luid"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ifdef.h
api_name:
 - NET_LUID
product: Windows
targetos: Windows
req.typenames: NET_LUID_LH, *PNET_LUID_LH
req.redist: 
---

# _NET_LUID_LH structure


## -description


The <b>NET_LUID</b> union is the locally unique identifier (LUID) for a network interface.


## -struct-fields




### -field Value

Type: <b>ULONG64</b>

A 64-bit value that represents the LUID.


### -field Info

A named union containing the component fields in the 64-bit LUID  <b>Value</b> member.


### -field Info.Reserved

<b>Type: <b>ULONG64</b>
</b>
This field is reserved.


### -field Info.NetLuidIndex

<b>Type: <b>ULONG64</b>
</b>
The network interface LUID index.


### -field Info.IfType

<b>Type: <b>ULONG64</b>
</b>
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




<a href="https://msdn.microsoft.com/7fa80938-d475-4ace-b463-a53aac26e88b">ConvertInterfaceAliasToLuid</a>



<a href="https://msdn.microsoft.com/cae669dc-899b-4485-b70a-5f58207a07df">ConvertInterfaceGuidToLuid</a>



<a href="https://msdn.microsoft.com/c757228c-93f1-4545-8921-9d048bca580c">ConvertInterfaceIndexToLuid</a>



<a href="https://msdn.microsoft.com/9d5bd1e9-0bf1-405a-8726-8e2c9ba4e022">ConvertInterfaceLuidToGuid</a>



<a href="https://msdn.microsoft.com/904cd94c-dd46-42ac-aef2-ffed4b3e5899">ConvertInterfaceLuidToIndex</a>



<a href="https://msdn.microsoft.com/c65f7b3c-55f4-40f8-9a7a-19d1066deca4">ConvertInterfaceLuidToNameA</a>



<a href="https://msdn.microsoft.com/e4269a6a-1237-4503-b7d7-756388458750">ConvertInterfaceLuidToNameW</a>



<a href="https://msdn.microsoft.com/daceabf9-ff43-4206-9f8f-f3924de9c5a5">ConvertInterfaceNameToLuidA</a>



<a href="https://msdn.microsoft.com/473be9f0-7fac-46f0-b33c-839906411fdc">ConvertInterfaceNameToLuidW</a>



<a href="https://msdn.microsoft.com/e8bb79f9-e7e9-470b-8883-36d08061661b">MIB_IF_ROW2</a>



<a href="https://msdn.microsoft.com/28265037-f7a3-40a4-b386-20f43f32a8b3">MIB_IPINTERFACE_ROW</a>
 

 

