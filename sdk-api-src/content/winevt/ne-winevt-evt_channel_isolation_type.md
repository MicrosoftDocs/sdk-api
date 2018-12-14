---
UID: NE:winevt._EVT_CHANNEL_ISOLATION_TYPE
title: EVT_CHANNEL_ISOLATION_TYPE
author: windows-sdk-content
description: Defines the default access permissions to apply to the channel.
old-location: wes\evt_channel_isolation_type.htm
tech.root: wes
ms.assetid: 63b01c20-f413-451d-b34d-b2496ebf8181
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EVT_CHANNEL_ISOLATION_TYPE, EVT_CHANNEL_ISOLATION_TYPE enumeration [EventLog], EvtChannelIsolationTypeApplication, EvtChannelIsolationTypeCustom, EvtChannelIsolationTypeSystem, wes.evt_channel_isolation_type, winevt/EVT_CHANNEL_ISOLATION_TYPE, winevt/EvtChannelIsolationTypeApplication, winevt/EvtChannelIsolationTypeCustom, winevt/EvtChannelIsolationTypeSystem
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - EVT_CHANNEL_ISOLATION_TYPE
product: Windows
targetos: Windows
req.typenames: EVT_CHANNEL_ISOLATION_TYPE
req.redist: 
---

# EVT_CHANNEL_ISOLATION_TYPE enumeration


## -description


Defines the default access permissions to apply to the channel.


## -enum-fields




### -field EvtChannelIsolationTypeApplication

Provides open access to the channel.


### -field EvtChannelIsolationTypeSystem

Provides restricted access to the channel and is used by applications running under system service accounts, drivers, or an application that logs events that relate to the health of the computer.


### -field EvtChannelIsolationTypeCustom

Provides custom access to the channel.


## -see-also




<a href="https://msdn.microsoft.com/882506e5-222b-45c8-af4b-59db8baa1dae">ChannelType Complex Type</a>



<a href="https://msdn.microsoft.com/ea17cbf8-ab60-4bf9-b0a2-998814a50bd0">EVT_CHANNEL_CONFIG_PROPERTY_ID</a>



<a href="https://msdn.microsoft.com/0f84f51c-716e-4a70-b31c-2b4f40b3fd83">EvtGetChannelConfigProperty</a>



<a href="https://msdn.microsoft.com/f5f11bd9-5eb0-4afe-8c8b-57fa3850ad56">EvtSetChannelConfigProperty</a>
 

 

