---
UID: NE:winevt._EVT_CHANNEL_SID_TYPE
title: EVT_CHANNEL_SID_TYPE (winevt.h)
description: Defines the values that determine whether the event includes the security identifier (SID) of the principal that logged the event.
helpviewer_keywords: ["EVT_CHANNEL_SID_TYPE","EVT_CHANNEL_SID_TYPE enumeration [EventLog]","EvtChannelSidTypeNone","EvtChannelSidTypePublishing","wes.evt_channel_sid_type","winevt/EVT_CHANNEL_SID_TYPE","winevt/EvtChannelSidTypeNone","winevt/EvtChannelSidTypePublishing"]
old-location: wes\evt_channel_sid_type.htm
tech.root: wes
ms.assetid: 7eadae8f-71b4-44de-ba66-0e460fee496c
ms.date: 12/05/2018
ms.keywords: EVT_CHANNEL_SID_TYPE, EVT_CHANNEL_SID_TYPE enumeration [EventLog], EvtChannelSidTypeNone, EvtChannelSidTypePublishing, wes.evt_channel_sid_type, winevt/EVT_CHANNEL_SID_TYPE, winevt/EvtChannelSidTypeNone, winevt/EvtChannelSidTypePublishing
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
req.typenames: EVT_CHANNEL_SID_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVT_CHANNEL_SID_TYPE
 - winevt/_EVT_CHANNEL_SID_TYPE
 - EVT_CHANNEL_SID_TYPE
 - winevt/EVT_CHANNEL_SID_TYPE
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
 - EVT_CHANNEL_SID_TYPE
---

# EVT_CHANNEL_SID_TYPE enumeration


## -description

Defines the values that determine whether the event includes the security identifier (SID) of the principal that logged the event.

## -enum-fields

### -field EvtChannelSidTypeNone:0

Do not include with the event the SID of the principal that logged the event.

### -field EvtChannelSidTypePublishing

Include with the event the SID of the principal that logged the event.

## -see-also

<a href="/windows/desktop/WES/eventmanifestschema-channelpublishingtype-complextype">ChannelPublishingType Complex Type</a>



<a href="/windows/desktop/api/winevt/ne-winevt-evt_channel_config_property_id">EVT_CHANNEL_CONFIG_PROPERTY_ID</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtgetchannelconfigproperty">EvtGetChannelConfigProperty</a>
