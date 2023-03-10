---
UID: NS:tdh._PROVIDER_EVENT_INFO
title: PROVIDER_EVENT_INFO (tdh.h)
description: Defines an array of events in a provider manifest.
helpviewer_keywords: ["*PPROVIDER_EVENT_INFO","PPROVIDER_EVENT_INFO","PPROVIDER_EVENT_INFO structure pointer [ETW]","PROVIDER_EVENT_INFO","PROVIDER_EVENT_INFO structure [ETW]","etw.provider_event_info","tdh/PPROVIDER_EVENT_INFO","tdh/PROVIDER_EVENT_INFO"]
old-location: etw\provider_event_info.htm
tech.root: ETW
ms.assetid: CC392841-7436-4543-A846-FB5A27D9A014
ms.date: 12/05/2018
ms.keywords: '*PPROVIDER_EVENT_INFO, PPROVIDER_EVENT_INFO, PPROVIDER_EVENT_INFO structure pointer [ETW], PROVIDER_EVENT_INFO, PROVIDER_EVENT_INFO structure [ETW], etw.provider_event_info, tdh/PPROVIDER_EVENT_INFO, tdh/PROVIDER_EVENT_INFO'
req.header: tdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.typenames: PROVIDER_EVENT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROVIDER_EVENT_INFO
 - tdh/_PROVIDER_EVENT_INFO
 - PROVIDER_EVENT_INFO
 - tdh/PROVIDER_EVENT_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tdh.h
api_name:
 - PROVIDER_EVENT_INFO
---

# PROVIDER_EVENT_INFO structure


## -description

The <b>PROVIDER_EVENT_INFO</b> structure defines an array of events in a provider manifest.

## -struct-fields

### -field NumberOfEvents

The number of elements in the <b>EventDescriptorsArray</b> array.

### -field Reserved

Reserved.

### -field EventDescriptorsArray

An array of <a href="/windows/desktop/api/evntprov/ns-evntprov-event_descriptor">EVENT_DESCRIPTOR</a> structures that contain information about each event.

## -see-also
<a href="/windows/desktop/api/evntprov/ns-evntprov-event_descriptor">EVENT_DESCRIPTOR</a>



<a href="/windows/desktop/api/tdh/nf-tdh-tdhenumeratemanifestproviderevents">TdhEnumerateManifestProviderEvents</a>



<a href="/windows/desktop/api/tdh/nf-tdh-tdhgetmanifesteventinformation">TdhGetManifestEventInformation</a>