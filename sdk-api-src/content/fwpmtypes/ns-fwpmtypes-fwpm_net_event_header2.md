---
UID: NS:fwpmtypes.FWPM_NET_EVENT_HEADER2_
title: FWPM_NET_EVENT_HEADER2 (fwpmtypes.h)
description: Contains information common to all events. (FWPM_NET_EVENT_HEADER2)
helpviewer_keywords: ["FWPM_NET_EVENT_FLAG_APP_ID_SET","FWPM_NET_EVENT_FLAG_IP_PROTOCOL_SET","FWPM_NET_EVENT_FLAG_IP_VERSION_SET","FWPM_NET_EVENT_FLAG_LOCAL_ADDR_SET","FWPM_NET_EVENT_FLAG_LOCAL_PORT_SET","FWPM_NET_EVENT_FLAG_PACKAGE_ID_SET","FWPM_NET_EVENT_FLAG_REAUTH_REASON_SET","FWPM_NET_EVENT_FLAG_REMOTE_ADDR_SET","FWPM_NET_EVENT_FLAG_REMOTE_PORT_SET","FWPM_NET_EVENT_FLAG_SCOPE_ID_SET","FWPM_NET_EVENT_FLAG_USER_ID_SET","FWPM_NET_EVENT_HEADER2","FWPM_NET_EVENT_HEADER2 structure [Filtering]","fwp.fwpm_net_event_header2","fwpmtypes/FWPM_NET_EVENT_HEADER2"]
old-location: fwp\fwpm_net_event_header2.htm
tech.root: fwp
ms.assetid: 1120d807-9188-4674-9acd-4b96e680f8af
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT_FLAG_APP_ID_SET, FWPM_NET_EVENT_FLAG_IP_PROTOCOL_SET, FWPM_NET_EVENT_FLAG_IP_VERSION_SET, FWPM_NET_EVENT_FLAG_LOCAL_ADDR_SET, FWPM_NET_EVENT_FLAG_LOCAL_PORT_SET, FWPM_NET_EVENT_FLAG_PACKAGE_ID_SET, FWPM_NET_EVENT_FLAG_REAUTH_REASON_SET, FWPM_NET_EVENT_FLAG_REMOTE_ADDR_SET, FWPM_NET_EVENT_FLAG_REMOTE_PORT_SET, FWPM_NET_EVENT_FLAG_SCOPE_ID_SET, FWPM_NET_EVENT_FLAG_USER_ID_SET, FWPM_NET_EVENT_HEADER2, FWPM_NET_EVENT_HEADER2 structure [Filtering], fwp.fwpm_net_event_header2, fwpmtypes/FWPM_NET_EVENT_HEADER2
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: FWPM_NET_EVENT_HEADER2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_NET_EVENT_HEADER2_
 - fwpmtypes/FWPM_NET_EVENT_HEADER2_
 - FWPM_NET_EVENT_HEADER2
 - fwpmtypes/FWPM_NET_EVENT_HEADER2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fwpmtypes.h
api_name:
 - FWPM_NET_EVENT_HEADER2
---

# FWPM_NET_EVENT_HEADER2 structure


## -description

The **FWPM_NET_EVENT_HEADER2** structure contains information common to all events.
[FWPM_NET_EVENT_HEADER0](ns-fwpmtypes-fwpm_net_event_header0.md) is available.

## -struct-fields

### -field timeStamp

Type: **[FILETIME](../minwinbase/ns-minwinbase-filetime.md)**

Time that the event occurred.

### -field flags

Type: **UINT32**

Flags indicating which of the following members are set.  Unused fields must be zero-initialized.

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
| FWPM_NET_EVENT_FLAG_REAUTH_REASON_SET | Indicates an existing connection was reauthorized. |
| FWPM_NET_EVENT_FLAG_PACKAGE_ID_SET | The **packageSid** member is set. |

### -field ipVersion

Type: **[FWP_IP_VERSION](../fwptypes/ne-fwptypes-fwp_ip_version.md)**

The IP version being used.

### -field ipProtocol

Type: **UINT8**

The IP protocol specified as an IPPROTO value. See the [socket](../winsock2/nf-winsock2-socket.md) reference topic for more information on possible protocol values.

### -field localAddrV4

Type: **UINT32**

The IPv4 local address.

Available when **ipVersion** is **FWP_IP_VERSION_V4**.

### -field localAddrV6

Type: **[FWP_BYTE_ARRAY16](../fwptypes/ns-fwptypes-fwp_byte_array16.md)**

The IPv6 local address.

Available when **ipVersion** is **FWP_IP_VERSION_V6**.

### -field remoteAddrV4

Type: **UINT32**

The IPv4 remote address.

Available when **ipVersion** is **FWP_IP_VERSION_V4**.

### -field remoteAddrV6

Type: **[FWP_BYTE_ARRAY16](../fwptypes/ns-fwptypes-fwp_byte_array16.md)**

The IPv6 remote address.

Available when **ipVersion** is **FWP_IP_VERSION_V6**.

### -field localPort

Type: **UINT16**

The local port.

### -field remotePort

Type: **UINT16**

The remote port.

### -field scopeId

Type: **UINT32**

The IPv6 scope ID.

### -field appId

Type: **[FWP_BYTE_BLOB](../fwptypes/ns-fwptypes-fwp_byte_blob.md)**

The application ID of the local application associated with the event.

### -field userId

Type: **SID***

The user ID corresponding to the traffic.

### -field addressFamily

Type: **[FWP_AF](../fwptypes/ne-fwptypes-fwp_af.md)**

A superset of non-Internet protocols.

Available when **ipVersion** is **FWP_IP_VERSION_NONE**.

### -field packageSid

Type: **SID***

The security identifier (SID) representing the package identifier (also referred to as the app container SID) intending to send or receive the network traffic.

## -see-also

[FWP_AF](../fwptypes/ne-fwptypes-fwp_af.md)

[FWP_BYTE_ARRAY16](../fwptypes/ns-fwptypes-fwp_byte_array16.md)

[FWP_BYTE_BLOB](../fwptypes/ns-fwptypes-fwp_byte_blob.md)

[FWP_IP_VERSION](../fwptypes/ne-fwptypes-fwp_ip_version.md)
