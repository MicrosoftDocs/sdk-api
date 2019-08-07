---
UID: NE:winevt._EVT_CHANNEL_SID_TYPE
title: EVT_CHANNEL_SID_TYPE (winevt.h)
author: windows-sdk-content
description: Defines the values that determine whether the event includes the security identifier (SID) of the principal that logged the event.
old-location: wes\evt_channel_sid_type.htm
tech.root: wes
ms.assetid: 7eadae8f-71b4-44de-ba66-0e460fee496c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EVT_CHANNEL_SID_TYPE, EVT_CHANNEL_SID_TYPE enumeration [EventLog], EvtChannelSidTypeNone, EvtChannelSidTypePublishing, wes.evt_channel_sid_type, winevt/EVT_CHANNEL_SID_TYPE, winevt/EvtChannelSidTypeNone, winevt/EvtChannelSidTypePublishing
ms.topic: enum
f1_keywords:
- winevt/EVT_CHANNEL_SID_TYPE
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
- EVT_CHANNEL_SID_TYPE
product: Windows
targetos: Windows
req.typenames: EVT_CHANNEL_SID_TYPE
req.redist: 
ms.custom: 19H1
---

# EVT_CHANNEL_SID_TYPE enumeration


## -description


Defines the values that determine whether the event includes the security identifier (SID) of the principal that logged the event.


## -enum-fields




### -field EvtChannelSidTypeNone

Do not include with the event the SID of the principal that logged the event.


### -field EvtChannelSidTypePublishing

Include with the event the SID of the principal that logged the event.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WES/eventmanifestschema-channelpublishingtype-complextype">ChannelPublishingType Complex Type</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winevt/ne-winevt-evt_channel_config_property_id">EVT_CHANNEL_CONFIG_PROPERTY_ID</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winevt/nf-winevt-evtgetchannelconfigproperty">EvtGetChannelConfigProperty</a>
 

 

