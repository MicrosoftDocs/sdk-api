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

# _EVT_CHANNEL_CLOCK_TYPE enumeration


## -description


Defines the values that specify the type of time stamp to use when logging events channel.


## -enum-fields




### -field EvtChannelClockTypeSystemTime

Uses the system time for the time stamp. The system time provides a low-resolution (10 milliseconds) time stamp but is comparatively less expensive to retrieve. System time is the default. 

Note that if the volume of events is high, the resolution for system time may not be fine enough to determine the sequence of events. If multiple events contain the same time stamp, the events may be delivered in the wrong order.


### -field EvtChannelClockTypeQPC

Uses the query performance counter (QPC) for the time stamp. The QPC time stamp provides a high-resolution (100 nanoseconds) time stamp but is comparatively more expensive to retrieve. 

You should use this resolution if you have high event rates or if the consumer merges events from different buffers.

Note that on older computers, the time stamp may not be accurate because the counter sometimes skips forward due to hardware errors.


## -see-also




<a href="https://msdn.microsoft.com/882506e5-222b-45c8-af4b-59db8baa1dae">ChannelType Complex Type</a>



<a href="https://msdn.microsoft.com/ea17cbf8-ab60-4bf9-b0a2-998814a50bd0">EVT_CHANNEL_CONFIG_PROPERTY_ID</a>



<a href="https://msdn.microsoft.com/0f84f51c-716e-4a70-b31c-2b4f40b3fd83">EvtGetChannelConfigProperty</a>



<a href="https://msdn.microsoft.com/f5f11bd9-5eb0-4afe-8c8b-57fa3850ad56">EvtSetChannelConfigProperty</a>
 

 

