---
UID: NE:winevt._EVT_CHANNEL_CLOCK_TYPE
title: EVT_CHANNEL_CLOCK_TYPE (winevt.h)
description: Defines the values that specify the type of time stamp to use when logging events channel.
helpviewer_keywords: ["EVT_CHANNEL_CLOCK_TYPE","EVT_CHANNEL_CLOCK_TYPE enumeration [EventLog]","EvtChannelClockTypeQPC","EvtChannelClockTypeSystemTime","wes.evt_channel_clock_type","winevt/EVT_CHANNEL_CLOCK_TYPE","winevt/EvtChannelClockTypeQPC","winevt/EvtChannelClockTypeSystemTime"]
old-location: wes\evt_channel_clock_type.htm
tech.root: wes
ms.assetid: 575a6667-b832-46e8-8704-0612e04b8669
ms.date: 12/05/2018
ms.keywords: EVT_CHANNEL_CLOCK_TYPE, EVT_CHANNEL_CLOCK_TYPE enumeration [EventLog], EvtChannelClockTypeQPC, EvtChannelClockTypeSystemTime, wes.evt_channel_clock_type, winevt/EVT_CHANNEL_CLOCK_TYPE, winevt/EvtChannelClockTypeQPC, winevt/EvtChannelClockTypeSystemTime
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
targetos: Windows
req.typenames: EVT_CHANNEL_CLOCK_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVT_CHANNEL_CLOCK_TYPE
 - winevt/_EVT_CHANNEL_CLOCK_TYPE
 - EVT_CHANNEL_CLOCK_TYPE
 - winevt/EVT_CHANNEL_CLOCK_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinEvt.h
api_name:
 - EVT_CHANNEL_CLOCK_TYPE
---

# EVT_CHANNEL_CLOCK_TYPE enumeration


## -description

Defines the values that specify the type of time stamp to use when logging events channel.

## -enum-fields

### -field EvtChannelClockTypeSystemTime:0

Uses the system time for the time stamp. The system time provides a low-resolution (10 milliseconds) time stamp but is comparatively less expensive to retrieve. System time is the default. 

Note that if the volume of events is high, the resolution for system time may not be fine enough to determine the sequence of events. If multiple events contain the same time stamp, the events may be delivered in the wrong order.

### -field EvtChannelClockTypeQPC

Uses the query performance counter (QPC) for the time stamp. The QPC time stamp provides a high-resolution (100 nanoseconds) time stamp but is comparatively more expensive to retrieve. 

You should use this resolution if you have high event rates or if the consumer merges events from different buffers.

Note that on older computers, the time stamp may not be accurate because the counter sometimes skips forward due to hardware errors.

## -see-also

<a href="/windows/desktop/WES/eventmanifestschema-channeltype-complextype">ChannelType Complex Type</a>



<a href="/windows/desktop/api/winevt/ne-winevt-evt_channel_config_property_id">EVT_CHANNEL_CONFIG_PROPERTY_ID</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtgetchannelconfigproperty">EvtGetChannelConfigProperty</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtsetchannelconfigproperty">EvtSetChannelConfigProperty</a>
