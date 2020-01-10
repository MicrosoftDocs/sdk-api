---
UID: NE:winevt._EVT_CHANNEL_TYPE
title: EVT_CHANNEL_TYPE (winevt.h)
description: Defines the type of a channel.
old-location: wes\evt_channel_type.htm
tech.root: wes
ms.assetid: 5650dd28-b0ef-4d74-abc6-85ed2bd56b38
ms.date: 12/05/2018
ms.keywords: EVT_CHANNEL_TYPE, EVT_CHANNEL_TYPE enumeration [EventLog], EvtChannelTypeAdmin, EvtChannelTypeAnalytic, EvtChannelTypeDebug, EvtChannelTypeOperational, wes.evt_channel_type, winevt/EVT_CHANNEL_TYPE, winevt/EvtChannelTypeAdmin, winevt/EvtChannelTypeAnalytic, winevt/EvtChannelTypeDebug, winevt/EvtChannelTypeOperational
f1_keywords:
- winevt/EVT_CHANNEL_TYPE
dev_langs:
- c++
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
- EVT_CHANNEL_TYPE
targetos: Windows
req.typenames: EVT_CHANNEL_TYPE
req.redist: 
ms.custom: 19H1
---

# EVT_CHANNEL_TYPE enumeration


## -description


Defines the type of a channel.


## -enum-fields




### -field EvtChannelTypeAdmin

The channel's type is Admin.


### -field EvtChannelTypeOperational

The channel's type is Operational.


### -field EvtChannelTypeAnalytic

The channel's type is Analytic.


### -field EvtChannelTypeDebug

The channel's type is Debug.


## -remarks



For a description of each channel type, see the <b>type</b> attribute of the <a href="https://docs.microsoft.com/windows/desktop/WES/eventmanifestschema-channeltype-complextype">ChannelType</a> complex type.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WES/eventmanifestschema-channeltype-complextype">ChannelType Complex Type</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winevt/ne-winevt-evt_channel_config_property_id">EVT_CHANNEL_CONFIG_PROPERTY_ID</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winevt/nf-winevt-evtgetchannelconfigproperty">EvtGetChannelConfigProperty</a>
 

 

