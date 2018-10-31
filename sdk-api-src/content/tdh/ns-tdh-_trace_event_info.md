---
UID: NS:tdh._TRACE_EVENT_INFO
title: "_TRACE_EVENT_INFO"
author: windows-sdk-content
description: Defines the information about the event.
old-location: etw\trace_event_info_struct.htm
tech.root: etw
ms.assetid: ecf57a23-0dd2-4954-82ac-e92f651c226f
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*PTRACE_EVENT_INFO, TRACE_EVENT_INFO, TRACE_EVENT_INFO structure [ETW], _TRACE_EVENT_INFO, etw.trace_event_info_struct, tdh.trace_event_info_struct, tdh/TRACE_EVENT_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tdh.h
api_name:
 - TRACE_EVENT_INFO
product: Windows
targetos: Windows
req.typenames: TRACE_EVENT_INFO
req.redist: 
---

# _TRACE_EVENT_INFO structure


## -description


Defines the information about the event.


## -struct-fields




### -field ProviderGuid

A GUID that identifies the provider.


### -field EventGuid

A GUID that identifies the MOF class that contains the event. If the provider uses a manifest to define its events, this member is GUID_NULL.


### -field EventDescriptor

A <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a> structure that describes the event.


### -field DecodingSource

A <a href="https://msdn.microsoft.com/d6cd09da-9a67-4df2-9d82-370c559d3bfc">DECODING_SOURCE</a> enumeration value that identifies the source used to parse the event's data (for example, an instrumenation manifest of WMI MOF class).


### -field ProviderNameOffset

The offset from the beginning of this structure to a null-terminated Unicode string that contains the name of the provider.


### -field LevelNameOffset

The offset from the beginning of this structure to a null-terminated Unicode string that contains the name of the level. For possible names, see Remarks in <a href="https://msdn.microsoft.com/c71aedef-7c43-4343-9d6d-94eb45da49b9">LevelType</a>. 


### -field ChannelNameOffset

The offset from the beginning of this structure to a null-terminated Unicode string that contains the name of the channel. For possible names, see Remarks in <a href="https://msdn.microsoft.com/882506e5-222b-45c8-af4b-59db8baa1dae">ChannelType</a>. 


### -field KeywordsNameOffset

The offset from the beginning of this structure to a list of null-terminated Unicode strings that contains the names of the keywords. The list is terminated with two NULL characters. For possible names, see Remarks in <a href="https://msdn.microsoft.com/6bd41d4a-1d55-4cce-a1f8-136f749fde2a">KeywordType</a>. 


### -field TaskNameOffset

The offset from the beginning of this structure to a null-terminated Unicode string that contains the name of the task. For possible names, see Remarks in <a href="https://msdn.microsoft.com/d117636d-6363-43b6-ac5a-52234ac7c729">TaskType</a>. 


### -field OpcodeNameOffset

The offset from the beginning of this structure to a null-terminated Unicode string that contains the name of the operation. For possible names, see Remarks in <a href="https://msdn.microsoft.com/d97953df-669b-4c55-b1a8-925022b339b7">OpcodeType</a>. 


### -field EventMessageOffset

The offset from the beginning of this structure to a null-terminated Unicode string that contains the event message string.  The offset is zero if there is no message string. For information on message strings, see the <b>message</b> attribute for <a href="https://msdn.microsoft.com/09ea89c9-6618-4874-ac72-5ee19cde4040">EventDefinitionType</a>.

The message string can contain insert sequences, for example, Unable to connect to the %1 printer. The number of the insert sequence identifies the property in the event data to use for the substitution.


### -field ProviderMessageOffset

The offset from the beginning of this structure to a null-terminated Unicode string that contains the localized provider name. 


### -field BinaryXMLOffset

Reserved.


### -field BinaryXMLSize

Reserved.


### -field EventNameOffset

 


### -field ActivityIDNameOffset

The offset from the beginning of this structure to a null-terminated Unicode string that contains the property name of the activity identifier in the MOF class. Supported for classic ETW events only.


### -field EventAttributesOffset

 


### -field RelatedActivityIDNameOffset

The offset from the beginning of this structure to a null-terminated Unicode string that contains the property name of the related activity identifier in the MOF class. Supported for legacy ETW events only.


### -field PropertyCount

The number of elements in the <b>EventPropertyInfoArray</b> array. 


### -field TopLevelPropertyCount

The number of properties in the <b>EventPropertyInfoArray</b> array that are top-level properties. This number does not include members of structures. Top-level properties come before all member properties in the array.


### -field Flags

Reserved.


### -field Reserved

 


### -field Tags

A 28-bit value associated with the event metadata. This value can be used by the event provider to associate additional semantic data with an event for use by an event processing tool. For example, a tag value of 5 might indicate that the event contains debugging information. The semantics of any values in this field are defined by the event provider.


### -field EventPropertyInfoArray

An array of <a href="https://msdn.microsoft.com/06b82b31-1f0e-45d5-88ec-9b9835af10df">EVENT_PROPERTY_INFO</a> structures that provides information about each property of the event's user data.


## -remarks



The value of an offset is zero if the member is not defined. 




## -see-also




<a href="https://msdn.microsoft.com/882506e5-222b-45c8-af4b-59db8baa1dae">ChannelType</a>



<a href="https://msdn.microsoft.com/d6cd09da-9a67-4df2-9d82-370c559d3bfc">DECODING_SOURCE</a>



<a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/06b82b31-1f0e-45d5-88ec-9b9835af10df">EVENT_PROPERTY_INFO</a>



<a href="https://msdn.microsoft.com/09ea89c9-6618-4874-ac72-5ee19cde4040">EventDefinitionType</a>



<a href="https://msdn.microsoft.com/6bd41d4a-1d55-4cce-a1f8-136f749fde2a">KeywordType</a>



<a href="https://msdn.microsoft.com/c71aedef-7c43-4343-9d6d-94eb45da49b9">LevelType</a>



<a href="https://msdn.microsoft.com/d97953df-669b-4c55-b1a8-925022b339b7">OpcodeType</a>



<a href="https://msdn.microsoft.com/d117636d-6363-43b6-ac5a-52234ac7c729">TaskType</a>



<a href="https://msdn.microsoft.com/93A03E1D-4047-49F1-987B-FB7BE03E0483">TdhEnumerateManifestProviderEvents</a>



<a href="https://msdn.microsoft.com/81542550-79aa-4d67-a472-ac3ee3a3ce63">TdhGetEventInformation</a>



<a href="https://msdn.microsoft.com/71702F1F-1708-4CA2-9BFB-3D7332AB6129">TdhGetManifestEventInformation</a>
 

 

