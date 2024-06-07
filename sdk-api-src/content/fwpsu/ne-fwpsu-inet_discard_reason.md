---
UID: NE:fwpsu.INET_DISCARD_REASON
tech.root: fwp
title: INET_DISCARD_REASON
ms.date: 06/06/2024
targetos: Windows
description: Defines the possible reasons that data is discarded by one of the transport layers.
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
 - INET_DISCARD_REASON
 - PINET_DISCARD_REASON
f1_keywords:
 - INET_DISCARD_REASON
 - fwpsu/INET_DISCARD_REASON
 - PINET_DISCARD_REASON
 - fwpsu/PINET_DISCARD_REASON
dev_langs:
 - c++
helpviewer_keywords:
 - INET_DISCARD_REASON
---

## -description

Defines the possible reasons that data is discarded by one of the transport layers.

## -enum-fields

### -field InetDiscardSourceUnspecified:0

The outgoing packet's source address is unspecified.

### -field InetDiscardDestinationMulticast:1

The outgoing packet's destination address is an unspecified address, and the transport does not support multicast addresses.

### -field InetDiscardHeaderInvalid:2

The packet has an invalid header.

### -field InetDiscardChecksumInvalid:3

The packet's checksum did not match.

### -field InetDiscardEndpointNotFound:4

The intended endpoint for the packet could not be found.

### -field InetDiscardConnectedPath:5

The packet remote address does not match the remote address of a connected endpoint.

### -field InetDiscardSessionState:6

The packet cannot be delivered based on network layer information.

### -field InetDiscardReceiveInspection:7

The connection was closed due to a receive inspection failure.

### -field InetDiscardAckInvalid:8

The packet is an invalid ACK segment.

### -field InetDiscardExpectedSyn:9

A SYN packet was expected but not received.

### -field InetDiscardRst:10

The packet is an invalid RST segment.

### -field InetDiscardSynRcvdSyn:11

A TCP connection in SYN_RCVD state received another SYN segment.

### -field InetDiscardSimultaneousConnect:12

A TCP connection has encountered the simultaneous-connect condition.

### -field InetDiscardPawsFailed:13

A TCP PAWS check failed.

### -field InetDiscardLandAttack:14

The packet was detected as part of a LAND (Local Area Network Denial) attack,

### -field InetDiscardMissedReset:15

An SYN segment outside the receive window was received on a SYN_RCVD connection. An RST may have been missed.

### -field InetDiscardOutsideWindow:16

A TCP segment was outside the receive window.

### -field InetDiscardDuplicateSegment:17

A duplicate TCP segment was received.

### -field InetDiscardClosedWindow:18

The TCP receive window was closed.

### -field InetDiscardTcbRemoved:19

The TCP connection was closed.

### -field InetDiscardFinWait2:20

The TCP connection is closing.

### -field InetDiscardReassemblyConflict:21

A TCP data reassembly conflict was encountered on reception of a FIN segment.

### -field InetDiscardFinReceived:22

A FIN was already received on a TCP connection; no more data can be received.

### -field InetDiscardListenerInvalidFlags:23

A segment with invalid flags was received by a listening TCP socket.

### -field InetDiscardUrgentDeliveryAllocationFailure:24

There is insufficient memory for URG delivery on a TCP connection.

### -field InetDiscardTcbNotInTcbTable:25

A TCP connection was closed due to urgent delivery.

### -field InetDiscardTimeWaitTcbReceivedRstOutsideWindow:26

A **TIME_WAIT** state TCP connection received a RST segment outside the window.

### -field InetDiscardTimeWaitTcbSynAndOtherFlags:27

A **TIME_WAIT** state TCP connection received a segment with SYN and one or more incompatible flags.

### -field InetDiscardTimeWaitTcb:28

A **TIME_WAIT** state TCP connection received an invalid segment.

### -field InetDiscardSynAckWithFastopenCookieRequest:29

The packet, a SYN-ACK containing a request for a Fast Open cookie, was discarded.

### -field InetDiscardPauseAccept:30

This indicates the packet was discarded due to a pause in acceptance.

### -field InetDiscardSynAttack:31

The packet was discarded as part of mitigating a SYN flood attack.

### -field InetDiscardAcceptInspection:32

The packet was discarded during the acceptance inspection process.

### -field InetDiscardAcceptRedirection:33

The packet was discarded because it was subject to acceptance redirection.

### -field InetDiscardReasonMaxEnumValue

The maximum value for enumeration.

## -remarks

## -see-also
