---
UID: NE:winevt._EVT_PUBLISHER_METADATA_PROPERTY_ID
title: "_EVT_PUBLISHER_METADATA_PROPERTY_ID"
author: windows-sdk-content
description: Defines the identifiers that identify the metadata properties of a provider.
old-location: wes\evt_publisher_metadata_property_id.htm
old-project: wes
ms.assetid: 10f4917d-68a1-4e90-ad7f-6bc19471ec38
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EVT_PUBLISHER_METADATA_PROPERTY_ID, EVT_PUBLISHER_METADATA_PROPERTY_ID enumeration [EventLog], EvtPublisherMetadataChannelReferenceFlags, EvtPublisherMetadataChannelReferenceID, EvtPublisherMetadataChannelReferenceIndex, EvtPublisherMetadataChannelReferenceMessageID, EvtPublisherMetadataChannelReferencePath, EvtPublisherMetadataChannelReferences, EvtPublisherMetadataHelpLink, EvtPublisherMetadataKeywordMessageID, EvtPublisherMetadataKeywordName, EvtPublisherMetadataKeywordValue, EvtPublisherMetadataKeywords, EvtPublisherMetadataLevelMessageID, EvtPublisherMetadataLevelName, EvtPublisherMetadataLevelValue, EvtPublisherMetadataLevels, EvtPublisherMetadataMessageFilePath, EvtPublisherMetadataOpcodeMessageID, EvtPublisherMetadataOpcodeName, EvtPublisherMetadataOpcodeValue, EvtPublisherMetadataOpcodes, EvtPublisherMetadataParameterFilePath, EvtPublisherMetadataPropertyIdEND, EvtPublisherMetadataPublisherGuid, EvtPublisherMetadataPublisherMessageID, EvtPublisherMetadataResourceFilePath, EvtPublisherMetadataTaskEventGuid, EvtPublisherMetadataTaskMessageID, EvtPublisherMetadataTaskName, EvtPublisherMetadataTaskValue, EvtPublisherMetadataTasks, _EVT_PUBLISHER_METADATA_PROPERTY_ID, wes.evt_publisher_metadata_property_id, winevt/EVT_PUBLISHER_METADATA_PROPERTY_ID, winevt/EvtPublisherMetadataChannelReferenceFlags, winevt/EvtPublisherMetadataChannelReferenceID, winevt/EvtPublisherMetadataChannelReferenceIndex, winevt/EvtPublisherMetadataChannelReferenceMessageID, winevt/EvtPublisherMetadataChannelReferencePath, winevt/EvtPublisherMetadataChannelReferences, winevt/EvtPublisherMetadataHelpLink, winevt/EvtPublisherMetadataKeywordMessageID, winevt/EvtPublisherMetadataKeywordName, winevt/EvtPublisherMetadataKeywordValue, winevt/EvtPublisherMetadataKeywords, winevt/EvtPublisherMetadataLevelMessageID, winevt/EvtPublisherMetadataLevelName, winevt/EvtPublisherMetadataLevelValue, winevt/EvtPublisherMetadataLevels, winevt/EvtPublisherMetadataMessageFilePath, winevt/EvtPublisherMetadataOpcodeMessageID, winevt/EvtPublisherMetadataOpcodeName, winevt/EvtPublisherMetadataOpcodeValue, winevt/EvtPublisherMetadataOpcodes, winevt/EvtPublisherMetadataParameterFilePath, winevt/EvtPublisherMetadataPropertyIdEND, winevt/EvtPublisherMetadataPublisherGuid, winevt/EvtPublisherMetadataPublisherMessageID, winevt/EvtPublisherMetadataResourceFilePath, winevt/EvtPublisherMetadataTaskEventGuid, winevt/EvtPublisherMetadataTaskMessageID, winevt/EvtPublisherMetadataTaskName, winevt/EvtPublisherMetadataTaskValue, winevt/EvtPublisherMetadataTasks
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: winevt.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: EVT_PUBLISHER_METADATA_PROPERTY_ID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinEvt.h
api_name:
 - EVT_PUBLISHER_METADATA_PROPERTY_ID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _EVT_PUBLISHER_METADATA_PROPERTY_ID enumeration


## -description


Defines the identifiers that identify the metadata properties of a provider.


## -enum-fields




### -field EvtPublisherMetadataPublisherGuid

Identifies the <b>guid</b> attribute of the provider. The variant type for this property is <b>EvtVarTypeGuid</b>.


### -field EvtPublisherMetadataResourceFilePath

Identifies the <b>resourceFilePath</b> attribute of the provider. The variant type for this property is <b>EvtVarTypeString</b>.


### -field EvtPublisherMetadataParameterFilePath

Identifies the <b>parameterFilePath</b> attribute of the provider. The variant type for this property is <b>EvtVarTypeString</b>.


### -field EvtPublisherMetadataMessageFilePath

Identifies the <b>messageFilePath</b> attribute of the provider. The variant type for this property is <b>EvtVarTypeString</b>.


### -field EvtPublisherMetadataHelpLink

Identifies the <b>helpLink</b> attribute of the provider. The variant type for this property is <b>EvtVarTypeString</b>.


### -field EvtPublisherMetadataPublisherMessageID

Identifies the <b>message</b> attribute of the provider. The metadata is the resource identifier assigned to the message string. To get the message string, call the <a href="https://msdn.microsoft.com/744fe166-b12c-49d4-ab13-b2ef6a6f9625">EvtFormatMessage</a> function. The variant type for this property is <b>EvtVarTypeUInt32</b>. If the provider does not specify a message, the value is –1.


### -field EvtPublisherMetadataChannelReferences

Identifies the <b>channels</b> child element of the provider. The variant type for this property is <b>EvtVarTypeEvtHandle</b>. To access the metadata of the channels that the provider defines or imports, use this handle when calling the <a href="https://msdn.microsoft.com/a522f0a8-6050-4082-acdf-e700ebfa7efc">EvtGetObjectArrayProperty</a> function. For details, see Remarks. When you are done with the handle, call the <a href="https://msdn.microsoft.com/c4b82d7b-508d-45bf-b990-04e90e846525">EvtClose</a> function.


### -field EvtPublisherMetadataChannelReferencePath

Identifies the <b>name</b> attribute of the channel. Use this identifier when calling the <a href="https://msdn.microsoft.com/a522f0a8-6050-4082-acdf-e700ebfa7efc">EvtGetObjectArrayProperty</a> function. For details, see Remarks. The variant type for this property is <b>EvtVarTypeString</b>.


### -field EvtPublisherMetadataChannelReferenceIndex

Identifies the zero-based index value of the channel in the list of channels. Use this identifier when calling the <a href="https://msdn.microsoft.com/a522f0a8-6050-4082-acdf-e700ebfa7efc">EvtGetObjectArrayProperty</a> function. For details, see Remarks. The variant type for this property is <b>EvtVarTypeUInt32</b>.


### -field EvtPublisherMetadataChannelReferenceID

Identifies the <b>value</b> attribute of the channel. Use this identifier when calling the <a href="https://msdn.microsoft.com/a522f0a8-6050-4082-acdf-e700ebfa7efc">EvtGetObjectArrayProperty</a> function. For details, see Remarks. The variant type for this property is <b>EvtVarTypeUInt32</b>.


### -field EvtPublisherMetadataChannelReferenceFlags

Identifies the flags value that indicates whether this channel is imported from another provider. The channel is imported if the EvtChannelReferenceImported flag value is set. Use this identifier when calling the <a href="https://msdn.microsoft.com/a522f0a8-6050-4082-acdf-e700ebfa7efc">EvtGetObjectArrayProperty</a> function. For details, see Remarks. The variant type for this property is <b>EvtVarTypeUInt32</b>.


### -field EvtPublisherMetadataChannelReferenceMessageID

Identifies the <b>message</b> attribute of the channel. Use this identifier when calling the <a href="https://msdn.microsoft.com/a522f0a8-6050-4082-acdf-e700ebfa7efc">EvtGetObjectArrayProperty</a> function. For details, see Remarks. The variant type for this property is <b>EvtVarTypeUInt32</b>. The property contains the resource identifier that is assigned to the message string. To get the message string, call the <a href="https://msdn.microsoft.com/744fe166-b12c-49d4-ab13-b2ef6a6f9625">EvtFormatMessage</a> function. If the channel does not specify a message, the value is –1.


### -field EvtPublisherMetadataLevels

Identifies the <b>levels</b> child element of the provider. The variant type for this property is <b>EvtVarTypeEvtHandle</b>. To access the metadata of the levels that the provider defines or references, use this handle when calling the <a href="https://msdn.microsoft.com/a522f0a8-6050-4082-acdf-e700ebfa7efc">EvtGetObjectArrayProperty</a> function. For details, see Remarks. When you are done with the handle, call the <a href="https://msdn.microsoft.com/c4b82d7b-508d-45bf-b990-04e90e846525">EvtClose</a> function.


### -field EvtPublisherMetadataLevelName

Identifies the <b>name</b> attribute of the level. Use this identifier when calling the <a href="https://msdn.microsoft.com/a522f0a8-6050-4082-acdf-e700ebfa7efc">EvtGetObjectArrayProperty</a> function. For details, see Remarks. The variant type for this property is <b>EvtVarTypeString</b>.


### -field EvtPublisherMetadataLevelValue

Identifies the <b>value</b> attribute of the level. Use this identifier when calling the <a href="https://msdn.microsoft.com/a522f0a8-6050-4082-acdf-e700ebfa7efc">EvtGetObjectArrayProperty</a> function. For details, see Remarks. The variant type for this property is <b>EvtVarTypeUInt32</b>.


### -field EvtPublisherMetadataLevelMessageID

Identifies the <b>message</b> attribute of the level. Use this identifier when calling the <a href="https://msdn.microsoft.com/a522f0a8-6050-4082-acdf-e700ebfa7efc">EvtGetObjectArrayProperty</a> function. For details, see Remarks. The variant type for this property is <b>EvtVarTypeUInt32</b>. The property contains the resource identifier that is assigned to the message string. To get the message string, call the <a href="https://msdn.microsoft.com/744fe166-b12c-49d4-ab13-b2ef6a6f9625">EvtFormatMessage</a> function. If the level does not specify a message, the value is –1.


### -field EvtPublisherMetadataTasks

Identifies the <b>tasks</b> child element of the provider. The variant type for this property is <b>EvtVarTypeEvtHandle</b>. To access the metadata of the tasks that the provider defines, use this handle when calling the <a href="https://msdn.microsoft.com/a522f0a8-6050-4082-acdf-e700ebfa7efc">EvtGetObjectArrayProperty</a> function. For details, see Remarks. When you are done with the handle, call the <a href="https://msdn.microsoft.com/c4b82d7b-508d-45bf-b990-04e90e846525">EvtClose</a> function.


### -field EvtPublisherMetadataTaskName

Identifies the <b>name</b> attribute of the task. Use this identifier when calling the <a href="https://msdn.microsoft.com/a522f0a8-6050-4082-acdf-e700ebfa7efc">EvtGetObjectArrayProperty</a> function. For details, see Remarks. The variant type for this property is <b>EvtVarTypeString</b>.


### -field EvtPublisherMetadataTaskEventGuid

Identifies the <b>eventGuid</b> attribute of the task. Use this identifier when calling the <a href="https://msdn.microsoft.com/a522f0a8-6050-4082-acdf-e700ebfa7efc">EvtGetObjectArrayProperty</a> function. For details, see Remarks. The variant type for this property is <b>EvtVarTypeString</b>.


### -field EvtPublisherMetadataTaskValue

Identifies the <b>value</b> attribute of the task. Use this identifier when calling the <a href="https://msdn.microsoft.com/a522f0a8-6050-4082-acdf-e700ebfa7efc">EvtGetObjectArrayProperty</a> function. For details, see Remarks. The variant type for this property is <b>EvtVarTypeUInt32</b>.


### -field EvtPublisherMetadataTaskMessageID

Identifies the <b>message</b> attribute of the task. Use this identifier when calling the <a href="https://msdn.microsoft.com/a522f0a8-6050-4082-acdf-e700ebfa7efc">EvtGetObjectArrayProperty</a> function. For details, see Remarks. The variant type for this property is <b>EvtVarTypeUInt32</b>. The property contains the resource identifier that is assigned to the message string. To get the message string, call the <a href="https://msdn.microsoft.com/744fe166-b12c-49d4-ab13-b2ef6a6f9625">EvtFormatMessage</a> function. If the task does not specify a message, the value is –1.


### -field EvtPublisherMetadataOpcodes

Identifies the <b>opcodes</b> child element of the provider. The variant type for this property is <b>EvtVarTypeEvtHandle</b>. To access the metadata of the opcodes that the provider defines or references, use this handle when calling the <a href="https://msdn.microsoft.com/a522f0a8-6050-4082-acdf-e700ebfa7efc">EvtGetObjectArrayProperty</a> function. For details, see Remarks. When you are done with the handle, call the <a href="https://msdn.microsoft.com/c4b82d7b-508d-45bf-b990-04e90e846525">EvtClose</a> function.


### -field EvtPublisherMetadataOpcodeName

Identifies the <b>name</b> attribute of the opcode. Use this identifier when calling the <a href="https://msdn.microsoft.com/a522f0a8-6050-4082-acdf-e700ebfa7efc">EvtGetObjectArrayProperty</a> function. For details, see Remarks. The variant type for this property is <b>EvtVarTypeString</b>.


### -field EvtPublisherMetadataOpcodeValue

Identifies the <b>value</b> attribute of the opcode. Use this identifier when calling the <a href="https://msdn.microsoft.com/a522f0a8-6050-4082-acdf-e700ebfa7efc">EvtGetObjectArrayProperty</a> function. For details, see Remarks. The variant type for this property is <b>EvtVarTypeUInt32</b>. The high word contains the opcode value and the low word contains the task to which it belongs. If the low word is zero, the opcode is defined globally; otherwise, the opcode is task specific. Use the low word value to determine the task that defines the opcode. 


### -field EvtPublisherMetadataOpcodeMessageID

Identifies the <b>message</b> attribute of the opcode. Use this identifier when calling the <a href="https://msdn.microsoft.com/a522f0a8-6050-4082-acdf-e700ebfa7efc">EvtGetObjectArrayProperty</a> function. For details, see Remarks. The variant type for this property is <b>EvtVarTypeUInt32</b>. The property contains the resource identifier that is assigned to the message string. To get the message string, call the <a href="https://msdn.microsoft.com/744fe166-b12c-49d4-ab13-b2ef6a6f9625">EvtFormatMessage</a> function. If the opcode does not specify a message, the value is –1.


### -field EvtPublisherMetadataKeywords

Identifies the <b>keywords</b> child element of the provider. The variant type for this property is <b>EvtVarTypeEvtHandle</b>. To access the metadata of the keywords that the provider defines, use this handle when calling the <a href="https://msdn.microsoft.com/a522f0a8-6050-4082-acdf-e700ebfa7efc">EvtGetObjectArrayProperty</a> function. For details, see Remarks. When you are done with the handle, call the <a href="https://msdn.microsoft.com/c4b82d7b-508d-45bf-b990-04e90e846525">EvtClose</a> function.


### -field EvtPublisherMetadataKeywordName

Identifies the <b>name</b> attribute of the keyword. Use this identifier when calling the <a href="https://msdn.microsoft.com/a522f0a8-6050-4082-acdf-e700ebfa7efc">EvtGetObjectArrayProperty</a> function. For details, see Remarks. The variant type for this property is <b>EvtVarTypeString</b>.


### -field EvtPublisherMetadataKeywordValue

Identifies the <b>mask</b> attribute of the keyword. Use this identifier when calling the <a href="https://msdn.microsoft.com/a522f0a8-6050-4082-acdf-e700ebfa7efc">EvtGetObjectArrayProperty</a> function. For details, see Remarks. The variant type for this property is <b>EvtVarTypeUInt64</b>.


### -field EvtPublisherMetadataKeywordMessageID

Identifies the <b>message</b> attribute of the keyword. Use this identifier when calling the <a href="https://msdn.microsoft.com/a522f0a8-6050-4082-acdf-e700ebfa7efc">EvtGetObjectArrayProperty</a> function. For details, see Remarks. The variant type for this property is <b>EvtVarTypeUInt32</b>. The property contains the resource identifier that is assigned to the message string. To get the message string, call the <a href="https://msdn.microsoft.com/744fe166-b12c-49d4-ab13-b2ef6a6f9625">EvtFormatMessage</a> function. If the keyword does not specify a message, the value is –1.


### -field EvtPublisherMetadataPropertyIdEND

This enumeration value marks the end of the enumeration values.


## -remarks



This list of identifiers in this enumeration are for those properties that cannot change. To get the configuration for a channel, call the <a href="https://msdn.microsoft.com/0f84f51c-716e-4a70-b31c-2b4f40b3fd83">EvtGetChannelConfigProperty</a> function.

You cannot use the following property identifiers when calling the <a href="https://msdn.microsoft.com/f85a46ef-873c-4dd9-8b5c-3763fd67fc06">EvtGetPublisherMetadataProperty</a> function: 

<ul>
<li><b>EvtPublisherMetadataChannelReferencePath</b></li>
<li><b>EvtPublisherMetadataChannelReferenceIndex</b></li>
<li><b>EvtPublisherMetadataChannelReferenceID</b></li>
<li><b>EvtPublisherMetadataChannelReferenceFlags</b></li>
<li><b>EvtPublisherMetadataChannelReferenceMessageID</b></li>
<li><b>EvtPublisherMetadataLevelName</b></li>
<li><b>EvtPublisherMetadataLevelValue</b></li>
<li><b>EvtPublisherMetadataLevelMessageID</b></li>
<li><b>EvtPublisherMetadataTaskName</b></li>
<li><b>EvtPublisherMetadataTaskEventGuid</b></li>
<li><b>EvtPublisherMetadataTaskValue</b></li>
<li><b>EvtPublisherMetadataTaskMessageID</b></li>
<li><b>EvtPublisherMetadataOpcodeName</b></li>
<li><b>EvtPublisherMetadataOpcodeValue</b></li>
<li><b>EvtPublisherMetadataOpcodeMessageID</b></li>
<li><b>EvtPublisherMetadataKeywordName</b></li>
<li><b>EvtPublisherMetadataKeywordValue</b></li>
<li><b>EvtPublisherMetadataKeywordMessageID</b></li>
</ul>
To use these identifiers, you must first retrieve the handle to the property's parent object.  To retrieve the channel properties, you must first retrieve the handle to the parent object using the <b>EvtPublisherMetadataChannelReferences</b> identifier; to retrieve the level properties, you must first retrieve the handle to the parent object using the <b>EvtPublisherMetadataLevels</b> identifier; to retrieve the task properties, you must first retrieve the handle to the parent object using the <b>EvtPublisherMetadataTasks</b> identifier; to retrieve the opcode properties, you must first retrieve the handle to the parent object using the <b>EvtPublisherMetadataOpcodes</b> identifier; and to retrieve the keyword properties, you must first retrieve the handle to the parent object using the <b>EvtPublisherMetadataKeywords</b> identifier. 

The handle points to an array of objects that contain the metadata for child type that the provider defines. To determine how many objects are in the array, call the <a href="https://msdn.microsoft.com/fc4043ac-48eb-400b-8cf6-b83cbbb2765c">EvtGetObjectArraySize</a> function. To access a property of one of the objects, call the <a href="https://msdn.microsoft.com/a522f0a8-6050-4082-acdf-e700ebfa7efc">EvtGetObjectArrayProperty</a> function and specify the identifier of the property that you want to retrieve.




## -see-also




<a href="https://msdn.microsoft.com/882506e5-222b-45c8-af4b-59db8baa1dae">ChannelType Complex Type</a>



<a href="https://msdn.microsoft.com/d5a71e51-c080-4976-9f33-fe24b523ae81">EVT_EVENT_METADATA_PROPERTY_ID</a>



<a href="https://msdn.microsoft.com/13cf5e71-07bb-45ac-89f9-b76a26539dcd">EVT_VARIANT_TYPE</a>



<a href="https://msdn.microsoft.com/f85a46ef-873c-4dd9-8b5c-3763fd67fc06">EvtGetPublisherMetadataProperty</a>



<a href="https://msdn.microsoft.com/70199cf5-a6d0-4780-9ff1-ed083a5b49ac">ProviderType Complex Type</a>
 

 

