---
UID: NS:fwpmtypes.FWPM_NET_EVENT_HEADER1_
title: FWPM_NET_EVENT_HEADER1 (fwpmtypes.h)
description: Information common to all events. Reserved.helpviewer_keywords: ["FWPM_NET_EVENT_FLAG_APP_ID_SET","FWPM_NET_EVENT_FLAG_IP_PROTOCOL_SET","FWPM_NET_EVENT_FLAG_IP_VERSION_SET","FWPM_NET_EVENT_FLAG_LOCAL_ADDR_SET","FWPM_NET_EVENT_FLAG_LOCAL_PORT_SET","FWPM_NET_EVENT_FLAG_REMOTE_ADDR_SET","FWPM_NET_EVENT_FLAG_REMOTE_PORT_SET","FWPM_NET_EVENT_FLAG_SCOPE_ID_SET","FWPM_NET_EVENT_FLAG_USER_ID_SET","FWPM_NET_EVENT_HEADER1","FWPM_NET_EVENT_HEADER1 structure [Filtering]","fwp.fwpm_net_event_header1","fwpmtypes/FWPM_NET_EVENT_HEADER1"]
old-location: fwp\fwpm_net_event_header1.htm
tech.root: fwp
ms.assetid: b5315a3b-07ae-4596-92f3-0ca72ca4dd49
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT_FLAG_APP_ID_SET, FWPM_NET_EVENT_FLAG_IP_PROTOCOL_SET, FWPM_NET_EVENT_FLAG_IP_VERSION_SET, FWPM_NET_EVENT_FLAG_LOCAL_ADDR_SET, FWPM_NET_EVENT_FLAG_LOCAL_PORT_SET, FWPM_NET_EVENT_FLAG_REMOTE_ADDR_SET, FWPM_NET_EVENT_FLAG_REMOTE_PORT_SET, FWPM_NET_EVENT_FLAG_SCOPE_ID_SET, FWPM_NET_EVENT_FLAG_USER_ID_SET, FWPM_NET_EVENT_HEADER1, FWPM_NET_EVENT_HEADER1 structure [Filtering], fwp.fwpm_net_event_header1, fwpmtypes/FWPM_NET_EVENT_HEADER1
f1_keywords:
- fwpmtypes/FWPM_NET_EVENT_HEADER1
dev_langs:
- c++
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
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
- Fwpmtypes.h
api_name:
- FWPM_NET_EVENT_HEADER1
targetos: Windows
req.typenames: FWPM_NET_EVENT_HEADER1
req.redist: 
ms.custom: 19H1
---

# FWPM_NET_EVENT_HEADER1 structure


## -description


The <b>FWPM_NET_EVENT_HEADER1</b> structure contains information common to all events. Reserved.
[FWPM_NET_EVENT_HEADER2](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_header2)a> is available. </div><div> </div>

## -struct-fields




### -field timeStamp

A <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that specifies the time the event occurred.


### -field flags

Flags indicating which of the following members are set.  Unused fields must be zero-initialized.

<table>
<tr>
<th>Net event flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FWPM_NET_EVENT_FLAG_IP_PROTOCOL_SET"></a><a id="fwpm_net_event_flag_ip_protocol_set"></a><dl>
<dt><b>FWPM_NET_EVENT_FLAG_IP_PROTOCOL_SET</b></dt>
</dl>
</td>
<td width="60%">
The <b>ipProtocol</b> member is set.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_NET_EVENT_FLAG_LOCAL_ADDR_SET"></a><a id="fwpm_net_event_flag_local_addr_set"></a><dl>
<dt><b>FWPM_NET_EVENT_FLAG_LOCAL_ADDR_SET</b></dt>
</dl>
</td>
<td width="60%">
Either the <b>localAddrV4</b>, <b>localAddrV6</b>, or <b>dstAddrEth</b> member is set. 

<div class="alert"><b>Note</b>  If this flag is present,  <b>FWPM_NET_EVENT_FLAG_IP_VERSION_SET</b> must also be present.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_NET_EVENT_FLAG_REMOTE_ADDR_SET"></a><a id="fwpm_net_event_flag_remote_addr_set"></a><dl>
<dt><b>FWPM_NET_EVENT_FLAG_REMOTE_ADDR_SET</b></dt>
</dl>
</td>
<td width="60%">
Either the <b>remoteAddrV4</b>, <b>remoteAddrV6</b>, or <b>srcAddrEth</b> field is set.

<div class="alert"><b>Note</b>  If this flag is present,  <b>FWPM_NET_EVENT_FLAG_IP_VERSION_SET</b> must also be present.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_NET_EVENT_FLAG_LOCAL_PORT_SET"></a><a id="fwpm_net_event_flag_local_port_set"></a><dl>
<dt><b>FWPM_NET_EVENT_FLAG_LOCAL_PORT_SET</b></dt>
</dl>
</td>
<td width="60%">
The <b>localPort</b> member is set.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_NET_EVENT_FLAG_REMOTE_PORT_SET"></a><a id="fwpm_net_event_flag_remote_port_set"></a><dl>
<dt><b>FWPM_NET_EVENT_FLAG_REMOTE_PORT_SET</b></dt>
</dl>
</td>
<td width="60%">
The <b>remotePort</b> member is set.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_NET_EVENT_FLAG_APP_ID_SET"></a><a id="fwpm_net_event_flag_app_id_set"></a><dl>
<dt><b>FWPM_NET_EVENT_FLAG_APP_ID_SET</b></dt>
</dl>
</td>
<td width="60%">
The <b>appId</b> member is set.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_NET_EVENT_FLAG_USER_ID_SET"></a><a id="fwpm_net_event_flag_user_id_set"></a><dl>
<dt><b>FWPM_NET_EVENT_FLAG_USER_ID_SET</b></dt>
</dl>
</td>
<td width="60%">
The <b>userId</b> member is set.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_NET_EVENT_FLAG_SCOPE_ID_SET"></a><a id="fwpm_net_event_flag_scope_id_set"></a><dl>
<dt><b>FWPM_NET_EVENT_FLAG_SCOPE_ID_SET</b></dt>
</dl>
</td>
<td width="60%">
The <b>scopeId</b> member is set.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_NET_EVENT_FLAG_IP_VERSION_SET"></a><a id="fwpm_net_event_flag_ip_version_set"></a><dl>
<dt><b>FWPM_NET_EVENT_FLAG_IP_VERSION_SET</b></dt>
</dl>
</td>
<td width="60%">
The <b>ipVersion</b> member is set.

</td>
</tr>
</table>
 


### -field ipVersion

An [FWP_IP_VERSION](https://docs.microsoft.com/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version)a> value that specifies the IP version being used. 


### -field ipProtocol

IP protocol specified as an IPPROTO value. See the <a href="https://docs.microsoft.com/windows/desktop/api/winsock2/nf-winsock2-socket">socket</a> reference topic for more information on possible protocol values.


### -field localAddrV4

Specifies an IPv4 local address.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.


### -field localAddrV6

A [FWP_BYTE_ARRAY16](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_array16)a> structure that specifies an IPv6 local address.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V6</b>.


### -field remoteAddrV4

Specifies an IPv4 remote address.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.


### -field remoteAddrV6

An [FWP_BYTE_ARRAY16](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_array16)a> structure that specifies an IPv6 remote address.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V6</b>.


### -field localPort

Specifies a local port.


### -field remotePort

Specifies a remote port.


### -field scopeId

IPv6 scope ID.


### -field appId

An [FWP_BYTE_BLOB](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob)a> that specifies the application ID of the local application associated with the event.


### -field userId

Contains a user ID that corresponds to the traffic.


### -field reserved1

Specifies a superset of non-Internet protocols.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_NONE</b>.


### -field reserved2

 


### -field reserved3

 


### -field reserved4

 


### -field reserved5

 


### -field reserved6

 


### -field reserved7

 


### -field reserved8

 


### -field reserved9

 


### -field reserved10

 




#### - ( unnamed struct )

Specifies details related to Ethernet traffic.

Available when <b>addressFamily</b> is <b>FWP_AF_ETHER</b>.



#### reserved2

A <a href="https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_array6_">FWP_BYTE_ARRAY6</a>  structure.



#### reserved3

A <a href="https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_array6_">FWP_BYTE_ARRAY6</a>  structure.



#### reserved4

A <a href="https://docs.microsoft.com/windows/win32/api/fwpmtypes/ne-fwpmtypes-dl_address_type">DL_ADDRESS_TYPE</a> enumeration.



#### reserved5

A <a href="https://docs.microsoft.com/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ether_encap_method_">FWP_ETHER_ENCAP_METHOD</a> enumeration.



#### reserved6

Indicates which protocol is encapsulated in the frame data.



#### reserved7

The SNAP (IEEE 802.2) DSAP, SSAP, and Control fields marshaled into a 32-bit value.



#### reserved8

The SNAP (IEEE 802.2) Organizationally Unique Identifier (OUI) marshaled into a 32-bit value.



#### reserved9

The VLAN (802.1p/q) VID, CFI, and Priority bits marshaled into a 16-bit value.



#### reserved10

The interface LUID corresponding to the network interface with which this packet is associated.


## -remarks



This structure is reserved for system use. [FWPM_NET_EVENT_HEADER2](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_header2)a> should be used in place of <b>FWPM_NET_EVENT_HEADER1</b>.




## -see-also




[FWPM_NET_EVENT_HEADER0](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_header0)a>



[FWPM_NET_EVENT_HEADER2](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_header2)a>
 

 

