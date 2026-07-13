---
UID: NE:fwpsu.FWPS_BUILTIN_LAYERS_
title: FWPS_BUILTIN_LAYERS
description: Defines constants that specify built-in run-time filtering layer identifiers. Each is represented by a locally unique identifier (LUID), which is 64 bits in size.
ms.date: 05/28/2024
tech.root: fwp
targetos: Windows
req.construct-type: enumeration
req.ddi-compliance: 
req.header: fwpsu.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: Windows
req.typenames: FWPS_BUILTIN_LAYERS_, FWPS_BUILTIN_LAYERS
typedef_isUnnamed: false
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - fwpsu.h
api_name:
 - FWPS_BUILTIN_LAYERS_
 - FWPS_BUILTIN_LAYERS
f1_keywords:
 - FWPS_BUILTIN_LAYERS_
 - fwpsu/FWPS_BUILTIN_LAYERS_
 - FWPS_BUILTIN_LAYERS
 - fwpsu/FWPS_BUILTIN_LAYERS
dev_langs:
 - c++
helpviewer_keywords:
 - FWPS_BUILTIN_LAYERS_
---

## -description

Defines constants that specify built-in run-time filtering layer identifiers. Each is represented by a locally unique identifier (LUID), which is 64 bits in size.

> [!NOTE]
> The V4 and V6 suffixes at the end of the run-time layer identifiers indicate whether the layer is located in the IPv4 network stack or in the IPv6 network stack.

## -enum-fields

### -field FWPS_LAYER_INBOUND_IPPACKET_V4

This filtering layer is located in the receive path just after the IP header of a received packet has been parsed but before any IP header processing takes place. No IPsec decryption or reassembly has occurred.

### -field FWPS_LAYER_INBOUND_IPPACKET_V4_DISCARD

This filtering layer is located in the receive path for processing any received packets that have been discarded at the network layer.

### -field FWPS_LAYER_INBOUND_IPPACKET_V6

This filtering layer is located in the receive path just after the IP header of a received packet has been parsed but before any IP header processing takes place. No IPsec decryption or reassembly has occurred.

### -field FWPS_LAYER_INBOUND_IPPACKET_V6_DISCARD

This filtering layer is located in the receive path for processing any received packets that have been discarded at the network layer.

### -field FWPS_LAYER_OUTBOUND_IPPACKET_V4

This filtering layer is located in the send path just before the sent packet is evaluated for fragmentation. All IP header processing is complete and all extension headers are in place. Any IPsec authentication and encryption has already occurred.

### -field FWPS_LAYER_OUTBOUND_IPPACKET_V4_DISCARD

This filtering layer is located in the send path for processing any sent packets that have been discarded at the network layer.

### -field FWPS_LAYER_OUTBOUND_IPPACKET_V6

This filtering layer is located in the send path just before the sent packet is evaluated for fragmentation. All IP header processing is complete and all extension headers are in place. Any IPsec authentication and encryption has already occurred.

### -field FWPS_LAYER_OUTBOUND_IPPACKET_V6_DISCARD

This filtering layer is located in the send path for processing any sent packets that have been discarded at the network layer.

### -field FWPS_LAYER_IPFORWARD_V4

This filtering layer is located in the forwarding path at the point where a received packet is forwarded.

### -field FWPS_LAYER_IPFORWARD_V4_DISCARD

This filtering layer is located in the forwarding path for processing any forwarded packets that have been discarded at the forward layer.

### -field FWPS_LAYER_IPFORWARD_V6

This filtering layer is located in the forwarding path at the point where a received packet is forwarded.

### -field FWPS_LAYER_IPFORWARD_V6_DISCARD

This filtering layer is located in the forwarding path for processing any forwarded packets that have been discarded at the forward layer.

### -field FWPS_LAYER_INBOUND_TRANSPORT_V4

This filtering layer is located in the receive path just after a received packet's header has been parsed by the network stack at the transport layer, but before any transport layer processing takes place.

### -field FWPS_LAYER_INBOUND_TRANSPORT_V4_DISCARD

This filtering layer is located in the receive path for processing any received packets that have been discarded at the transport layer.

### -field FWPS_LAYER_INBOUND_TRANSPORT_V6

This filtering layer is located in the receive path just after a received packet's header has been parsed by the network stack at the transport layer, but before any transport layer processing takes place.

### -field FWPS_LAYER_INBOUND_TRANSPORT_V6_DISCARD

This filtering layer is located in the receive path for processing any received packets that have been discarded at the transport layer.

### -field FWPS_LAYER_OUTBOUND_TRANSPORT_V4

This filtering layer is located in the send path just after a sent packet has been passed to the network layer for processing but before any network layer processing takes place. This filtering layer is located at the top of the network layer instead of at the bottom of the transport layer so that any packets that are sent by third-party transports or as raw packets are filtered at this layer.

### -field FWPS_LAYER_OUTBOUND_TRANSPORT_V4_DISCARD

This filtering layer is located in the send path for processing any sent packets that have been discarded at the transport layer.

### -field FWPS_LAYER_OUTBOUND_TRANSPORT_V6

This filtering layer is located in the send path just after a sent packet has been passed to the network layer for processing but before any network layer processing takes place. This filtering layer is located at the top of the network layer instead of at the bottom of the transport layer so that any packets that are sent by third-party transports or as raw packets are filtered at this layer.

### -field FWPS_LAYER_OUTBOUND_TRANSPORT_V6_DISCARD

This filtering layer is located in the send path for processing any sent packets that have been discarded at the transport layer.

### -field FWPS_LAYER_STREAM_V4

This filtering layer is located in the stream data path. This layer allows for processing network data on a per stream basis. At the stream layer, the network data is bidirectional.

### -field FWPS_LAYER_STREAM_V4_DISCARD

This filtering layer is reserved for future use.

### -field FWPS_LAYER_STREAM_V6

This filtering layer is located in the stream data path. This layer allows for processing network data on a per stream basis. At the stream layer, the network data is bidirectional.

### -field FWPS_LAYER_STREAM_V6_DISCARD

This filtering layer is reserved for future use.

### -field FWPS_LAYER_DATAGRAM_DATA_V4

This filtering layer is located in the datagram data path. This layer allows for processing network data on a per datagram basis. At the datagram layer, the network data is bidirectional.

### -field FWPS_LAYER_DATAGRAM_DATA_V4_DISCARD

This filtering layer is located in the datagram data path for processing any datagrams that have been discarded.

### -field FWPS_LAYER_DATAGRAM_DATA_V6

This filtering layer is located in the datagram data path. This layer allows for processing network data on a per datagram basis. At the datagram layer, the network data is bidirectional.

### -field FWPS_LAYER_DATAGRAM_DATA_V6_DISCARD

This filtering layer is located in the datagram data path for processing any datagrams that have been discarded.

### -field FWPS_LAYER_INBOUND_ICMP_ERROR_V4

This filtering layer is located in the receive path for processing received ICMP messages for the transport protocol.

### -field FWPS_LAYER_INBOUND_ICMP_ERROR_V4_DISCARD

This filtering layer is located in the receive path for processing received ICMP messages that have been discarded.

### -field FWPS_LAYER_INBOUND_ICMP_ERROR_V6

This filtering layer is located in the receive path for processing received ICMP messages for the transport protocol.

### -field FWPS_LAYER_INBOUND_ICMP_ERROR_V6_DISCARD

This filtering layer is located in the receive path for processing received ICMP messages that have been discarded.

### -field FWPS_LAYER_OUTBOUND_ICMP_ERROR_V4

This filtering layer is located in the send path for processing sent ICMP messages for the transport protocol.

### -field FWPS_LAYER_OUTBOUND_ICMP_ERROR_V4_DISCARD

This filtering layer is located in the send path for processing sent ICMP messages that have been discarded.

### -field FWPS_LAYER_OUTBOUND_ICMP_ERROR_V6

This filtering layer is located in the send path for processing sent ICMP messages for the transport protocol.

### -field FWPS_LAYER_OUTBOUND_ICMP_ERROR_V6_DISCARD

This filtering layer is located in the send path for processing sent ICMP messages that have been discarded.

### -field FWPS_LAYER_ALE_RESOURCE_ASSIGNMENT_V4

This filtering layer allows for authorizing transport port assignments, bind requests, promiscuous mode requests, and raw mode requests.

### -field FWPS_LAYER_ALE_RESOURCE_ASSIGNMENT_V4_DISCARD

This filtering layer allows for processing the following discarded items: transport port assignments, bind requests, promiscuous mode requests, and raw mode requests.

### -field FWPS_LAYER_ALE_RESOURCE_ASSIGNMENT_V6

This filtering layer allows for authorizing transport port assignments, bind requests, promiscuous mode requests, and raw mode requests.

### -field FWPS_LAYER_ALE_RESOURCE_ASSIGNMENT_V6_DISCARD

This filtering layer allows for processing the following discarded items: transport port assignments, bind requests, promiscuous mode requests, and raw mode requests.

### -field FWPS_LAYER_ALE_AUTH_LISTEN_V4

This filtering layer allows for authorizing TCP listen requests.

### -field FWPS_LAYER_ALE_AUTH_LISTEN_V4_DISCARD

This filtering layer allows for processing TCP listen requests that have been discarded.

### -field FWPS_LAYER_ALE_AUTH_LISTEN_V6

This filtering layer allows for authorizing TCP listen requests.

### -field FWPS_LAYER_ALE_AUTH_LISTEN_V6_DISCARD

This filtering layer allows for processing TCP listen requests that have been discarded.

### -field FWPS_LAYER_ALE_AUTH_RECV_ACCEPT_V4

This filtering layer allows for authorizing accept requests for incoming TCP connections, as well as authorizing incoming non-TCP traffic based on the first packet received.

### -field FWPS_LAYER_ALE_AUTH_RECV_ACCEPT_V4_DISCARD

This filtering layer allows for processing accept requests for incoming TCP connections that have been discarded, as well as processing authorizations for incoming non-TCP traffic that have been discarded.

### -field FWPS_LAYER_ALE_AUTH_RECV_ACCEPT_V6

This filtering layer allows for authorizing accept requests for incoming TCP connections, as well as authorizing incoming non-TCP traffic based on the first packet received.

### -field FWPS_LAYER_ALE_AUTH_RECV_ACCEPT_V6_DISCARD

This filtering layer allows for processing accept requests for incoming TCP connections that have been discarded, as well as processing authorizations for incoming non-TCP traffic that have been discarded.

### -field FWPS_LAYER_ALE_AUTH_CONNECT_V4

This filtering layer allows for authorizing connect requests for outgoing TCP connections, as well as authorizing outgoing non-TCP traffic based on the first packet sent.

### -field FWPS_LAYER_ALE_AUTH_CONNECT_V4_DISCARD

This filtering layer allows for processing connect requests for outgoing TCP connections that have been discarded, as well as processing authorizations for outgoing non-TCP traffic that have been discarded.

### -field FWPS_LAYER_ALE_AUTH_CONNECT_V6

This filtering layer allows for authorizing connect requests for outgoing TCP connections, as well as authorizing outgoing non-TCP traffic based on the first packet sent.

### -field FWPS_LAYER_ALE_AUTH_CONNECT_V6_DISCARD

This filtering layer allows for processing connect requests for outgoing TCP connections that have been discarded, as well as processing authorizations for outgoing non-TCP traffic that have been discarded.

### -field FWPS_LAYER_ALE_FLOW_ESTABLISHED_V4

This filtering layer allows for notification of when a TCP connection has been established, or when non-TCP traffic has been authorized.

### -field FWPS_LAYER_ALE_FLOW_ESTABLISHED_V4_DISCARD

This filtering layer allows for processing when an established TCP connection has been discarded at the flow established layer, as well as when authorized non-TCP traffic has been discarded at the flow established layer.

### -field FWPS_LAYER_ALE_FLOW_ESTABLISHED_V6

This filtering layer allows for notification of when a TCP connection has been established, or when non-TCP traffic has been authorized.

### -field FWPS_LAYER_ALE_FLOW_ESTABLISHED_V6_DISCARD

This filtering layer allows for processing when an established TCP connection has been discarded at the flow established layer, as well as when authorized non-TCP traffic has been discarded at the flow established layer.

### -field FWPS_LAYER_INBOUND_MAC_FRAME_ETHERNET

This filtering layer allows for inspecting the MAC frame data at the inbound lower (to the NDIS protocol driver) layer. Note: Available only on Windows 8 and later.

### -field FWPS_LAYER_OUTBOUND_MAC_FRAME_ETHERNET

This filtering layer allows for inspecting the MAC frame data at the outbound upper (to the NDIS protocol driver) layer. Note: Available only on Windows 8 and later.

### -field FWPS_LAYER_RESERVED1_V4

This filtering layer is not supported.

### -field FWPS_LAYER_RESERVED1_V6

This filtering layer is not supported.

### -field FWPS_LAYER_NAME_RESOLUTION_CACHE_V4

This filtering layer allows for querying the names recently resolved by the system.

### -field FWPS_LAYER_NAME_RESOLUTION_CACHE_V6

This filtering layer allows for querying the names recently resolved by the system.

### -field FWPS_LAYER_ALE_RESOURCE_RELEASE_V4

This filtering layer is used as an opportunity to reclaim resources allocated by the callout driver in any of the ALE_RESOURCE_ASSIGNMENT layers.

### -field FWPS_LAYER_ALE_RESOURCE_RELEASE_V6

This filtering layer is used as an opportunity to reclaim resources allocated by the callout driver in any of the ALE_RESOURCE_ASSIGNMENT layers.

### -field FWPS_LAYER_ALE_ENDPOINT_CLOSURE_V4

This filtering layer is used as an opportunity to reclaim resources allocated by the callout driver in any of the ALE_AUTH_CONNECT or ALE_AUTH_RECV_ACCEPT layers.

### -field FWPS_LAYER_ALE_ENDPOINT_CLOSURE_V6

This filtering layer is used as an opportunity to reclaim resources allocated by the callout driver in any of the ALE_AUTH_CONNECT or ALE_AUTH_RECV_ACCEPT layers.

### -field FWPS_LAYER_ALE_CONNECT_REDIRECT_V4

This filtering layer allows for the redirecting of connect requests to a different IPV4/ IPV6 address and TCP/UDP port.

### -field FWPS_LAYER_ALE_CONNECT_REDIRECT_V6

This filtering layer allows for the redirecting of connect requests to a different IPV4/ IPV6 address and TCP/UDP port.

### -field FWPS_LAYER_ALE_BIND_REDIRECT_V4

This filtering layer allows for the redirecting of bind requests to a different local IPV4/ IPV6 address and/or local TCP/UDP port.

### -field FWPS_LAYER_ALE_BIND_REDIRECT_V6

This filtering layer allows for the redirecting of bind requests to a different local IPV4/ IPV6 address and/or local TCP/UDP port.

### -field FWPS_LAYER_STREAM_PACKET_V4

This filtering layer allows for inspection of network data on a per-TCP packet basis, including handshake and flow control exchanges. At the stream packet layer, the network data is bidirectional.

### -field FWPS_LAYER_STREAM_PACKET_V6

This filtering layer allows for inspection of network data on a per-TCP packet basis, including handshake and flow control exchanges. At the stream packet layer, the network data is bidirectional.

### -field FWPS_LAYER_INGRESS_VSWITCH_ETHERNET

This filtering layer allows for inspecting the ingress 802.3 data of the Hyper-V extensible switch. Note: Available only on Windows 8 and later.

### -field FWPS_LAYER_EGRESS_VSWITCH_ETHERNET

This filtering layer allows for inspecting the egress 802.3 data of the Hyper-V extensible switch. Note: Available only on Windows 8 and later.

### -field FWPS_LAYER_INGRESS_VSWITCH_TRANSPORT_V4

This filtering layer allows for inspecting the ingress transport data of the Hyper-V extensible switch. Note: Available only on Windows 8 and later.

### -field FWPS_LAYER_INGRESS_VSWITCH_TRANSPORT_V6

This filtering layer allows for inspecting the ingress transport data of the Hyper-V extensible switch. Note: Available only on Windows 8 and later.

### -field FWPS_LAYER_EGRESS_VSWITCH_TRANSPORT_V4

This filtering layer allows for inspecting the egress transport data of the Hyper-V extensible switch. Note: Available only on Windows 8 and later.

### -field FWPS_LAYER_EGRESS_VSWITCH_TRANSPORT_V6

This filtering layer allows for inspecting the egress transport data of the Hyper-V extensible switch. Note: Available only on Windows 8 and later.

### -field FWPS_LAYER_INBOUND_TRANSPORT_FAST

TBD

### -field FWPS_LAYER_OUTBOUND_TRANSPORT_FAST

TBD

### -field FWPS_LAYER_INBOUND_MAC_FRAME_NATIVE_FAST

This filtering layer allows for inspecting the MAC frame data at the inbound lower (to the NDIS miniport driver) layer. Note: Available only on Windows 8 and later.

### -field FWPS_LAYER_OUTBOUND_MAC_FRAME_NATIVE_FAST

This filtering layer allows for inspecting the MAC frame data at the outbound lower (to the NDIS miniport driver) layer. Note: Available only on Windows 8 and later.

### -field FWPS_LAYER_INBOUND_RESERVED2

Reserved for system use.

### -field FWPS_LAYER_RESERVED_LAYER_9

Reserved for system use.

### -field FWPS_LAYER_RESERVED_LAYER_10

Reserved for system use.

### -field FWPS_LAYER_OUTBOUND_NETWORK_CONNECTION_POLICY_V4

This filtering layer is where a WFP filter driver can inspect an outgoing IPv4 connection, and read/write the routing policy that was configured for this connection. See [FwpmConnectionPolicyAdd0](/windows/win32/api/fwpmu/nf-fwpmu-fwpmconnectionpolicyadd0).

### -field FWPS_LAYER_OUTBOUND_NETWORK_CONNECTION_POLICY_V6

This filtering layer is where a WFP filter driver can inspect an outgoing IPv6 connection, and read/write the routing policy that was configured for this connection. See [FwpmConnectionPolicyAdd0](/windows/win32/api/fwpmu/nf-fwpmu-fwpmconnectionpolicyadd0).

### -field FWPS_LAYER_IPSEC_KM_DEMUX_V4

This filtering layer is used to determine which keying modules are invoked when the local system is the initiator. This is a user-mode filtering layer.

### -field FWPS_LAYER_IPSEC_KM_DEMUX_V6

This filtering layer is used to determine which keying modules are invoked when the local system is the initiator. This is a user-mode filtering layer.

### -field FWPS_LAYER_IPSEC_V4

This filtering layer allows the keying module to look up quick-mode policy information when negotiating quick-mode security associations. This is a user-mode filtering layer.

### -field FWPS_LAYER_IPSEC_V6

This filtering layer allows the keying module to look up quick-mode policy information when negotiating quick-mode security associations. This is a user-mode filtering layer.

### -field FWPS_LAYER_IKEEXT_V4

This filtering layer allows the IKE and authenticated IP modules to look up main-mode policy information when negotiating main-mode security associations. This is a user-mode filtering layer.

### -field FWPS_LAYER_IKEEXT_V6

This filtering layer allows the IKE and authenticated IP modules to look up main-mode policy information when negotiating main-mode security associations. This is a user-mode filtering layer.

### -field FWPS_LAYER_RPC_UM

This filtering layer allows for inspecting the RPC data fields that are available in user mode. This is a user-mode filtering layer.

### -field FWPS_LAYER_RPC_EPMAP

This filtering layer allows for inspecting the RPC data fields that are available in user mode during endpoint resolution. This is a user-mode filtering layer.

### -field FWPS_LAYER_RPC_EP_ADD

This filtering layer allows for inspecting the RPC data fields that are available in user mode when a new endpoint is added. This is a user-mode filtering layer.

### -field FWPS_LAYER_RPC_PROXY_CONN

This filtering layer allows for inspecting RpcProxy connection requests. This is a user-mode filtering layer.

### -field FWPS_LAYER_RPC_PROXY_IF

This filtering layer allows for inspecting the interface used for RpcProxy connections. This is a user-mode filtering layer.

### -field FWPS_LAYER_KM_AUTHORIZATION

This filtering layer allows for authorizing security association establishment.

### -field FWPS_BUILTIN_LAYER_MAX

Maximum range value for testing purposes.

## -remarks

Each run-time layer identifier has an associated run-time data field identifier that represents a set of constant values. These data field identifiers are declared as **FWPS_FIELDS_XXX** enumerations in `fwpsu.h`. For more info, see [Data field identifiers](/windows-hardware/drivers/network/data-field-identifiers).

The constants **FWPS_LAYER_INBOUND_IPPACKET_V4** through **FWPS_LAYER_ALE_FLOW_ESTABLISHED_V6** are for kernel-mode layers.

The types **FWPS_LAYER_KM_DEMUX_V4** through **FWPS_LAYER_RPC_EPMAP** are for user-mode layers.

## -see-also
