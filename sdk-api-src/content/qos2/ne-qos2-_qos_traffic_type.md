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

# _QOS_TRAFFIC_TYPE enumeration


## -description


The <b>QOS_TRAFFIC_TYPE</b> enumeration defines the various traffic types.  Each flow has a single traffic type.  This allows the QOS subsystem to apply user-specified policies to each type.


## -enum-fields




### -field QOSTrafficTypeBestEffort

Flow traffic has the same network priority as regular traffic not associated with QOS.

This traffic type is the same as not specifying priority, and as a result,  the DSCP mark and 802.1p tag are not added to sent traffic.


### -field QOSTrafficTypeBackground

Flow traffic has a network priority lower than that of <b>QOSTrafficTypeBestEffort</b>.  This traffic type could be used for traffic of an application doing data backup.

Sent traffic will contain a DSCP mark with a value of 0x08 and an 802.1p tag with a value of 2.


### -field QOSTrafficTypeExcellentEffort

Flow traffic has a network priority higher than <b>QOSTrafficTypeBestEffort</b>, yet lower than <b>QOSTrafficTypeAudioVideo</b>.  This traffic type should be used for data traffic that is more important than normal end-user scenarios, such as email.

Sent traffic will contain a DSCP mark with value of 0x28 and 802.1p tag with a value of 5.



### -field QOSTrafficTypeAudioVideo

Flow traffic has a network priority higher than <b>QOSTrafficTypeExcellentEffort</b>, yet lower than <b>QOSTrafficTypeVoice</b>.  This traffic type should be used for A/V streaming scenarios such as MPEG2 streaming.

Sent traffic will contain a DSCP mark with a value of 0x28 and an 802.1p tag with a value of 5.



### -field QOSTrafficTypeVoice

Flow traffic has a network priority higher than <b>QOSTrafficTypeAudioVideo</b>, yet lower than <b>QOSTrafficTypeControl</b>.  This traffic type should be used for realtime voice streams such as VOIP.

Sent traffic will contain a DSCP mark with a value of 0x38 and an 802.1p tag with a value of 7.



### -field QOSTrafficTypeControl

Flow traffic has the highest network priority.  This traffic type should only be used for the most critical of data.  For example, it may be used for data carrying user inputs.

Sent traffic will contain a DSCP mark with a value of 0x38 and an 802.1p tag with a value of 7.



## -remarks



802.1p tags are  added to sent traffic only when the following conditions are met:<ul>
<li>
<a href="https://msdn.microsoft.com/44136284-b553-446e-a95f-1eac476a7143">QOSAddSocketToFlow</a> is called without the QOS_NON_ADAPTIVE_FLOW flag</li>
<li> The destination host is on the local link and not across a router</li>
<li>The qWAVE subsystem has determined that 802.1p tagged packets are not discarded by a network element on the end-to-end path
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/44136284-b553-446e-a95f-1eac476a7143">QOSAddSocketToFlow</a>



<a href="https://msdn.microsoft.com/b30e8887-4445-480d-aba8-79ec36384648">QOSSetFlow</a>



<a href="https://msdn.microsoft.com/022fde13-415e-49aa-8df4-472c4eadd6a0">Quality Windows Audio/Video Experience (qWAVE)</a>
 

 

