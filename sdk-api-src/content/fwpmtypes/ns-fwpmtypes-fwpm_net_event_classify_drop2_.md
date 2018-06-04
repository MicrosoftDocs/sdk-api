---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# FWPM_NET_EVENT_CLASSIFY_DROP2_ structure


## -description


The <b>FWPM_NET_EVENT_CLASSIFY_DROP2</b> structure contains information that describes a layer drop  failure.
<div class="alert"><b>Note</b>  <b>FWPM_NET_EVENT_CLASSIFY_DROP2</b> is the specific implementation of FWPM_NET_EVENT_CLASSIFY_DROP used in Windows 8. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7, <a href="https://msdn.microsoft.com/2bc38e75-450e-4ad7-8954-ff339ae769f5">FWPM_NET_EVENT_CLASSIFY_DROP1</a> is available. For Windows Vista, <a href="https://msdn.microsoft.com/9688ff75-292f-44f2-b3ed-41a9dd1ef918">FWPM_NET_EVENT_CLASSIFY_DROP0</a> is available.</div><div> </div>

## -struct-fields




### -field filterId

A LUID identifying the filter where the failure occurred.


### -field layerId

Indicates the identifier of the filtering layer where the failure occurred.  For more information, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff549947">Filtering Layer Identifiers</a>.


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
 

 

