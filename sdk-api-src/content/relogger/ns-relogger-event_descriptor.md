---
UID: NS:relogger._EVENT_DESCRIPTOR
title: EVENT_DESCRIPTOR (relogger.h)
description: Contains metadata that defines the event.
helpviewer_keywords: ["*PEVENT_DESCRIPTOR","EVENT_DESCRIPTOR","EVENT_DESCRIPTOR structure [ETW]","PCEVENT_DESCRIPTOR","PCEVENT_DESCRIPTOR structure pointer [ETW]","PEVENT_DESCRIPTOR","PEVENT_DESCRIPTOR structure pointer [ETW]","_EVENT_DESCRIPTOR","base.event_descriptor","etw.event_descriptor","relogger/EVENT_DESCRIPTOR","relogger/PCEVENT_DESCRIPTOR","relogger/PEVENT_DESCRIPTOR"]
old-location: etw\event_descriptor.htm
tech.root: ETW
ms.assetid: 907e6c38-5eaa-49da-9dc0-d055dcc69d1a
ms.date: 12/05/2018
ms.keywords: '*PEVENT_DESCRIPTOR, EVENT_DESCRIPTOR, EVENT_DESCRIPTOR structure [ETW], PCEVENT_DESCRIPTOR, PCEVENT_DESCRIPTOR structure pointer [ETW], PEVENT_DESCRIPTOR, PEVENT_DESCRIPTOR structure pointer [ETW], _EVENT_DESCRIPTOR, base.event_descriptor, etw.event_descriptor, relogger/EVENT_DESCRIPTOR, relogger/PCEVENT_DESCRIPTOR, relogger/PEVENT_DESCRIPTOR'
req.header: relogger.h
req.include-header: Evntprov.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Relogger.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: EVENT_DESCRIPTOR, *PEVENT_DESCRIPTOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVENT_DESCRIPTOR
 - relogger/_EVENT_DESCRIPTOR
 - PEVENT_DESCRIPTOR
 - relogger/PEVENT_DESCRIPTOR
 - EVENT_DESCRIPTOR
 - relogger/EVENT_DESCRIPTOR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - relogger.h
api_name:
 - EVENT_DESCRIPTOR
---

# EVENT_DESCRIPTOR structure


## -description

The <b>EVENT_DESCRIPTOR</b> structure contains metadata that defines the event.

## -struct-fields

### -field Id

The event identifier.

### -field Version

The version of the event. The version indicates a revision to the event definition. You can use this member and the Id member to uniquely identify the event within the scope of a provider.

### -field Channel

The audience for the event (for example, administrator or developer).

### -field Level

The severity or level of detail included in the event (for example, informational or fatal).

### -field Opcode

A step in a sequence of operations being performed within the Task.

### -field Task

A larger unit of work within an application or component (is broader than the Opcode).

### -field Keyword

A bitmask that specifies a logical group of related events. Each bit corresponds to one group. An event may belong to one or more groups. The keyword can contain one or more provider-defined keywords, standard keywords, or both.

## -remarks

This structure represents an event defined in the manifest. You do not declare and populate this structure, instead you use the <a href="/windows/desktop/WES/message-compiler--mc-exe-">Message Compiler (MC.exe)</a> to generate a header file that declares and populates this structure for each event in the manifest. For details on writing the manifest and generating the header file, see <a href="/windows/desktop/WES/writing-an-instrumentation-manifest">Writing an Instrumentation Manifest</a> and <a href="/windows/desktop/WES/compiling-an-instrumentation-manifest">Compiling an Instrumentation Manifest</a>.

For details on the members of this structure, see the attributes of the <a href="/windows/desktop/WES/eventmanifestschema-eventdefinitiontype-complextype">EventDefinitionType</a> complex type. 

 You specify this structure when calling <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwrite">EventWrite</a> or <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer">EventWriteTransfer</a> to write the event. You can also use it when calling <a href="/windows/desktop/api/evntprov/nf-evntprov-eventenabled">EventEnabled</a> to determine if you should write the event.

This structure is also included in the <a href="/windows/desktop/api/evntcons/ns-evntcons-event_header">EVENT_HEADER</a> structure that is returned with the event record when you consume events using the <a href="/windows/desktop/ETW/eventrecordcallback">EventRecordCallback</a> callback. For MOF-defined events, the <b>Opcode</b> member contains the event type value. The <b>Version</b> and <b>Level</b> members contain the expected information.

## -see-also

<a href="/windows/desktop/api/evntcons/ns-evntcons-event_header">EVENT_HEADER</a>



<a href="/windows/desktop/api/evntprov/nf-evntprov-eventdesccreate">EventDescCreate</a>



<a href="/windows/desktop/api/evntprov/nf-evntprov-eventdescgetchannel">EventDescGetChannel</a>



<a href="/windows/desktop/api/evntprov/nf-evntprov-eventdescgetid">EventDescGetId</a>



<a href="/windows/desktop/api/evntprov/nf-evntprov-eventdescgetkeyword">EventDescGetKeyword</a>



<a href="/windows/desktop/api/evntprov/nf-evntprov-eventdescgetlevel">EventDescGetLevel</a>



<a href="/windows/desktop/api/evntprov/nf-evntprov-eventdescgetopcode">EventDescGetOpcode</a>



<a href="/windows/desktop/api/evntprov/nf-evntprov-eventdescgettask">EventDescGetTask</a>



<a href="/windows/desktop/api/evntprov/nf-evntprov-eventdescgetversion">EventDescGetVersion</a>



<a href="/windows/desktop/api/evntprov/nf-evntprov-eventdescorkeyword">EventDescOrKeyword</a>



<a href="/windows/desktop/api/evntprov/nf-evntprov-eventdescsetchannel">EventDescSetChannel</a>



<a href="/windows/desktop/api/evntprov/nf-evntprov-eventdescsetid">EventDescSetId</a>



<a href="/windows/desktop/api/evntprov/nf-evntprov-eventdescsetkeyword">EventDescSetKeyword</a>



<a href="/windows/desktop/api/evntprov/nf-evntprov-eventdescsetlevel">EventDescSetLevel</a>



<a href="/windows/desktop/api/evntprov/nf-evntprov-eventdescsetopcode">EventDescSetOpcode</a>



<a href="/windows/desktop/api/evntprov/nf-evntprov-eventdescsettask">EventDescSetTask</a>



<a href="/windows/desktop/api/evntprov/nf-evntprov-eventdescsetversion">EventDescSetVersion</a>



<a href="/windows/desktop/api/evntprov/nf-evntprov-eventdesczero">EventDescZero</a>



<a href="/windows/desktop/api/evntprov/nf-evntprov-eventenabled">EventEnabled</a>



<a href="/windows/desktop/api/evntprov/nf-evntprov-eventwrite">EventWrite</a>



<a href="/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer">EventWriteTransfer</a>



<a href="/windows/desktop/api/tdh/ns-tdh-provider_event_info">PROVIDER_EVENT_INFO</a>



<a href="/windows/desktop/api/tdh/nf-tdh-tdhenumeratemanifestproviderevents">TdhEnumerateManifestProviderEvents</a>



<a href="/windows/desktop/api/tdh/nf-tdh-tdhgetmanifesteventinformation">TdhGetManifestEventInformation</a>