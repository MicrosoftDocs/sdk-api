---
UID: NS:ifdef._NDIS_INTERFACE_INFORMATION
title: "_NDIS_INTERFACE_INFORMATION"
author: windows-sdk-content
description: The NDIS_INTERFACE_INFORMATION structure provides information about a network interface for the OID_GEN_INTERFACE_INFO OID.
old-location: netvista\ndis_interface_information_str.htm
tech.root: netvista
ms.assetid: 9bfcd319-faff-4bae-8653-511154c19863
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: "*PNDIS_INTERFACE_INFORMATION, NDIS_INTERFACE_INFORMATION, NDIS_INTERFACE_INFORMATION structure [Network Drivers Starting with Windows Vista], PNDIS_INTERFACE_INFORMATION, PNDIS_INTERFACE_INFORMATION structure pointer [Network Drivers Starting with Windows Vista], _NDIS_INTERFACE_INFORMATION, ifdef/NDIS_INTERFACE_INFORMATION, ifdef/PNDIS_INTERFACE_INFORMATION, net_if_struct_ref_7b31aa66-635c-4992-b5d6-301c004bdc8a.xml, netvista.ndis_interface_information_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ifdef.h
api_name:
 - NDIS_INTERFACE_INFORMATION
product: Windows
targetos: Windows
req.typenames: NDIS_INTERFACE_INFORMATION, *PNDIS_INTERFACE_INFORMATION
req.redist: 
---

# _NDIS_INTERFACE_INFORMATION structure


## -description


The NDIS_INTERFACE_INFORMATION structure provides information about a network interface for the 
  <a href="netvista.oid_gen_interface_info">OID_GEN_INTERFACE_INFO</a> OID.


## -struct-fields




### -field ifOperStatus

The operational status of the interface. This status is the same as the value that the 
     <a href="netvista.oid_gen_operational_status">OID_GEN_OPERATIONAL_STATUS</a> OID
     returns.


### -field ifOperStatusFlags

The operational status flags of the interface. This field is reserved for the NDIS proxy interface
     provider. Other interface providers should set this member to zero.


### -field MediaConnectState

The 
     <a href="https://msdn.microsoft.com/5af5e050-4b2b-45a9-8549-3a3818d7b06f">NET_IF_MEDIA_CONNECT_STATE</a> connection state type.


### -field MediaDuplexState

The media duplex state of the interface. This state is the same as the value that the 
     <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/network/oid-gen-media-duplex-state">OID_GEN_MEDIA_DUPLEX_STATE</a> OID
     returns.


### -field ifMtu

The maximum transmission unit (MTU) of the interface. This MTU is the same as the value that the 
     <a href="netvista.oid_gen_maximum_frame_size">OID_GEN_MAXIMUM_FRAME_SIZE</a> OID
     returns.


### -field ifPromiscuousMode

A Boolean value that is <b>TRUE</b> if the interface is in promiscuous mode or <b>FALSE</b> if it is not. This
     value is the same as the value that 
     <a href="netvista.oid_gen_promiscuous_mode">OID_GEN_PROMISCUOUS_MODE</a> OID query
     returns.


### -field ifDeviceWakeUpEnable

A Boolean value that is <b>TRUE</b> if the interface supports wake-on-LAN capability and the capability is enabled, or <b>FALSE</b> if it does
     not.


### -field XmitLinkSpeed

The transmit link speed, in bytes per second, of the interface. This speed is the same as the
     value that an 
     <a href="netvista.oid_gen_xmit_link_speed">OID_GEN_XMIT_LINK_SPEED</a> OID query
     returns.


### -field RcvLinkSpeed

The receive link speed, in bytes per second, of the interface. This speed is the same as the value
     that an 
     <a href="netvista.oid_gen_rcv_link_speed">OID_GEN_RCV_LINK_SPEED</a> OID query
     returns.


### -field ifLastChange

The time that the interface entered its current operational state. This time is the same as the
     value that an 
     <a href="netvista.oid_gen_last_change">OID_GEN_LAST_CHANGE</a> OID query
     returns.


### -field ifCounterDiscontinuityTime

The time of the last discontinuity of the interface's counters. This time is the same as the value
     that an 
     <a href="netvista.oid_gen_discontinuity_time">OID_GEN_DISCONTINUITY_TIME</a> OID
     query returns.


### -field ifInUnknownProtos

The number of packets that were received through the interface and that were discarded because of
     an unknown or unsupported protocol. This number is the same as the value that an 
     <a href="netvista.oid_gen_unknown_protos">OID_GEN_UNKNOWN_PROTOS</a> OID query
     returns.


### -field ifInDiscards

The number of inbound packets that were discarded even though no errors had been detected to
     prevent them from being deliverable to a higher-layer protocol. This number is the same as the value
     that an 
     <a href="netvista.oid_gen_rcv_discards">OID_GEN_RCV_DISCARDS</a> OID query
     returns.


### -field ifInErrors

The number of inbound packets that contained errors that prevented them from being deliverable to
     a higher layer protocol. This number is the same as the value that an 
     <a href="netvista.oid_gen_rcv_error">OID_GEN_RCV_ERROR</a> OID query returns.


### -field ifHCInOctets

The total number of bytes that are received on this interface. This number is the same as the
     value that an 
     <a href="netvista.oid_gen_bytes_rcv">OID_GEN_BYTES_RCV</a> OID returns.


### -field ifHCInUcastPkts

The number of directed packets that are received without errors on the interface. This number is
     the same as the value that an 
     <a href="netvista.oid_gen_directed_frames_rcv">OID_GEN_DIRECTED_FRAMES_RCV</a> OID
     query returns.


### -field ifHCInMulticastPkts

The number of multicast/functional packets that are received without errors on the interface. This
     number is the same as the value that an 
     <a href="netvista.oid_gen_multicast_frames_rcv">OID_GEN_MULTICAST_FRAMES_RCV</a> OID
     query returns.


### -field ifHCInBroadcastPkts

The number of broadcast packets that are received without errors on the interface. This number is
     the same as the value that an 
     <a href="netvista.oid_gen_broadcast_frames_rcv">OID_GEN_BROADCAST_FRAMES_RCV</a> OID
     query returns.


### -field ifHCOutOctets

The number of bytes that are transmitted without errors on the interface. This number is the same
     as the value that an 
     <a href="netvista.oid_gen_bytes_xmit">OID_GEN_BYTES_XMIT</a> OID query
     returns.


### -field ifHCOutUcastPkts

The number of directed packets that are transmitted without errors on the interface. This number
     is the same as the value that an 
     <a href="netvista.oid_gen_directed_frames_xmit">OID_GEN_DIRECTED_FRAMES_XMIT</a> OID
     query returns.


### -field ifHCOutMulticastPkts

The number of multicast/functional packets that are transmitted without errors on the interface.
     This number is the same as the value that an 
     <a href="netvista.oid_gen_multicast_frames_xmit">OID_GEN_MULTICAST_FRAMES_XMIT</a> OID query returns.


### -field ifHCOutBroadcastPkts

The number of broadcast packets that are transmitted without errors on the interface. This number
     is the same as the value that an 
     <a href="netvista.oid_gen_broadcast_frames_xmit">OID_GEN_BROADCAST_FRAMES_XMIT</a> OID query returns.


### -field ifOutErrors

The number of packets that the interface fails to transmit. This number is the same as the value
     that an 
     <a href="netvista.oid_gen_xmit_error">OID_GEN_XMIT_ERROR</a> OID query
     returns.


### -field ifOutDiscards

The number of packets that the interface discards. This number is the same as the value that an 
     <a href="netvista.oid_gen_xmit_discards">OID_GEN_XMIT_DISCARDS</a> OID query
     returns.


### -field ifHCInUcastOctets

The number of bytes in directed packets that are received without errors. This count is the same
     value that 
     <a href="netvista.oid_gen_directed_bytes_rcv">OID_GEN_DIRECTED_BYTES_RCV</a> returns.


### -field ifHCInMulticastOctets

The number of bytes in multicast/functional packets that are received without errors. This count
     is the same value that 
     <a href="netvista.oid_gen_multicast_bytes_rcv">OID_GEN_MULTICAST_BYTES_RCV</a> returns.


### -field ifHCInBroadcastOctets

The number of bytes in broadcast packets that are received without errors. This count is the same
     value that 
     <a href="netvista.oid_gen_broadcast_bytes_rcv">OID_GEN_BROADCAST_BYTES_RCV</a> returns.


### -field ifHCOutUcastOctets

The number of bytes in directed packets that are transmitted without errors. This count is the
     same value that 
     <a href="netvista.oid_gen_directed_bytes_xmit">OID_GEN_DIRECTED_BYTES_XMIT</a> returns.


### -field ifHCOutMulticastOctets

The number of bytes in multicast/functional packets that are transmitted without errors. This
     count is the same value that 
     <a href="netvista.oid_gen_multicast_bytes_xmit">OID_GEN_MULTICAST_BYTES_XMIT</a> returns.


### -field ifHCOutBroadcastOctets

The number of bytes in broadcast packets that are transmitted without errors. This count is the
     same value that 
     <a href="netvista.oid_gen_broadcast_bytes_xmit">OID_GEN_BROADCAST_BYTES_XMIT</a> returns.


### -field CompartmentId

The compartment that the interface belongs to, if the interface provider can provide the ID of the
     compartment to which the interface belongs. Otherwise, it should return
     NET_IF_COMPARTMENT_ID_UNSPECIFIED. If the interface provider returns NET_IF_COMPARTMENT_ID_UNSPECIFIED
     for the compartment ID, NDIS will return the right compartment ID for this interface.


### -field SupportedStatistics

The supported statistics. For more information, see the 
     <b>SupportedStatistics</b> member of the 
     <a href="https://msdn.microsoft.com/5423d073-02a5-468b-b91e-713ac67a5253">NDIS_MINIPORT_ADAPTER_GENERAL_ATTRIBUTES</a> structure.


## -remarks



NDIS interface providers populate an NDIS_INTERFACE_INFORMATION structure in response to a query of
    the 
    <a href="netvista.oid_gen_interface_info">OID_GEN_INTERFACE_INFO</a> OID. This
    structure contains information that changes during the lifetime of the interface.

To register as an interface provider, an NDIS driver calls the 
    <a href="https://msdn.microsoft.com/1624426b-9e67-4aa2-83d8-f1e6fa484858">NdisIfRegisterProvider</a> function.




## -see-also




<a href="netvista.introduction_to_network_drivers">Introduction to Network Drivers</a>



<a href="https://msdn.microsoft.com/5423d073-02a5-468b-b91e-713ac67a5253">NDIS_MINIPORT_ADAPTER_GENERAL_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/5af5e050-4b2b-45a9-8549-3a3818d7b06f">NET_IF_MEDIA_CONNECT_STATE</a>



<a href="https://msdn.microsoft.com/1624426b-9e67-4aa2-83d8-f1e6fa484858">NdisIfRegisterProvider</a>



<a href="netvista.oid_gen_broadcast_bytes_rcv">OID_GEN_BROADCAST_BYTES_RCV</a>



<a href="netvista.oid_gen_broadcast_bytes_xmit">OID_GEN_BROADCAST_BYTES_XMIT</a>



<a href="netvista.oid_gen_broadcast_frames_rcv">OID_GEN_BROADCAST_FRAMES_RCV</a>



<a href="netvista.oid_gen_broadcast_frames_xmit">OID_GEN_BROADCAST_FRAMES_XMIT</a>



<a href="netvista.oid_gen_bytes_rcv">OID_GEN_BYTES_RCV</a>



<a href="netvista.oid_gen_bytes_xmit">OID_GEN_BYTES_XMIT</a>



<a href="netvista.oid_gen_directed_bytes_rcv">OID_GEN_DIRECTED_BYTES_RCV</a>



<a href="netvista.oid_gen_directed_bytes_xmit">OID_GEN_DIRECTED_BYTES_XMIT</a>



<a href="netvista.oid_gen_directed_frames_rcv">OID_GEN_DIRECTED_FRAMES_RCV</a>



<a href="netvista.oid_gen_directed_frames_xmit">OID_GEN_DIRECTED_FRAMES_XMIT</a>



<a href="netvista.oid_gen_discontinuity_time">OID_GEN_DISCONTINUITY_TIME</a>



<a href="netvista.oid_gen_interface_info">OID_GEN_INTERFACE_INFO</a>



<a href="netvista.oid_gen_last_change">OID_GEN_LAST_CHANGE</a>



<a href="netvista.oid_gen_maximum_frame_size">OID_GEN_MAXIMUM_FRAME_SIZE</a>



<a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/network/oid-gen-media-connect-status-ex">OID_GEN_MEDIA_CONNECT_STATUS_EX</a>



<a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/network/oid-gen-media-duplex-state">OID_GEN_MEDIA_DUPLEX_STATE</a>



<a href="netvista.oid_gen_multicast_bytes_rcv">OID_GEN_MULTICAST_BYTES_RCV</a>



<a href="netvista.oid_gen_multicast_bytes_xmit">OID_GEN_MULTICAST_BYTES_XMIT</a>



<a href="netvista.oid_gen_multicast_frames_rcv">OID_GEN_MULTICAST_FRAMES_RCV</a>



<a href="netvista.oid_gen_multicast_frames_xmit">OID_GEN_MULTICAST_FRAMES_XMIT</a>



<a href="netvista.oid_gen_operational_status">OID_GEN_OPERATIONAL_STATUS</a>



<a href="netvista.oid_gen_promiscuous_mode">OID_GEN_PROMISCUOUS_MODE</a>



<a href="netvista.oid_gen_rcv_discards">OID_GEN_RCV_DISCARDS</a>



<a href="netvista.oid_gen_rcv_error">OID_GEN_RCV_ERROR</a>



<a href="netvista.oid_gen_rcv_link_speed">OID_GEN_RCV_LINK_SPEED</a>



<a href="netvista.oid_gen_unknown_protos">OID_GEN_UNKNOWN_PROTOS</a>



<a href="netvista.oid_gen_xmit_discards">OID_GEN_XMIT_DISCARDS</a>



<a href="netvista.oid_gen_xmit_error">OID_GEN_XMIT_ERROR</a>



<a href="netvista.oid_gen_xmit_link_speed">OID_GEN_XMIT_LINK_SPEED</a>
 

 

