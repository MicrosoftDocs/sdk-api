---
UID: NE:tdh._EVENT_FIELD_TYPE
title: EVENT_FIELD_TYPE (tdh.h)
description: Defines the provider information to retrieve.
helpviewer_keywords: ["EVENT_FIELD_TYPE","EVENT_FIELD_TYPE enumeration [ETW]","EventChannelInformation","EventInformationMax","EventKeywordInformation","EventLevelInformation","EventOpcodeInformation","EventTaskInformation","etw.event_field_type_enum","tdh.event_field_type_enum","tdh/EVENT_FIELD_TYPE","tdh/EventChannelInformation","tdh/EventInformationMax","tdh/EventKeywordInformation","tdh/EventLevelInformation","tdh/EventOpcodeInformation","tdh/EventTaskInformation"]
old-location: etw\event_field_type_enum.htm
tech.root: ETW
ms.assetid: da525556-e42b-41cb-b954-300f378477e5
ms.date: 12/05/2018
ms.keywords: EVENT_FIELD_TYPE, EVENT_FIELD_TYPE enumeration [ETW], EventChannelInformation, EventInformationMax, EventKeywordInformation, EventLevelInformation, EventOpcodeInformation, EventTaskInformation, etw.event_field_type_enum, tdh.event_field_type_enum, tdh/EVENT_FIELD_TYPE, tdh/EventChannelInformation, tdh/EventInformationMax, tdh/EventKeywordInformation, tdh/EventLevelInformation, tdh/EventOpcodeInformation, tdh/EventTaskInformation
req.header: tdh.h
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
req.typenames: EVENT_FIELD_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVENT_FIELD_TYPE
 - tdh/_EVENT_FIELD_TYPE
 - EVENT_FIELD_TYPE
 - tdh/EVENT_FIELD_TYPE
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
 - EVENT_FIELD_TYPE
---

# EVENT_FIELD_TYPE enumeration


## -description

Defines the provider information to retrieve.

## -enum-fields

### -field EventKeywordInformation:0

Keyword information defined in the manifest. For providers that define themselves using MOF classes, this type returns the enable flags values if the provider class includes the Flags property. For details, see the "Specifying level and enable flags values for a provider" section of <a href="/windows/desktop/ETW/event-tracing-mof-qualifiers">Event Tracing MOF Qualifiers</a>.

### -field EventLevelInformation

Level information defined in the manifest.

### -field EventChannelInformation

Channel information defined in the manifest.

### -field EventTaskInformation

Task information defined in the manifest.

### -field EventOpcodeInformation

Operation code information defined in the manifest.

### -field EventInformationMax

Reserved.

## -remarks

If you specify <b>EventOpcodeInformation</b> when calling <a href="/windows/desktop/api/tdh/nf-tdh-tdhqueryproviderfieldinformation">TdhQueryProviderFieldInformation</a>, you must specify the  <i>EventFieldValue</i> parameter as follows:

<ul>
<li>Bits 0 - 15 must contain the task value</li>
<li>Bits 16 - 23 must contain the opcode value</li>
</ul>
You can get the task and opcode values from <a href="/windows/desktop/api/evntprov/ns-evntprov-event_descriptor">EVENT_RECORD.EventHeader.EventDescriptor</a>.

WMI MOF class supports retrieving keyword and level information only.

## -see-also

<a href="/windows/desktop/api/tdh/ns-tdh-provider_field_infoarray">PROVIDER_FIELD_INFOARRAY</a>



<a href="/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfieldinformation">TdhEnumerateProviderFieldInformation</a>



<a href="/windows/desktop/api/tdh/nf-tdh-tdhqueryproviderfieldinformation">TdhQueryProviderFieldInformation</a>
