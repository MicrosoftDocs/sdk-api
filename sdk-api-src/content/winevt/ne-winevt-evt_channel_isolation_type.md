---
UID: NE:winevt._EVT_CHANNEL_ISOLATION_TYPE
title: EVT_CHANNEL_ISOLATION_TYPE (winevt.h)
description: Defines the default access permissions to apply to the channel.
helpviewer_keywords: ["EVT_CHANNEL_ISOLATION_TYPE","EVT_CHANNEL_ISOLATION_TYPE enumeration [EventLog]","EvtChannelIsolationTypeApplication","EvtChannelIsolationTypeCustom","EvtChannelIsolationTypeSystem","wes.evt_channel_isolation_type","winevt/EVT_CHANNEL_ISOLATION_TYPE","winevt/EvtChannelIsolationTypeApplication","winevt/EvtChannelIsolationTypeCustom","winevt/EvtChannelIsolationTypeSystem"]
old-location: wes\evt_channel_isolation_type.htm
tech.root: wes
ms.assetid: 63b01c20-f413-451d-b34d-b2496ebf8181
ms.date: 12/05/2018
ms.keywords: EVT_CHANNEL_ISOLATION_TYPE, EVT_CHANNEL_ISOLATION_TYPE enumeration [EventLog], EvtChannelIsolationTypeApplication, EvtChannelIsolationTypeCustom, EvtChannelIsolationTypeSystem, wes.evt_channel_isolation_type, winevt/EVT_CHANNEL_ISOLATION_TYPE, winevt/EvtChannelIsolationTypeApplication, winevt/EvtChannelIsolationTypeCustom, winevt/EvtChannelIsolationTypeSystem
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
req.typenames: EVT_CHANNEL_ISOLATION_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVT_CHANNEL_ISOLATION_TYPE
 - winevt/_EVT_CHANNEL_ISOLATION_TYPE
 - EVT_CHANNEL_ISOLATION_TYPE
 - winevt/EVT_CHANNEL_ISOLATION_TYPE
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
 - EVT_CHANNEL_ISOLATION_TYPE
---

# EVT_CHANNEL_ISOLATION_TYPE enumeration


## -description

Defines the default access permissions to apply to the channel.

## -enum-fields

### -field EvtChannelIsolationTypeApplication:0

Provides open access to the channel.

### -field EvtChannelIsolationTypeSystem

Provides restricted access to the channel and is used by applications running under system service accounts, drivers, or an application that logs events that relate to the health of the computer.

### -field EvtChannelIsolationTypeCustom

Provides custom access to the channel.

## -see-also

<a href="/windows/desktop/WES/eventmanifestschema-channeltype-complextype">ChannelType Complex Type</a>



<a href="/windows/desktop/api/winevt/ne-winevt-evt_channel_config_property_id">EVT_CHANNEL_CONFIG_PROPERTY_ID</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtgetchannelconfigproperty">EvtGetChannelConfigProperty</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtsetchannelconfigproperty">EvtSetChannelConfigProperty</a>
