---
UID: NS:ifdef._NDIS_INTERFACE_INFORMATION
title: NDIS_INTERFACE_INFORMATION (ifdef.h)
description: The NDIS_INTERFACE_INFORMATION structure provides information about a network interface for the OID_GEN_INTERFACE_INFO OID.
helpviewer_keywords: ["*PNDIS_INTERFACE_INFORMATION","NDIS_INTERFACE_INFORMATION","NDIS_INTERFACE_INFORMATION structure [Network Drivers Starting with Windows Vista]","PNDIS_INTERFACE_INFORMATION","PNDIS_INTERFACE_INFORMATION structure pointer [Network Drivers Starting with Windows Vista]","ifdef/NDIS_INTERFACE_INFORMATION","ifdef/PNDIS_INTERFACE_INFORMATION","net_if_struct_ref_7b31aa66-635c-4992-b5d6-301c004bdc8a.xml","netvista.ndis_interface_information_str"]
old-location: netvista\ndis_interface_information_str.htm
tech.root: NetVista
ms.assetid: 9bfcd319-faff-4bae-8653-511154c19863
ms.date: 12/05/2018
ms.keywords: '*PNDIS_INTERFACE_INFORMATION, NDIS_INTERFACE_INFORMATION, NDIS_INTERFACE_INFORMATION structure [Network Drivers Starting with Windows Vista], PNDIS_INTERFACE_INFORMATION, PNDIS_INTERFACE_INFORMATION structure pointer [Network Drivers Starting with Windows Vista], ifdef/NDIS_INTERFACE_INFORMATION, ifdef/PNDIS_INTERFACE_INFORMATION, net_if_struct_ref_7b31aa66-635c-4992-b5d6-301c004bdc8a.xml, netvista.ndis_interface_information_str'
req.header: ifdef.h
req.include-header: Ndis.h
req.target-type: Windows
req.target-min-winverclnt: Supported for NDIS 6.0 drivers in Windows Vista.
req.target-min-winversvr: 
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
req.typenames: NDIS_INTERFACE_INFORMATION, *PNDIS_INTERFACE_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NDIS_INTERFACE_INFORMATION
 - ifdef/_NDIS_INTERFACE_INFORMATION
 - PNDIS_INTERFACE_INFORMATION
 - ifdef/PNDIS_INTERFACE_INFORMATION
 - NDIS_INTERFACE_INFORMATION
 - ifdef/NDIS_INTERFACE_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ifdef.h
api_name:
 - NDIS_INTERFACE_INFORMATION
---

# NDIS_INTERFACE_INFORMATION structure


## -description

The NDIS_INTERFACE_INFORMATION structure provides information about a network interface for the 
  <a href="/windows-hardware/drivers/network/oid-gen-interface-info">OID_GEN_INTERFACE_INFO</a> OID.

## -struct-fields

### -field ifOperStatus

The operational status of the interface. This status is the same as the value that the 
     <a href="/windows-hardware/drivers/network/oid-gen-operational-status">OID_GEN_OPERATIONAL_STATUS</a> OID
     returns.

### -field ifOperStatusFlags

The operational status flags of the interface. This field is reserved for the NDIS proxy interface
     provider. Other interface providers should set this member to zero.

### -field MediaConnectState

The 
     <a href="/windows/desktop/api/ifdef/ne-ifdef-net_if_media_connect_state">NET_IF_MEDIA_CONNECT_STATE</a> connection state type.

### -field MediaDuplexState

The media duplex state of the interface. This state is the same as the value that the 
     <a href="/windows-hardware/drivers/network/oid-gen-media-duplex-state">OID_GEN_MEDIA_DUPLEX_STATE</a> OID
     returns.

### -field ifMtu

The maximum transmission unit (MTU) of the interface. This MTU is the same as the value that the 
     <a href="/windows-hardware/drivers/network/oid-gen-maximum-frame-size">OID_GEN_MAXIMUM_FRAME_SIZE</a> OID
     returns.

### -field ifPromiscuousMode

A Boolean value that is <b>TRUE</b> if the interface is in promiscuous mode or <b>FALSE</b> if it is not. This
     value is the same as the value that 
     <a href="/windows-hardware/drivers/network/oid-gen-promiscuous-mode">OID_GEN_PROMISCUOUS_MODE</a> OID query
     returns.

### -field ifDeviceWakeUpEnable

A Boolean value that is <b>TRUE</b> if the interface supports wake-on-LAN capability and the capability is enabled, or <b>FALSE</b> if it does
     not.

### -field XmitLinkSpeed

The transmit link speed, in bytes per second, of the interface. This speed is the same as the
     value that an 
     <a href="/windows-hardware/drivers/network/oid-gen-xmit-link-speed">OID_GEN_XMIT_LINK_SPEED</a> OID query
     returns.

### -field RcvLinkSpeed

The receive link speed, in bytes per second, of the interface. This speed is the same as the value
     that an 
     <a href="/windows-hardware/drivers/network/oid-gen-rcv-link-speed">OID_GEN_RCV_LINK_SPEED</a> OID query
     returns.

### -field ifLastChange

The time that the interface entered its current operational state. This time is the same as the
     value that an 
     <a href="/windows-hardware/drivers/network/oid-gen-last-change">OID_GEN_LAST_CHANGE</a> OID query
     returns.

### -field ifCounterDiscontinuityTime

The time of the last discontinuity of the interface's counters. This time is the same as the value
     that an 
     <a href="/windows-hardware/drivers/network/oid-gen-discontinuity-time">OID_GEN_DISCONTINUITY_TIME</a> OID
     query returns.

### -field ifInUnknownProtos

The number of packets that were received through the interface and that were discarded because of
     an unknown or unsupported protocol. This number is the same as the value that an 
     <a href="/windows-hardware/drivers/network/oid-gen-unknown-protos">OID_GEN_UNKNOWN_PROTOS</a> OID query
     returns.

### -field ifInDiscards

The number of inbound packets that were discarded even though no errors had been detected to
     prevent them from being deliverable to a higher-layer protocol. This number is the same as the value
     that an 
     <a href="/windows-hardware/drivers/network/oid-gen-rcv-discards">OID_GEN_RCV_DISCARDS</a> OID query
     returns.

### -field ifInErrors

The number of inbound packets that contained errors that prevented them from being deliverable to
     a higher layer protocol. This number is the same as the value that an 
     <a href="/windows-hardware/drivers/network/oid-gen-rcv-error">OID_GEN_RCV_ERROR</a> OID query returns.

### -field ifHCInOctets

The total number of bytes that are received on this interface. This number is the same as the
     value that an 
     <a href="/windows-hardware/drivers/network/oid-gen-bytes-rcv">OID_GEN_BYTES_RCV</a> OID returns.

### -field ifHCInUcastPkts

The number of directed packets that are received without errors on the interface. This number is
     the same as the value that an 
     <a href="/windows-hardware/drivers/network/oid-gen-directed-frames-rcv">OID_GEN_DIRECTED_FRAMES_RCV</a> OID
     query returns.

### -field ifHCInMulticastPkts

The number of multicast/functional packets that are received without errors on the interface. This
     number is the same as the value that an 
     <a href="/windows-hardware/drivers/network/oid-gen-multicast-frames-rcv">OID_GEN_MULTICAST_FRAMES_RCV</a> OID
     query returns.

### -field ifHCInBroadcastPkts

The number of broadcast packets that are received without errors on the interface. This number is
     the same as the value that an 
     <a href="/windows-hardware/drivers/network/oid-gen-broadcast-frames-rcv">OID_GEN_BROADCAST_FRAMES_RCV</a> OID
     query returns.

### -field ifHCOutOctets

The number of bytes that are transmitted without errors on the interface. This number is the same
     as the value that an 
     <a href="/windows-hardware/drivers/network/oid-gen-bytes-xmit">OID_GEN_BYTES_XMIT</a> OID query
     returns.

### -field ifHCOutUcastPkts

The number of directed packets that are transmitted without errors on the interface. This number
     is the same as the value that an 
     <a href="/windows-hardware/drivers/network/oid-gen-directed-frames-xmit">OID_GEN_DIRECTED_FRAMES_XMIT</a> OID
     query returns.

### -field ifHCOutMulticastPkts

The number of multicast/functional packets that are transmitted without errors on the interface.
     This number is the same as the value that an 
     <a href="/windows-hardware/drivers/network/oid-gen-multicast-frames-xmit">OID_GEN_MULTICAST_FRAMES_XMIT</a> OID query returns.

### -field ifHCOutBroadcastPkts

The number of broadcast packets that are transmitted without errors on the interface. This number
     is the same as the value that an 
     <a href="/windows-hardware/drivers/network/oid-gen-broadcast-frames-xmit">OID_GEN_BROADCAST_FRAMES_XMIT</a> OID query returns.

### -field ifOutErrors

The number of packets that the interface fails to transmit. This number is the same as the value
     that an 
     <a href="/windows-hardware/drivers/network/oid-gen-xmit-error">OID_GEN_XMIT_ERROR</a> OID query
     returns.

### -field ifOutDiscards

The number of packets that the interface discards. This number is the same as the value that an 
     <a href="/windows-hardware/drivers/network/oid-gen-xmit-discards">OID_GEN_XMIT_DISCARDS</a> OID query
     returns.

### -field ifHCInUcastOctets

The number of bytes in directed packets that are received without errors. This count is the same
     value that 
     <a href="/windows-hardware/drivers/network/oid-gen-directed-bytes-rcv">OID_GEN_DIRECTED_BYTES_RCV</a> returns.

### -field ifHCInMulticastOctets

The number of bytes in multicast/functional packets that are received without errors. This count
     is the same value that 
     <a href="/windows-hardware/drivers/network/oid-gen-multicast-bytes-rcv">OID_GEN_MULTICAST_BYTES_RCV</a> returns.

### -field ifHCInBroadcastOctets

The number of bytes in broadcast packets that are received without errors. This count is the same
     value that 
     <a href="/windows-hardware/drivers/network/oid-gen-broadcast-bytes-rcv">OID_GEN_BROADCAST_BYTES_RCV</a> returns.

### -field ifHCOutUcastOctets

The number of bytes in directed packets that are transmitted without errors. This count is the
     same value that 
     <a href="/windows-hardware/drivers/network/oid-gen-directed-bytes-xmit">OID_GEN_DIRECTED_BYTES_XMIT</a> returns.

### -field ifHCOutMulticastOctets

The number of bytes in multicast/functional packets that are transmitted without errors. This
     count is the same value that 
     <a href="/windows-hardware/drivers/network/oid-gen-multicast-bytes-xmit">OID_GEN_MULTICAST_BYTES_XMIT</a> returns.

### -field ifHCOutBroadcastOctets

The number of bytes in broadcast packets that are transmitted without errors. This count is the
     same value that 
     <a href="/windows-hardware/drivers/network/oid-gen-broadcast-bytes-xmit">OID_GEN_BROADCAST_BYTES_XMIT</a> returns.

### -field CompartmentId

The compartment that the interface belongs to, if the interface provider can provide the ID of the
     compartment to which the interface belongs. Otherwise, it should return
     NET_IF_COMPARTMENT_ID_UNSPECIFIED. If the interface provider returns NET_IF_COMPARTMENT_ID_UNSPECIFIED
     for the compartment ID, NDIS will return the right compartment ID for this interface.

### -field SupportedStatistics

The supported statistics. For more information, see the 
     <b>SupportedStatistics</b> member of the 
     <a href="/windows-hardware/drivers/ddi/content/ndis/ns-ndis-_ndis_miniport_adapter_general_attributes">NDIS_MINIPORT_ADAPTER_GENERAL_ATTRIBUTES</a> structure.

## -remarks

NDIS interface providers populate an NDIS_INTERFACE_INFORMATION structure in response to a query of
    the 
    <a href="/windows-hardware/drivers/network/oid-gen-interface-info">OID_GEN_INTERFACE_INFO</a> OID. This
    structure contains information that changes during the lifetime of the interface.

To register as an interface provider, an NDIS driver calls the 
    <a href="/windows-hardware/drivers/ddi/content/ndis/nf-ndis-ndisifregisterprovider">NdisIfRegisterProvider</a> function.

## -see-also

<a href="/windows-hardware/drivers/network/introduction-to-network-drivers">Introduction to Network Drivers</a>



<a href="/windows-hardware/drivers/ddi/content/ndis/ns-ndis-_ndis_miniport_adapter_general_attributes">NDIS_MINIPORT_ADAPTER_GENERAL_ATTRIBUTES</a>



<a href="/windows/desktop/api/ifdef/ne-ifdef-net_if_media_connect_state">NET_IF_MEDIA_CONNECT_STATE</a>



<a href="/windows-hardware/drivers/ddi/content/ndis/nf-ndis-ndisifregisterprovider">NdisIfRegisterProvider</a>



<a href="/windows-hardware/drivers/network/oid-gen-broadcast-bytes-rcv">OID_GEN_BROADCAST_BYTES_RCV</a>



<a href="/windows-hardware/drivers/network/oid-gen-broadcast-bytes-xmit">OID_GEN_BROADCAST_BYTES_XMIT</a>



<a href="/windows-hardware/drivers/network/oid-gen-broadcast-frames-rcv">OID_GEN_BROADCAST_FRAMES_RCV</a>



<a href="/windows-hardware/drivers/network/oid-gen-broadcast-frames-xmit">OID_GEN_BROADCAST_FRAMES_XMIT</a>



<a href="/windows-hardware/drivers/network/oid-gen-bytes-rcv">OID_GEN_BYTES_RCV</a>



<a href="/windows-hardware/drivers/network/oid-gen-bytes-xmit">OID_GEN_BYTES_XMIT</a>



<a href="/windows-hardware/drivers/network/oid-gen-directed-bytes-rcv">OID_GEN_DIRECTED_BYTES_RCV</a>



<a href="/windows-hardware/drivers/network/oid-gen-directed-bytes-xmit">OID_GEN_DIRECTED_BYTES_XMIT</a>



<a href="/windows-hardware/drivers/network/oid-gen-directed-frames-rcv">OID_GEN_DIRECTED_FRAMES_RCV</a>



<a href="/windows-hardware/drivers/network/oid-gen-directed-frames-xmit">OID_GEN_DIRECTED_FRAMES_XMIT</a>



<a href="/windows-hardware/drivers/network/oid-gen-discontinuity-time">OID_GEN_DISCONTINUITY_TIME</a>



<a href="/windows-hardware/drivers/network/oid-gen-interface-info">OID_GEN_INTERFACE_INFO</a>



<a href="/windows-hardware/drivers/network/oid-gen-last-change">OID_GEN_LAST_CHANGE</a>



<a href="/windows-hardware/drivers/network/oid-gen-maximum-frame-size">OID_GEN_MAXIMUM_FRAME_SIZE</a>



<a href="/windows-hardware/drivers/network/oid-gen-media-connect-status-ex">OID_GEN_MEDIA_CONNECT_STATUS_EX</a>



<a href="/windows-hardware/drivers/network/oid-gen-media-duplex-state">OID_GEN_MEDIA_DUPLEX_STATE</a>



<a href="/windows-hardware/drivers/network/oid-gen-multicast-bytes-rcv">OID_GEN_MULTICAST_BYTES_RCV</a>



<a href="/windows-hardware/drivers/network/oid-gen-multicast-bytes-xmit">OID_GEN_MULTICAST_BYTES_XMIT</a>



<a href="/windows-hardware/drivers/network/oid-gen-multicast-frames-rcv">OID_GEN_MULTICAST_FRAMES_RCV</a>



<a href="/windows-hardware/drivers/network/oid-gen-multicast-frames-xmit">OID_GEN_MULTICAST_FRAMES_XMIT</a>



<a href="/windows-hardware/drivers/network/oid-gen-operational-status">OID_GEN_OPERATIONAL_STATUS</a>



<a href="/windows-hardware/drivers/network/oid-gen-promiscuous-mode">OID_GEN_PROMISCUOUS_MODE</a>



<a href="/windows-hardware/drivers/network/oid-gen-rcv-discards">OID_GEN_RCV_DISCARDS</a>



<a href="/windows-hardware/drivers/network/oid-gen-rcv-error">OID_GEN_RCV_ERROR</a>



<a href="/windows-hardware/drivers/network/oid-gen-rcv-link-speed">OID_GEN_RCV_LINK_SPEED</a>



<a href="/windows-hardware/drivers/network/oid-gen-unknown-protos">OID_GEN_UNKNOWN_PROTOS</a>



<a href="/windows-hardware/drivers/network/oid-gen-xmit-discards">OID_GEN_XMIT_DISCARDS</a>



<a href="/windows-hardware/drivers/network/oid-gen-xmit-error">OID_GEN_XMIT_ERROR</a>



<a href="/windows-hardware/drivers/network/oid-gen-xmit-link-speed">OID_GEN_XMIT_LINK_SPEED</a>