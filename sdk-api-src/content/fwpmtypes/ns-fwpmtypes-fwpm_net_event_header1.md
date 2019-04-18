---
UID: NS:fwpmtypes.FWPM_NET_EVENT_HEADER1_
title: FWPM_NET_EVENT_HEADER1 (fwpmtypes.h)
author: windows-sdk-content
description: Information common to all events. Reserved.
old-location: fwp\fwpm_net_event_header1.htm
tech.root: fwp
ms.assetid: b5315a3b-07ae-4596-92f3-0ca72ca4dd49
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT_FLAG_APP_ID_SET, FWPM_NET_EVENT_FLAG_IP_PROTOCOL_SET, FWPM_NET_EVENT_FLAG_IP_VERSION_SET, FWPM_NET_EVENT_FLAG_LOCAL_ADDR_SET, FWPM_NET_EVENT_FLAG_LOCAL_PORT_SET, FWPM_NET_EVENT_FLAG_REMOTE_ADDR_SET, FWPM_NET_EVENT_FLAG_REMOTE_PORT_SET, FWPM_NET_EVENT_FLAG_SCOPE_ID_SET, FWPM_NET_EVENT_FLAG_USER_ID_SET, FWPM_NET_EVENT_HEADER1, FWPM_NET_EVENT_HEADER1 structure [Filtering], fwp.fwpm_net_event_header1, fwpmtypes/FWPM_NET_EVENT_HEADER1
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: FWPM_NET_EVENT_HEADER1
req.redist: 
ms.custom: 19H1
---

# FWPM_NET_EVENT_HEADER1 structure


## -description


The <b>FWPM_NET_EVENT_HEADER1</b> structure contains information common to all events. Reserved.
<div class="alert"><b>Note</b>  <b>FWPM_NET_EVENT_HEADER1</b> is a specific implementation of FWPM_NET_EVENT_HEADER that is reserved for system use. For Windows Vista and Windows 7, <a href="https://msdn.microsoft.com/2fbb805d-d38b-4918-a291-fe1000ac2ea2">FWPM_NET_EVENT_HEADER0</a> is available. For Windows 8, <a href="https://msdn.microsoft.com/1120d807-9188-4674-9acd-4b96e680f8af">FWPM_NET_EVENT_HEADER2</a> is available. </div><div> </div>

## -struct-fields




### -field timeStamp

A <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that specifies the time the event occurred.


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

An <a href="https://msdn.microsoft.com/1712b83c-f32d-4981-9950-ab870a376182">FWP_IP_VERSION</a> value that specifies the IP version being used. 


### -field ipProtocol

IP protocol specified as an IPPROTO value. See the <a href="https://msdn.microsoft.com/6bf6e6c4-6268-479c-86a6-52e90cf317db">socket</a> reference topic for more information on possible protocol values.


### -field localAddrV4

Specifies an IPv4 local address.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.


### -field localAddrV6

A <a href="https://msdn.microsoft.com/254ee02f-747d-46e4-9851-141db57e1aa7">FWP_BYTE_ARRAY16</a> structure that specifies an IPv6 local address.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V6</b>.


### -field remoteAddrV4

Specifies an IPv4 remote address.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.


### -field remoteAddrV6

An <a href="https://msdn.microsoft.com/254ee02f-747d-46e4-9851-141db57e1aa7">FWP_BYTE_ARRAY16</a> structure that specifies an IPv6 remote address.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V6</b>.


### -field localPort

Specifies a local port.


### -field remotePort

Specifies a remote port.


### -field scopeId

IPv6 scope ID.


### -field appId

An <a href="https://msdn.microsoft.com/85f360bf-5ee4-4980-b4ce-15ff310d8fbe">FWP_BYTE_BLOB</a> that specifies the application ID of the local application associated with the event.


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

A <a href="https://msdn.microsoft.com/395b5c1c-988b-4d85-9b31-c1f84e02a90c">FWP_BYTE_ARRAY6</a>  structure.



#### reserved3

A <a href="https://msdn.microsoft.com/395b5c1c-988b-4d85-9b31-c1f84e02a90c">FWP_BYTE_ARRAY6</a>  structure.



#### reserved4

A <a href="https://msdn.microsoft.com/en-us/library/Dd744934(v=VS.85).aspx">DL_ADDRESS_TYPE</a> enumeration.



#### reserved5

A <a href="https://msdn.microsoft.com/fd94a02e-ba2d-4f99-a340-11f2e594f319">FWP_ETHER_ENCAP_METHOD</a> enumeration.



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



This structure is reserved for system use. <a href="https://msdn.microsoft.com/2fbb805d-d38b-4918-a291-fe1000ac2ea2">FWPM_NET_EVENT_HEADER0</a> or <a href="https://msdn.microsoft.com/1120d807-9188-4674-9acd-4b96e680f8af">FWPM_NET_EVENT_HEADER2</a> should be used in place of <b>FWPM_NET_EVENT_HEADER1</b>.




## -see-also




<a href="https://msdn.microsoft.com/2fbb805d-d38b-4918-a291-fe1000ac2ea2">FWPM_NET_EVENT_HEADER0</a>



<a href="https://msdn.microsoft.com/1120d807-9188-4674-9acd-4b96e680f8af">FWPM_NET_EVENT_HEADER2</a>
 

 

