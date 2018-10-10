---
UID: NE:winevt._EVT_CHANNEL_SID_TYPE
title: "_EVT_CHANNEL_SID_TYPE"
author: windows-sdk-content
description: Defines the values that determine whether the event includes the security identifier (SID) of the principal that logged the event.
old-location: wes\evt_channel_sid_type.htm
tech.root: WES
ms.assetid: 7eadae8f-71b4-44de-ba66-0e460fee496c
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: EVT_CHANNEL_SID_TYPE, EVT_CHANNEL_SID_TYPE enumeration [EventLog], EvtChannelSidTypeNone, EvtChannelSidTypePublishing, _EVT_CHANNEL_SID_TYPE, wes.evt_channel_sid_type, winevt/EVT_CHANNEL_SID_TYPE, winevt/EvtChannelSidTypeNone, winevt/EvtChannelSidTypePublishing
ms.prod: windows
ms.technology: windows-sdk
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
 - EVT_CHANNEL_SID_TYPE
product: Windows
targetos: Windows
req.typenames: EVT_CHANNEL_SID_TYPE
req.redist: 
---

# _EVT_CHANNEL_SID_TYPE enumeration


## -description


Defines the values that determine whether the event includes the security identifier (SID) of the principal that logged the event.


## -enum-fields




### -field EvtChannelSidTypeNone

Do not include with the event the SID of the principal that logged the event.


### -field EvtChannelSidTypePublishing

Include with the event the SID of the principal that logged the event.


## -see-also




<a href="https://msdn.microsoft.com/4b3980f4-8652-4070-97c0-99cd1a9fc85a">ChannelPublishingType Complex Type</a>



<a href="https://msdn.microsoft.com/ea17cbf8-ab60-4bf9-b0a2-998814a50bd0">EVT_CHANNEL_CONFIG_PROPERTY_ID</a>



<a href="https://msdn.microsoft.com/0f84f51c-716e-4a70-b31c-2b4f40b3fd83">EvtGetChannelConfigProperty</a>
 

 

