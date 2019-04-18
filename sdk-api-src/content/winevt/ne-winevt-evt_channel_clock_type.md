---
UID: NE:winevt._EVT_CHANNEL_CLOCK_TYPE
title: EVT_CHANNEL_CLOCK_TYPE (winevt.h)
author: windows-sdk-content
description: Defines the values that specify the type of time stamp to use when logging events channel.
old-location: wes\evt_channel_clock_type.htm
tech.root: wes
ms.assetid: 575a6667-b832-46e8-8704-0612e04b8669
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EVT_CHANNEL_CLOCK_TYPE, EVT_CHANNEL_CLOCK_TYPE enumeration [EventLog], EvtChannelClockTypeQPC, EvtChannelClockTypeSystemTime, wes.evt_channel_clock_type, winevt/EVT_CHANNEL_CLOCK_TYPE, winevt/EvtChannelClockTypeQPC, winevt/EvtChannelClockTypeSystemTime
ms.topic: enum
req.header: winevt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - WinEvt.h
api_name:
 - EVT_CHANNEL_CLOCK_TYPE
product: Windows
targetos: Windows
req.typenames: EVT_CHANNEL_CLOCK_TYPE
req.redist: 
ms.custom: 19H1
---

# EVT_CHANNEL_CLOCK_TYPE enumeration


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
 

 

