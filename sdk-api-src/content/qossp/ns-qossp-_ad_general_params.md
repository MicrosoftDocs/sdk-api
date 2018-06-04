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

# _AD_GENERAL_PARAMS structure


## -description


The <b>AD_GENERAL_PARAMS</b> structure contains the General Characterization Parameters contained in the RSVP Adspec object.


## -struct-fields




### -field IntServAwareHopCount

Number of hops that conform to Integrated Services (INTSERV) requirements.


### -field PathBandwidthEstimate

Minimum bandwidth available from sender to receiver.


### -field MinimumLatency

Sum of the minimum latency of the packet forwarding process in routers, in milliseconds. Can be set to INDETERMINATE_LATENCY.


### -field PathMTU

Maximum Transmission Unit (MTU) for the end-to-end path between sender and receiver that will not incur packet fragmentation.


### -field Flags

Flags associated with the parameters. The following flag is supported:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AD_FLAG_BREAK_BIT"></a><a id="ad_flag_break_bit"></a><dl>
<dt><b>AD_FLAG_BREAK_BIT</b></dt>
</dl>
</td>
<td width="60%">
Indicates the existence of a network element in the data path that does not support QOS control services. When set in a specific service override, indicates QOS service was not supported on at least one hop.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/90fad5de-7105-4126-a6db-d4fb663e01f4">RSVP_ADSPEC</a>
 

 

