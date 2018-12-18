---
UID: NS:fwpmtypes.FWPM_NET_EVENT_CLASSIFY_DROP1_
title: FWPM_NET_EVENT_CLASSIFY_DROP1
author: windows-sdk-content
description: Contains information that describes a layer drop failure.
old-location: fwp\fwpm_net_event_classify_drop1.htm
tech.root: fwp
ms.assetid: 2bc38e75-450e-4ad7-8954-ff339ae769f5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FWPM_NET_EVENT_CLASSIFY_DROP1, FWPM_NET_EVENT_CLASSIFY_DROP1 structure [Filtering], FWP_DIRECTION_FORWARD, FWP_DIRECTION_IN, FWP_DIRECTION_OUT, fwp.fwpm_net_event_classify_drop1, fwpmtypes/FWPM_NET_EVENT_CLASSIFY_DROP1
ms.topic: struct
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwpmtypes.h
api_name:
 - FWPM_NET_EVENT_CLASSIFY_DROP1
product: Windows
targetos: Windows
req.typenames: FWPM_NET_EVENT_CLASSIFY_DROP1
req.redist: 
---

# FWPM_NET_EVENT_CLASSIFY_DROP1 structure


## -description


The <b>FWPM_NET_EVENT_CLASSIFY_DROP1</b> structure contains information that describes a layer drop  failure.
<div class="alert"><b>Note</b>  <b>FWPM_NET_EVENT_CLASSIFY_DROP1</b> is the specific implementation of FWPM_NET_EVENT_CLASSIFY_DROP used in Windows 7. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 8, <a href="https://msdn.microsoft.com/1e018d6c-ed56-43f9-90b3-f2af42861617">FWPM_NET_EVENT_CLASSIFY_DROP2</a> is available. For Windows Vista, <a href="https://msdn.microsoft.com/9688ff75-292f-44f2-b3ed-41a9dd1ef918">FWPM_NET_EVENT_CLASSIFY_DROP0</a> is available.</div><div> </div>

## -struct-fields




### -field filterId

A LUID identifying the filter where the failure occurred.


### -field layerId

Indicates the identifier of the filtering layer where the failure occurred.  For more information, see <a href="https://msdn.microsoft.com/3b2daef1-558b-4e3a-a98a-f4dfa80a29c0">Filtering Layer Identifiers</a>.


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


## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

