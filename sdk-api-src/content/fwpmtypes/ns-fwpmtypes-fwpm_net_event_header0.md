---
UID: NS:fwpmtypes.FWPM_NET_EVENT_HEADER0_
title: FWPM_NET_EVENT_HEADER0 (fwpmtypes.h)
description: Information common to all events.
helpviewer_keywords: ["FWPM_NET_EVENT_FLAG_APP_ID_SET","FWPM_NET_EVENT_FLAG_IP_PROTOCOL_SET","FWPM_NET_EVENT_FLAG_IP_VERSION_SET","FWPM_NET_EVENT_FLAG_LOCAL_ADDR_SET","FWPM_NET_EVENT_FLAG_LOCAL_PORT_SET","FWPM_NET_EVENT_FLAG_REMOTE_ADDR_SET","FWPM_NET_EVENT_FLAG_REMOTE_PORT_SET","FWPM_NET_EVENT_FLAG_SCOPE_ID_SET","FWPM_NET_EVENT_FLAG_USER_ID_SET","FWPM_NET_EVENT_HEADER0","FWPM_NET_EVENT_HEADER0 structure [Filtering]","fwp.fwpm_net_event_header0","fwpmtypes/FWPM_NET_EVENT_HEADER0"]
old-location: fwp\fwpm_net_event_header0.htm
tech.root: fwp
ms.assetid: 2fbb805d-d38b-4918-a291-fe1000ac2ea2
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT_FLAG_APP_ID_SET, FWPM_NET_EVENT_FLAG_IP_PROTOCOL_SET, FWPM_NET_EVENT_FLAG_IP_VERSION_SET, FWPM_NET_EVENT_FLAG_LOCAL_ADDR_SET, FWPM_NET_EVENT_FLAG_LOCAL_PORT_SET, FWPM_NET_EVENT_FLAG_REMOTE_ADDR_SET, FWPM_NET_EVENT_FLAG_REMOTE_PORT_SET, FWPM_NET_EVENT_FLAG_SCOPE_ID_SET, FWPM_NET_EVENT_FLAG_USER_ID_SET, FWPM_NET_EVENT_HEADER0, FWPM_NET_EVENT_HEADER0 structure [Filtering], fwp.fwpm_net_event_header0, fwpmtypes/FWPM_NET_EVENT_HEADER0
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: FWPM_NET_EVENT_HEADER0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_NET_EVENT_HEADER0_
 - fwpmtypes/FWPM_NET_EVENT_HEADER0_
 - FWPM_NET_EVENT_HEADER0
 - fwpmtypes/FWPM_NET_EVENT_HEADER0
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
 - FWPM_NET_EVENT_HEADER0
---

# FWPM_NET_EVENT_HEADER0 structure


## -description

The **FWPM_NET_EVENT_HEADER0** structure contains information common to all events.
[FWPM_NET_EVENT_HEADER2](ns-fwpmtypes-fwpm_net_event_header2.md) is available.

## -struct-fields

### -field timeStamp

A [FILETIME](../minwinbase/ns-minwinbase-filetime.md) structure that specifies the time the event occurred

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

### -field ipVersion

A [FWP_IP_VERSION](../fwptypes/ne-fwptypes-fwp_ip_version.md) value that specifies the IP version being used.

### -field ipProtocol

IP protocol specified as an IPPROTO value. See the [socket](/windows/desktop/api/winsock2/nf-winsock2-socket) reference topic for more information on possible protocol values.

### -field localAddrV4

Specifies an IPv4 local address.

Available when **ipVersion** is **FWP_IP_VERSION_V4**.

### -field localAddrV6

A [FWP_BYTE_ARRAY16](../fwptypes/ns-fwptypes-fwp_byte_array16.md) that contains an IPv6 local address.

Available when **ipVersion** is **FWP_IP_VERSION_V6**.

### -field remoteAddrV4

Specifies an IPv4 remote address.

Available when **ipVersion** is **FWP_IP_VERSION_V4**.

### -field remoteAddrV6

A [FWP_BYTE_ARRAY16](../fwptypes/ns-fwptypes-fwp_byte_array16.md) that contains an IPv6 remote address.

Available when **ipVersion** is **FWP_IP_VERSION_V6**.

### -field localPort

Specifies a local port.

### -field remotePort

Specifies a remote port.

### -field scopeId

IPv6 scope ID.

### -field appId

A [FWP_BYTE_BLOB](../fwptypes/ns-fwptypes-fwp_byte_blob.md) that contains the application ID of the local application associated with the event.

### -field userId

Contains a user ID that corresponds to the traffic.

## -see-also

[FILETIME](../minwinbase/ns-minwinbase-filetime.md)

[FWPM_NET_EVENT0](ns-fwpmtypes-fwpm_net_event0.md)

[FWP_BYTE_ARRAY16](../fwptypes/ns-fwptypes-fwp_byte_array16.md)

[FWP_BYTE_BLOB](../fwptypes/ns-fwptypes-fwp_byte_blob.md)

[FWP_IP_VERSION](../fwptypes/ne-fwptypes-fwp_ip_version.md)

[Windows Filtering Platform  API Structures](/windows/desktop/FWP/fwp-structs)

[socket](/windows/desktop/api/winsock2/nf-winsock2-socket)
