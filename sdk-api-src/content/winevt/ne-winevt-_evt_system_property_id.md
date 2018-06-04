---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _EVT_SYSTEM_PROPERTY_ID enumeration


## -description


Defines the identifiers that identify the system-specific properties of an event.


## -enum-fields




### -field EvtSystemProviderName

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



Before accessing these properties, check the variant type to ensure that it is not EvtVarTypeNULL; not all events will contain all system properties. For a list of system properties, see the <a href="https://msdn.microsoft.com/36037697-b777-4e5c-99af-77964200a3e4">Event</a> schema.




## -see-also




<a href="https://msdn.microsoft.com/1c933266-28d9-4ef2-b156-eedf4ccb189b">EVT_RENDER_CONTEXT_FLAGS</a>



<a href="https://msdn.microsoft.com/e7206481-c734-425f-a2b6-fa0d9a2b66c1">EVT_RENDER_FLAGS</a>



<a href="https://msdn.microsoft.com/729cfd74-c158-463d-9247-ee2c75b259d4">EvtCreateRenderContext</a>



<a href="https://msdn.microsoft.com/521322b6-3424-4321-bcba-fa8dcdc05a76">EvtRender</a>
 

 

