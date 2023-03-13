---
UID: NE:winevt._EVT_SYSTEM_PROPERTY_ID
title: EVT_SYSTEM_PROPERTY_ID (winevt.h)
description: Defines the identifiers that identify the system-specific properties of an event.
helpviewer_keywords: ["EVT_SYSTEM_PROPERTY_ID","EVT_SYSTEM_PROPERTY_ID enumeration [EventLog]","EvtSystemActivityID","EvtSystemChannel","EvtSystemComputer","EvtSystemEventID","EvtSystemEventRecordId","EvtSystemKeywords","EvtSystemLevel","EvtSystemOpcode","EvtSystemProcessID","EvtSystemPropertyIdEND","EvtSystemProviderGuid","EvtSystemProviderName","EvtSystemQualifiers","EvtSystemRelatedActivityID","EvtSystemTask","EvtSystemThreadID","EvtSystemTimeCreated","EvtSystemUserID","EvtSystemVersion","wes.evt_system_property_id","winevt/EVT_SYSTEM_PROPERTY_ID","winevt/EvtSystemActivityID","winevt/EvtSystemChannel","winevt/EvtSystemComputer","winevt/EvtSystemEventID","winevt/EvtSystemEventRecordId","winevt/EvtSystemKeywords","winevt/EvtSystemLevel","winevt/EvtSystemOpcode","winevt/EvtSystemProcessID","winevt/EvtSystemPropertyIdEND","winevt/EvtSystemProviderGuid","winevt/EvtSystemProviderName","winevt/EvtSystemQualifiers","winevt/EvtSystemRelatedActivityID","winevt/EvtSystemTask","winevt/EvtSystemThreadID","winevt/EvtSystemTimeCreated","winevt/EvtSystemUserID","winevt/EvtSystemVersion"]
old-location: wes\evt_system_property_id.htm
tech.root: wes
ms.assetid: a77cfbac-9abd-41e1-8ce6-ba92de97eb64
ms.date: 12/05/2018
ms.keywords: EVT_SYSTEM_PROPERTY_ID, EVT_SYSTEM_PROPERTY_ID enumeration [EventLog], EvtSystemActivityID, EvtSystemChannel, EvtSystemComputer, EvtSystemEventID, EvtSystemEventRecordId, EvtSystemKeywords, EvtSystemLevel, EvtSystemOpcode, EvtSystemProcessID, EvtSystemPropertyIdEND, EvtSystemProviderGuid, EvtSystemProviderName, EvtSystemQualifiers, EvtSystemRelatedActivityID, EvtSystemTask, EvtSystemThreadID, EvtSystemTimeCreated, EvtSystemUserID, EvtSystemVersion, wes.evt_system_property_id, winevt/EVT_SYSTEM_PROPERTY_ID, winevt/EvtSystemActivityID, winevt/EvtSystemChannel, winevt/EvtSystemComputer, winevt/EvtSystemEventID, winevt/EvtSystemEventRecordId, winevt/EvtSystemKeywords, winevt/EvtSystemLevel, winevt/EvtSystemOpcode, winevt/EvtSystemProcessID, winevt/EvtSystemPropertyIdEND, winevt/EvtSystemProviderGuid, winevt/EvtSystemProviderName, winevt/EvtSystemQualifiers, winevt/EvtSystemRelatedActivityID, winevt/EvtSystemTask, winevt/EvtSystemThreadID, winevt/EvtSystemTimeCreated, winevt/EvtSystemUserID, winevt/EvtSystemVersion
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
req.typenames: EVT_SYSTEM_PROPERTY_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVT_SYSTEM_PROPERTY_ID
 - winevt/_EVT_SYSTEM_PROPERTY_ID
 - EVT_SYSTEM_PROPERTY_ID
 - winevt/EVT_SYSTEM_PROPERTY_ID
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
 - EVT_SYSTEM_PROPERTY_ID
---

# EVT_SYSTEM_PROPERTY_ID enumeration


## -description

Defines the identifiers that identify the system-specific properties of an event.

## -enum-fields

### -field EvtSystemProviderName:0

Identifies the <b>Name</b> attribute of the provider element. The variant type for this property is <b>EvtVarTypeString</b>.

### -field EvtSystemProviderGuid

Identifies the <b>Guid</b> attribute of the provider element. The variant type for this property is <b>EvtVarTypeGuid</b>.

### -field EvtSystemEventID

Identifies the <b>EventID</b> element. The variant type for this property is <b>EvtVarTypeUInt16</b>.

### -field EvtSystemQualifiers

Identifies the <b>Qualifiers</b> attribute of the EventID element. The variant type for this property is <b>EvtVarTypeUInt16</b>.

### -field EvtSystemLevel

Identifies the <b>Level</b> element. The variant type for this property is <b>EvtVarTypeUInt8</b>.

### -field EvtSystemTask

Identifies the <b>Task</b> element. The variant type for this property is <b>EvtVarTypeUInt16</b>.

### -field EvtSystemOpcode

Identifies the <b>Opcode</b> element. The variant type for this property is <b>EvtVarTypeUInt8</b>.

### -field EvtSystemKeywords

Identifies the <b>Keywords</b> element. The variant type for this property is <b>EvtVarTypeInt64</b>.

### -field EvtSystemTimeCreated

Identifies the <b>SystemTime</b> attribute of the TimeCreated element. The variant type for this property is <b>EvtVarTypeFileTime</b>.

### -field EvtSystemEventRecordId

Identifies the <b>EventRecordID</b> element. The variant type for this property is <b>EvtVarTypeUInt64</b>.

### -field EvtSystemActivityID

Identifies the <b>ActivityID</b> attribute of the Correlation element. The variant type for this property is <b>EvtVarTypeGuid</b>.

### -field EvtSystemRelatedActivityID

Identifies the <b>RelatedActivityID</b> attribute of the Correlation element. The variant type for this property is <b>EvtVarTypeGuid</b>.

### -field EvtSystemProcessID

Identifies the <b>ProcessID</b> attribute of the Execution element. The variant type for this property is <b>EvtVarTypeUInt32</b>.

### -field EvtSystemThreadID

Identifies the <b>ThreadID</b> attribute of the Execution element. The variant type for this property is <b>EvtVarTypeUInt32</b>.

### -field EvtSystemChannel

Identifies the <b>Channel</b> element. The variant type for this property is <b>EvtVarTypeString</b>.

### -field EvtSystemComputer

Identifies the <b>Computer</b> element. The variant type for this property is <b>EvtVarTypeString</b>.

### -field EvtSystemUserID

Identifies the <b>UserID</b> element. The variant type for this property is <b>EvtVarTypeSid</b>.

### -field EvtSystemVersion

Identifies the <b>Version</b> element. The variant type for this property is <b>EvtVarTypeUInt8</b>.

### -field EvtSystemPropertyIdEND

  This enumeration value marks the end of the enumeration values.

## -remarks

Before accessing these properties, check the variant type to ensure that it is not EvtVarTypeNULL; not all events will contain all system properties. For a list of system properties, see the <a href="/windows/desktop/WES/eventschema-schema">Event</a> schema.

## -see-also

<a href="/windows/desktop/api/winevt/ne-winevt-evt_render_context_flags">EVT_RENDER_CONTEXT_FLAGS</a>



<a href="/windows/desktop/api/winevt/ne-winevt-evt_render_flags">EVT_RENDER_FLAGS</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtcreaterendercontext">EvtCreateRenderContext</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtrender">EvtRender</a>
