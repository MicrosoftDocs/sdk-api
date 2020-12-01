---
UID: NS:fwpmtypes.FWPM_NET_EVENT_HEADER1_
title: FWPM_NET_EVENT_HEADER1 (fwpmtypes.h)
description: Information common to all events. Reserved.
helpviewer_keywords: ["FWPM_NET_EVENT_FLAG_APP_ID_SET","FWPM_NET_EVENT_FLAG_IP_PROTOCOL_SET","FWPM_NET_EVENT_FLAG_IP_VERSION_SET","FWPM_NET_EVENT_FLAG_LOCAL_ADDR_SET","FWPM_NET_EVENT_FLAG_LOCAL_PORT_SET","FWPM_NET_EVENT_FLAG_REMOTE_ADDR_SET","FWPM_NET_EVENT_FLAG_REMOTE_PORT_SET","FWPM_NET_EVENT_FLAG_SCOPE_ID_SET","FWPM_NET_EVENT_FLAG_USER_ID_SET","FWPM_NET_EVENT_HEADER1","FWPM_NET_EVENT_HEADER1 structure [Filtering]","fwp.fwpm_net_event_header1","fwpmtypes/FWPM_NET_EVENT_HEADER1"]
old-location: fwp\fwpm_net_event_header1.htm
tech.root: fwp
ms.assetid: b5315a3b-07ae-4596-92f3-0ca72ca4dd49
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT_FLAG_APP_ID_SET, FWPM_NET_EVENT_FLAG_IP_PROTOCOL_SET, FWPM_NET_EVENT_FLAG_IP_VERSION_SET, FWPM_NET_EVENT_FLAG_LOCAL_ADDR_SET, FWPM_NET_EVENT_FLAG_LOCAL_PORT_SET, FWPM_NET_EVENT_FLAG_REMOTE_ADDR_SET, FWPM_NET_EVENT_FLAG_REMOTE_PORT_SET, FWPM_NET_EVENT_FLAG_SCOPE_ID_SET, FWPM_NET_EVENT_FLAG_USER_ID_SET, FWPM_NET_EVENT_HEADER1, FWPM_NET_EVENT_HEADER1 structure [Filtering], fwp.fwpm_net_event_header1, fwpmtypes/FWPM_NET_EVENT_HEADER1
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
targetos: Windows
req.typenames: FWPM_NET_EVENT_HEADER1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_NET_EVENT_HEADER1_
 - fwpmtypes/FWPM_NET_EVENT_HEADER1_
 - FWPM_NET_EVENT_HEADER1
 - fwpmtypes/FWPM_NET_EVENT_HEADER1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwpmtypes.h
api_name:
 - FWPM_NET_EVENT_HEADER1
---

## -description

The **FWPM_NET_EVENT_HEADER1** structure contains information common to all events. Reserved.

[FWPM_NET_EVENT_HEADER2](ns-fwpmtypes-fwpm_net_event_header2.md) is available.

## -struct-fields

### -field timeStamp

A [FILETIME](../minwinbase/ns-minwinbase-filetime.md) structure that specifies the time the event occurred.

### -field flags

Flags indicating which of the following members are set. Unused fields must be zero-initialized.

| Net event flag | Meaning |
| -------------- | ------- |
| FWPM_NET_EVENT_FLAG_IP_PROTOCOL_SET | The **ipProtocol** member is set. |
| FWPM_NET_EVENT_FLAG_LOCAL_ADDR_SET | Either the **localAddrV4** member or the **localAddrV6** member is set. If this flag is present,  **FWPM_NET_EVENT_FLAG_IP_VERSION_SET** must also be present. |
| FWPM_NET_EVENT_FLAG_REMOTE_ADDR_SET | Either the **remoteAddrV4** member of the **remoteAddrV6** field is set. If this flag is present,  **FWPM_NET_EVENT_FLAG_IP_VERSION_SET** must also be present. |
| FWPM_NET_EVENT_FLAG_LOCAL_PORT_SET | The **localPort** member is set. |
| FWPM_NET_EVENT_FLAG_REMOTE_PORT_SET | The **remotePort** member is set. |
| FWPM_NET_EVENT_FLAG_APP_ID_SET | The **appId** member is set. |
| FWPM_NET_EVENT_FLAG_USER_ID_SET | The **userId** member is set. |
| FWPM_NET_EVENT_FLAG_SCOPE_ID_SET | The **scopeId** member is set. |
| FWPM_NET_EVENT_FLAG_IP_VERSION_SET | The **ipVersion** member is set. |

### -field ipVersion

An [FWP_IP_VERSION](../fwptypes/ne-fwptypes-fwp_ip_version.md) value that specifies the IP version being used.

### -field ipProtocol

IP protocol specified as an IPPROTO value. See the [socket](../winsock2/nf-winsock2-socket.md) reference topic for more information on possible protocol values.

### -field localAddrV4

Specifies an IPv4 local address.

Available when **ipVersion** is **FWP_IP_VERSION_V4**.

### -field localAddrV6

A [FWP_BYTE_ARRAY16](../fwptypes/ns-fwptypes-fwp_byte_array16.md) structure that specifies an IPv6 local address.

Available when **ipVersion** is **FWP_IP_VERSION_V6**.

### -field remoteAddrV4

Specifies an IPv4 remote address.

Available when **ipVersion** is **FWP_IP_VERSION_V4**.

### -field remoteAddrV6

An [FWP_BYTE_ARRAY16](../fwptypes/ns-fwptypes-fwp_byte_array16.md) structure that specifies an IPv6 remote address.

Available when **ipVersion** is **FWP_IP_VERSION_V6**.

### -field localPort

Specifies a local port.

### -field remotePort

Specifies a remote port.

### -field scopeId

IPv6 scope ID.

### -field appId

An [FWP_BYTE_BLOB](../fwptypes/ns-fwptypes-fwp_byte_blob.md) that specifies the application ID of the local application associated with the event.

### -field userId

Contains a user ID that corresponds to the traffic.

### -field reserved1

Specifies a superset of non-Internet protocols.

Available when **ipVersion** is **FWP_IP_VERSION_NONE**.

### -field reserved2

A [FWP_BYTE_ARRAY6](../fwptypes/ns-fwptypes-fwp_byte_array6.md) structure.

### -field reserved3

A [FWP_BYTE_ARRAY6](../fwptypes/ns-fwptypes-fwp_byte_array6.md) structure.

### -field reserved4

A [DL_ADDRESS_TYPE](../fwpmtypes/ne-fwpmtypes-dl_address_type.md) enumeration.

### -field reserved5

A [FWP_ETHER_ENCAP_METHOD](../fwptypes/ne-fwptypes-fwp_ether_encap_method.md) enumeration.

### -field reserved6

Indicates which protocol is encapsulated in the frame data.

### -field reserved7

The SNAP (IEEE 802.2) DSAP, SSAP, and Control fields marshaled into a 32-bit value.

### -field reserved8

The SNAP (IEEE 802.2) Organizationally Unique Identifier (OUI) marshaled into a 32-bit value.

### -field reserved9

The VLAN (802.1p/q) VID, CFI, and Priority bits marshaled into a 16-bit value.

### -field reserved10

The interface LUID corresponding to the network interface with which this packet is associated.

## -remarks

The unnamed struct specifies details related to Ethernet traffic. It's available when **addressFamily** is **FWP_AF_ETHER**.

This structure is reserved for system use. [FWPM_NET_EVENT_HEADER2](ns-fwpmtypes-fwpm_net_event_header2.md) should be used in place of **FWPM_NET_EVENT_HEADER1**.

## -see-also

[FWPM_NET_EVENT_HEADER0](ns-fwpmtypes-fwpm_net_event_header0.md)

[FWPM_NET_EVENT_HEADER2](ns-fwpmtypes-fwpm_net_event_header2.md)
