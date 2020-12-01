---
UID: NE:nldef._NL_NEIGHBOR_STATE
title: NL_NEIGHBOR_STATE (nldef.h)
description: The NL_NEIGHBOR_STATE enumeration type defines the state of a network layer neighbor IP address, as described in RFC 2461, section 7.3.2.
helpviewer_keywords: ["*PNL_NEIGHBOR_STATE","NL_NEIGHBOR_STATE","NL_NEIGHBOR_STATE enumeration [Network Drivers Starting with Windows Vista]","NlnsDelay","NlnsIncomplete","NlnsMaximum","NlnsPermanent","NlnsProbe","NlnsReachable","NlnsStale","NlnsUnreachable","PNL_NEIGHBOR_STATE","PNL_NEIGHBOR_STATE enumeration pointer [Network Drivers Starting with Windows Vista]","iphelper_dfada3d6-bdd8-4ce0-a7db-25882d0dac4a.xml","netvista.nl_neighbor_state","nldef/NL_NEIGHBOR_STATE","nldef/NlnsDelay","nldef/NlnsIncomplete","nldef/NlnsMaximum","nldef/NlnsPermanent","nldef/NlnsProbe","nldef/NlnsReachable","nldef/NlnsStale","nldef/NlnsUnreachable","nldef/PNL_NEIGHBOR_STATE"]
old-location: netvista\nl_neighbor_state.htm
tech.root: NetVista
ms.assetid: 7751011b-c473-4697-b311-62e3a6d9b1ae
ms.date: 12/05/2018
ms.keywords: '*PNL_NEIGHBOR_STATE, NL_NEIGHBOR_STATE, NL_NEIGHBOR_STATE enumeration [Network Drivers Starting with Windows Vista], NlnsDelay, NlnsIncomplete, NlnsMaximum, NlnsPermanent, NlnsProbe, NlnsReachable, NlnsStale, NlnsUnreachable, PNL_NEIGHBOR_STATE, PNL_NEIGHBOR_STATE enumeration pointer [Network Drivers Starting with Windows Vista], iphelper_dfada3d6-bdd8-4ce0-a7db-25882d0dac4a.xml, netvista.nl_neighbor_state, nldef/NL_NEIGHBOR_STATE, nldef/NlnsDelay, nldef/NlnsIncomplete, nldef/NlnsMaximum, nldef/NlnsPermanent, nldef/NlnsProbe, nldef/NlnsReachable, nldef/NlnsStale, nldef/NlnsUnreachable, nldef/PNL_NEIGHBOR_STATE'
req.header: nldef.h
req.include-header: Netioapi.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating   systems.
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
req.typenames: NL_NEIGHBOR_STATE, *PNL_NEIGHBOR_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NL_NEIGHBOR_STATE
 - nldef/_NL_NEIGHBOR_STATE
 - PNL_NEIGHBOR_STATE
 - nldef/PNL_NEIGHBOR_STATE
 - NL_NEIGHBOR_STATE
 - nldef/NL_NEIGHBOR_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - nldef.h
api_name:
 - NL_NEIGHBOR_STATE
---

# NL_NEIGHBOR_STATE enumeration


## -description

The NL_NEIGHBOR_STATE enumeration type defines the state of a network layer neighbor IP address, as
  described in RFC 2461, section 7.3.2.

## -enum-fields

### -field NlnsUnreachable

The IP address is unreachable.

### -field NlnsIncomplete

Address resolution is in progress and the link-layer address of the neighbor has not yet been
     determined. Specifically for IPv6, a Neighbor Solicitation message has been sent to the solicited-node multicast
     IP address of the target, but the corresponding neighbor advertisement has not yet been received.

### -field NlnsProbe

The neighbor is no longer known to be reachable, and probes are being sent to verify reachability.
     For IPv6, a reachability confirmation is actively being sought by regularly retransmitting unicast
     Neighbor Solicitation probes until a reachability confirmation is received.

### -field NlnsDelay

The neighbor is no longer known to be reachable, and traffic has recently been sent to the
     neighbor. However, instead of probing the neighbor immediately, sending probes is delayed for a short
     time to give upper layer protocols an opportunity to provide reachability confirmation. For IPv6, more
     time has elapsed than is specified in the 
     <b>ReachabilityTime.ReachableTime</b> member of the 
     <a href="/previous-versions/windows/hardware/drivers/ff559263(v=vs.85)">MIB_IPNET_ROW2</a> structure since the last
     positive confirmation was received that the forward path was functioning properly and a packet was sent.
     If no reachability confirmation is received within a period of time (used to delay the first probe) of
     entering the <b>NlnsDelay</b> state, a IPv6 Neighbor Solicitation (NS) message is sent, and the 
     <b>State</b> member of MIB_IPNET_ROW2 is changed to NlnsProbe.

### -field NlnsStale

The neighbor is no longer known to be reachable, but until traffic is sent to the neighbor, no
     attempt should be made to verify its reachability. For IPv6, more time has elapsed than is specified in
     the 
     <b>ReachabilityTime.ReachableTime</b> member of the 
     <a href="/previous-versions/windows/hardware/drivers/ff559263(v=vs.85)">MIB_IPNET_ROW2</a> structure since the last
     positive confirmation was received that the forward path was functioning properly. While the 
     <b>State</b> member of MIB_IPNET_ROW2 is NlnsStale, no action occurs until a packet is sent. The
     <b>NlnsStale</b> state is entered upon receiving an unsolicited neighbor discovery message that updates the
     cached IP address. Receipt of such a message does not confirm reachability, and entering the NlnsStale
     state insures reachability is verified quickly if the entry is actually being used. However,
     reachability is not actually verified until the entry is actually used.

### -field NlnsReachable

The neighbor is known to have been reachable recently (within tens of seconds ago). For IPv6, a
     positive confirmation was received within the time that is specified in the 
     <b>ReachabilityTime.ReachableTime</b> member of the 
     <a href="/previous-versions/windows/hardware/drivers/ff559263(v=vs.85)">MIB_IPNET_ROW2</a> structure that the forward
     path to the neighbor was functioning properly. While the 
     <b>State</b> member of MIB_IPNET_ROW2 is NlnsReachable, no special action occurs as packets are
     sent.

### -field NlnsPermanent

The IP address is a permanent address.

### -field NlnsMaximum

A maximum value for testing purposes.

## -remarks

For more information about RFC 2461, section 7.3.2, see the 
    <a href="https://www.ietf.org/rfc/rfc2461.txt">Neighbor Discovery for IP Version 6
    (IPv6)</a> memo from Network Working Group.

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff559263(v=vs.85)">MIB_IPNET_ROW2</a>