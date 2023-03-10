---
UID: NS:fwpmtypes.FWPM_NET_EVENT_HEADER3_
title: FWPM_NET_EVENT_HEADER3 (fwpmtypes.h)
description: Contains information common to all events. (FWPM_NET_EVENT_HEADER3)
helpviewer_keywords: ["FWPM_NET_EVENT_FLAG_APP_ID_SET","FWPM_NET_EVENT_FLAG_IP_PROTOCOL_SET","FWPM_NET_EVENT_FLAG_IP_VERSION_SET","FWPM_NET_EVENT_FLAG_LOCAL_ADDR_SET","FWPM_NET_EVENT_FLAG_LOCAL_PORT_SET","FWPM_NET_EVENT_FLAG_PACKAGE_ID_SET","FWPM_NET_EVENT_FLAG_REAUTH_REASON_SET","FWPM_NET_EVENT_FLAG_REMOTE_ADDR_SET","FWPM_NET_EVENT_FLAG_REMOTE_PORT_SET","FWPM_NET_EVENT_FLAG_SCOPE_ID_SET","FWPM_NET_EVENT_FLAG_USER_ID_SET","FWPM_NET_EVENT_HEADER3","FWPM_NET_EVENT_HEADER3 structure [Filtering]","fwp.fwpm_net_event_header3","fwpmtypes/FWPM_NET_EVENT_HEADER3"]
old-location: fwp\fwpm_net_event_header3.htm
tech.root: fwp
ms.assetid: 1AAC1649-B9F2-40E6-956B-6179A3E1C112
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT_FLAG_APP_ID_SET, FWPM_NET_EVENT_FLAG_IP_PROTOCOL_SET, FWPM_NET_EVENT_FLAG_IP_VERSION_SET, FWPM_NET_EVENT_FLAG_LOCAL_ADDR_SET, FWPM_NET_EVENT_FLAG_LOCAL_PORT_SET, FWPM_NET_EVENT_FLAG_PACKAGE_ID_SET, FWPM_NET_EVENT_FLAG_REAUTH_REASON_SET, FWPM_NET_EVENT_FLAG_REMOTE_ADDR_SET, FWPM_NET_EVENT_FLAG_REMOTE_PORT_SET, FWPM_NET_EVENT_FLAG_SCOPE_ID_SET, FWPM_NET_EVENT_FLAG_USER_ID_SET, FWPM_NET_EVENT_HEADER3, FWPM_NET_EVENT_HEADER3 structure [Filtering], fwp.fwpm_net_event_header3, fwpmtypes/FWPM_NET_EVENT_HEADER3
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: FWPM_NET_EVENT_HEADER3
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_NET_EVENT_HEADER3_
 - fwpmtypes/FWPM_NET_EVENT_HEADER3_
 - FWPM_NET_EVENT_HEADER3
 - fwpmtypes/FWPM_NET_EVENT_HEADER3
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
 - FWPM_NET_EVENT_HEADER3
---

# FWPM_NET_EVENT_HEADER3 structure


## -description

The **FWPM_NET_EVENT_HEADER3** structure contains information common to all events.
[FWPM_NET_EVENT_HEADER0](ns-fwpmtypes-fwpm_net_event_header0.md) is available.

## -struct-fields

### -field timeStamp

Time that the event occurred.

### -field flags

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

The IP version being used.

### -field ipProtocol

The IP protocol specified as an IPPROTO value. See the [socket](../winsock2/nf-winsock2-socket.md) reference topic for more information on possible protocol values.

### -field localAddrV4

The IPv4 local address.

Available when **ipVersion** is **FWP_IP_VERSION_V4**.

### -field localAddrV6

The IPv6 local address.

Available when **ipVersion** is **FWP_IP_VERSION_V6**.

### -field remoteAddrV4

The IPv4 remote address.

Available when **ipVersion** is **FWP_IP_VERSION_V4**.

### -field remoteAddrV6

The IPv6 remote address.

Available when **ipVersion** is **FWP_IP_VERSION_V6**.

### -field localPort

The local port.

### -field remotePort

The remote port.

### -field scopeId

The IPv6 scope ID.

### -field appId

The application ID of the local application associated with the event.

### -field userId

The user ID corresponding to the traffic.

### -field addressFamily

A superset of non-Internet protocols.

Available when **ipVersion** is **FWP_IP_VERSION_NONE**.

### -field packageSid

The security identifier (SID) representing the package identifier (also referred to as the app container SID) intending to send or receive the network traffic.

### -field enterpriseId

The enterprise identifier for use with enterprise data protection (EDP).

### -field policyFlags

The policy flags for EDP.

### -field effectiveName

The EDP remote server used for name-based policy.

## -see-also

[FWP_AF](../fwptypes/ne-fwptypes-fwp_af.md)

[FWP_BYTE_ARRAY16](../fwptypes/ns-fwptypes-fwp_byte_array16.md)

[FWP_BYTE_BLOB](../fwptypes/ns-fwptypes-fwp_byte_blob.md)

[FWP_IP_VERSION](../fwptypes/ne-fwptypes-fwp_ip_version.md)
