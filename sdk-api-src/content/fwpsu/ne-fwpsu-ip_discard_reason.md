---
UID: NE:fwpsu.IP_DISCARD_REASON
tech.root: fwp
title: IP_DISCARD_REASON
ms.date: 06/06/2024
targetos: Windows
description: Defines the possible reasons that data is discarded by one of the network layers.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: fwpsu.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
typedef_isUnnamed: true
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - fwpsu.h
api_name:
 - IP_DISCARD_REASON
 - PIP_DISCARD_REASON
f1_keywords:
 - IP_DISCARD_REASON
 - fwpsu/IP_DISCARD_REASON
 - PIP_DISCARD_REASON
 - fwpsu/PIP_DISCARD_REASON
dev_langs:
 - c++
helpviewer_keywords:
 - IP_DISCARD_REASON
---

## -description

Defines the possible reasons that data is discarded by one of the network layers.

## -enum-fields

### -field IpDiscardBadSourceAddress

The outgoing packet's source address is a multicast address, a broadcast address, or an IPv6 address that contains an embedded IPv4 loopback or unspecified address.

### -field IpDiscardNotLocallyDestined

The received packet's destination address doesn't exist on the system, and no appropriate forwarding interface exists.

### -field IpDiscardProtocolUnreachable

There's either no transport protocol handler for the received packet or the transport protocol handler refused to process the packet.

### -field IpDiscardPortUnreachable

There's no application that is receiving packets on the received packet's destination port.

### -field IpDiscardBadLength

A length field specified within the received packet is inconsistent with the packet's length.

### -field IpDiscardMalformedHeader

The received packet contains a recognized extension header or option whose contents are invalid.

### -field IpDiscardNoRoute

The received packet can't be forwarded to its destination address because the system's routing table doesn't contain a route to that destination.

### -field IpDiscardBeyondScope

The received packet can't be forwarded because the packet's incoming and outgoing network interfaces have different zone indexes for the packet's zone level.

### -field IpDiscardInspectionDrop

The packet was dropped during inspection due to failing security checks or protocol compliance issues.

### -field IpDiscardTooManyDecapsulations

The received packet cannot be forwarded to its destination address because there are too many decapsulations.

### -field IpDiscardAdministrativelyProhibited

The packet was discarded due to administrative policies prohibiting its transmission or receipt.

### -field IpDiscardBadChecksum

The packet was discarded because its checksum was incorrect, indicating potential data corruption.

### -field IpDiscardFirstFragmentIncomplete

The first fragment of the packet was incomplete, leading to the discard of the entire packet.

### -field IpDiscardHeaderNotContiguous

The packet's header wasn't contiguous in memory, causing it to be discarded.

### -field IpDiscardHeaderNotAligned

The packet header wasn't properly aligned, leading to its discard due to formatting issues.

### -field IpDiscardReceivePathMax

The packet was discarded as it exceeded the maximum length allowed on the receive path.

### -field IpDiscardHopLimitExceeded

The received packet's hop limit or time-to-live limit has been exceeded.

### -field IpDiscardAddressUnreachable

The outgoing packet can't be sent to the packet's destination address either because the destination doesn't exist or packets aren't allowed to be sent to that destination.

### -field IpDiscardRscPacket

The outgoing packet can't be sent because it is a receive-side coalesced (RSC) packet.

### -field IpDiscardSourceViolation

The packet was discarded because it violated source address validation checks.

### -field IpDiscardForwardPathMax

The packet exceeded the maximum path length for forwarding and was discarded.

### -field IpDiscardArbitrationUnhandled

The packet was discarded because it required arbitration that wasn't handled.

### -field IpDiscardInspectionAbsorb

The outgoing packet cannot be sent because WFP took ownership of the packet.

### -field IpDiscardDontFragmentMtuExceeded

The packet was discarded because it exceeded the MTU size and had the Don't Fragment bit set.

### -field IpDiscardBufferLengthExceeded

The packet was discarded because it exceeded the buffer length limitations.

### -field IpDiscardAddressResolutionTimeout

The packet was discarded due to a timeout in address resolution.

### -field IpDiscardAddressResolutionFailure

The packet was discarded because address resolution failed.

### -field IpDiscardIpsecFailure

The packet was discarded due to an IPsec processing failure.

### -field IpDiscardExtensionHeadersFailure

The packet was discarded because of a failure related to processing IPv6 extension headers.

### -field IpDiscardAllocationFailure

The packet was discarded due to a failure in allocating necessary resources.

### -field IpDiscardIpsnpiClientDrop

The packet was discarded by an IPSNPI client due to unspecified reasons.

### -field IpDiscardUnsupportedOffload

The packet was discarded because it required an unsupported offload operation.

### -field IpDiscardRoutingFailure

The packet was discarded due to a failure in routing.

### -field IpDiscardAncillaryDataFailure

The packet was discarded because of a failure related to ancillary data processing.

### -field IpDiscardRawDataFailure

The packet was discarded due to a failure in processing raw data.

### -field IpDiscardSessionStateFailure

The packet was discarded because of a failure related to session state management.

### -field IpDiscardIpsnpiAllocationFailure

The packet was discarded due to an allocation failure within the IPSNPI subsystem.

### -field IpDiscardIpsnpiModifiedButNotForwarded

The packet was modified by IPSNPI but not forwarded, leading to its discard.

### -field IpDiscardIpsnpiNoNextHop

The packet was discarded because no next hop could be determined in the IPSNPI subsystem.

### -field IpDiscardIpsnpiNoCompartment

The packet was discarded due to a missing compartment in the IPSNPI subsystem.

### -field IpDiscardIpsnpiNoInterface

The packet was discarded because no interface was found in the IPSNPI subsystem.

### -field IpDiscardIpsnpiNoSubInterface

The packet was discarded due to the absence of a sub-interface in the IPSNPI subsystem.

### -field IpDiscardIpsnpiInterfaceDisabled

The packet was discarded because the interface in the IPSNPI subsystem was disabled.

### -field IpDiscardIpsnpiSegmentationFailed

The packet was discarded due to a failure in segmentation within the IPSNPI subsystem.

### -field IpDiscardIpsnpiNoEthernetHeader

The packet was discarded because it lacked an Ethernet header in the IPSNPI subsystem.

### -field IpDiscardIpsnpiUnexpectedFragment

The packet was discarded because it was an unexpected fragment in the IPSNPI subsystem.

### -field IpDiscardIpsnpiUnsupportedInterfaceType

The packet was discarded due to an unsupported interface type in the IPSNPI subsystem.

### -field IpDiscardIpsnpiInvalidLsoInfo

The packet was discarded because of invalid Large Send Offload (LSO) information in the IPSNPI subsystem.

### -field IpDiscardIpsnpiInvalidUsoInfo

The packet was discarded due to invalid UDP Segmentation Offload (USO) information in the IPSNPI subsystem.

### -field IpDiscardInternalError

The packet was discarded due to an internal error within the system.

### -field IpDiscardAdministrativelyConfigured

The packet was discarded due to an administrative configuration that prevented its processing.

### -field IpDiscardBadOption

The packet was discarded because it contained a bad option or an option that couldn't be processed.

### -field IpDiscardLoopbackDisallowed

The packet was discarded because loopback was disallowed for its type or destination.

### -field IpDiscardSmallerScope

The packet was discarded because its scope was smaller than required for successful delivery.

### -field IpDiscardQueueFull

The packet was discarded because the processing queue was full.

### -field IpDiscardInterfaceDisabled

The packet was discarded because the interface it arrived on was disabled.

### -field IpDiscardNlClientDiscard

The packet was discarded by a Netlink client due to unspecified reasons.

### -field IpDiscardIpsnpiUroSegmentSizeExceedsMtu

The packet was discarded because the segment size for UDP RSC Offload (URO) exceeded the MTU in the IPSNPI subsystem.

### -field IpDiscardSwUsoFailure

The packet was discarded due to a UDP Segmentation Offload (USO) failure.

### -field IpDiscardMax

The maximum value for enumeration.

## -remarks

## -see-also
