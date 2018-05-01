---
UID: NS:fwpmtypes.FWPM_NET_EVENT_CLASSIFY_DROP_MAC0_
title: FWPM_NET_EVENT_CLASSIFY_DROP_MAC0_
author: windows-driver-content
description: Contains information that describes a MAC layer drop failure.
old-location: fwp\fwpm_net_event_classify_drop_mac0.htm
old-project: FWP
ms.assetid: 750c2cfa-6799-492d-9e10-b4260541ada7
ms.author: windowsdriverdev
ms.date: 4/12/2018
ms.keywords: FWPM_NET_EVENT_CLASSIFY_DROP_MAC0, FWPM_NET_EVENT_CLASSIFY_DROP_MAC0 structure [Filtering], FWPM_NET_EVENT_CLASSIFY_DROP_MAC0_, FWP_DIRECTION_FORWARD, FWP_DIRECTION_IN, FWP_DIRECTION_OUT, fwp.fwpm_net_event_classify_drop_mac0, fwpmtypes/FWPM_NET_EVENT_CLASSIFY_DROP_MAC0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: FWPM_NET_EVENT_CLASSIFY_DROP_MAC0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	fwpmtypes.h
api_name:
-	FWPM_NET_EVENT_CLASSIFY_DROP_MAC0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FWPM_NET_EVENT_CLASSIFY_DROP_MAC0_ structure


## -description



    The <b>FWPM_NET_EVENT_CLASSIFY_DROP_MAC0</b> structure contains information that describes a MAC layer drop  failure.


## -struct-fields




### -field localMacAddr

The local MAC address.


### -field remoteMacAddr

The remote MAC address.


### -field mediaType

The media type of the NDIS port.


### -field ifType

The interface type, as defined by the Internet Assigned Names Authority (IANA). Possible values for the interface type are listed in the Ipifcons.h include file. 


### -field etherType

Indicates which protocol is encapsulated in the frame data. The values used for this field comes from the Ethernet V2 specification's numbering space.


### -field ndisPortNumber

The number assigned to the NDIS port.


### -field reserved

Reserved for internal use.


### -field vlanTag

The VLAN (802.1p/q) VID, CFI, and Priority fields marshaled into a 16-bit value. (See VLAN_TAG in netiodef.h.)


### -field ifLuid

The interface LUID corresponding to the network interface with which this packet is associated.


### -field filterId

The LUID identifying the filter where the failure occured.


### -field layerId

The identifier of the filtering layer where the failure occurred. For more information, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff549947">Filtering Layer Identifiers</a>



### -field reauthReason

Indicates the reason for reauthorizing a previously authorized connection. 


### -field originalProfile

Indicates the identifier of the profile to which  the  packet was received (or from which the packet was sent).


### -field currentProfile

Indicates the identifier of the profile where the packet was when the failure occurred.


### -field msFwpDirection

Indicates the direction of the packet transmission.

Possible values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FWP_DIRECTION_IN"></a><a id="fwp_direction_in"></a><dl>
<dt><b>FWP_DIRECTION_IN</b></dt>
</dl>
</td>
<td width="60%">
The packet is inbound.

0x00003900L

</td>
</tr>
<tr>
<td width="40%"><a id="FWP_DIRECTION_OUT"></a><a id="fwp_direction_out"></a><dl>
<dt><b>FWP_DIRECTION_OUT</b></dt>
</dl>
</td>
<td width="60%">
The packet is outbound.

0x00003901L

</td>
</tr>
<tr>
<td width="40%"><a id="FWP_DIRECTION_FORWARD"></a><a id="fwp_direction_forward"></a><dl>
<dt><b>FWP_DIRECTION_FORWARD</b></dt>
</dl>
</td>
<td width="60%">
The packet is traversing an interface which it must pass through on the way to its destination.

0x00003902L

</td>
</tr>
</table>
 


### -field isLoopback

Indicates whether the packet originated from (or was heading to) the loopback adapter.


### -field vSwitchId

GUID identifier of a vSwitch.


### -field vSwitchSourcePort

Transient source port of a packet within the vSwitch.


### -field vSwitchDestinationPort

Transient destination port of a packet within the vSwitch.


## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

