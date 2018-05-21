---
UID: NS:tdh._PROPERTY_DATA_DESCRIPTOR
title: "_PROPERTY_DATA_DESCRIPTOR"
author: windows-driver-content
description: Defines the property to retrieve.
old-location: etw\property_data_descriptor_struct.htm
old-project: ETW
ms.assetid: 38e6f5b1-fce5-45e4-ac7a-09ba40d29837
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: "*PPROPERTY_DATA_DESCRIPTOR, PROPERTY_DATA_DESCRIPTOR, PROPERTY_DATA_DESCRIPTOR structure [ETW], _PROPERTY_DATA_DESCRIPTOR, etw.property_data_descriptor_struct, tdh.property_data_descriptor_struct, tdh/PROPERTY_DATA_DESCRIPTOR"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: PROPERTY_DATA_DESCRIPTOR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Tdh.h
api_name:
-	PROPERTY_DATA_DESCRIPTOR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# _PROPERTY_DATA_DESCRIPTOR structure


## -description



		Defines the property to retrieve.
		
		
	
	


## -struct-fields




### -field PropertyName

Pointer to a null-terminated Unicode string that contains the case-sensitive property name. You can use the <b>NameOffset</b> member of the <a href="https://msdn.microsoft.com/06b82b31-1f0e-45d5-88ec-9b9835af10df">EVENT_PROPERTY_INFO</a> structure to get the property name.

The following table lists the possible values of <i>PropertyName</i> for WPP events. Use the suggested TDH data type when formatting the returned buffer from <a href="https://msdn.microsoft.com/3975792e-cc24-430a-914f-420f3a5ec1d6">TdhGetProperty</a>.

<table>
<tr>
<th>Name</th>
<th>TDH Data Type</th>
<th>Description</th>
</tr>
<tr>
<td>FormattedString</td>
<td>TDH_INTYPE_UNICODESTRING</td>
<td>The formatted WPP trace message.</td>
</tr>
<tr>
<td>SequenceNum</td>
<td>TDH_INTYPE_UINT32</td>
<td>The local or global sequence number of the trace message. Local sequence numbers, which are unique only to this trace session, are the default.</td>
</tr>
<tr>
<td>FunctionName</td>
<td>TDH_INTYPE_UNICODESTRING</td>
<td>The name of the function that generated the trace message.</td>
</tr>
<tr>
<td>ComponentName</td>
<td>TDH_INTYPE_UNICODESTRING</td>
<td>The name of the component of the provider that generated the trace message. The component name appears only if it is specified in the tracing code.</td>
</tr>
<tr>
<td>SubComponentName</td>
<td>TDH_INTYPE_UNICODESTRING</td>
<td>The name of the subcomponent of the provider that generated the trace message. The subcomponent name appears only if it is specified in the tracing code.</td>
</tr>
<tr>
<td>TraceGuid</td>
<td>TDH_INTYPE_GUID</td>
<td>The GUID associated with the WPP trace message.</td>
</tr>
<tr>
<td>GuidTypeName</td>
<td>TDH_INTYPE_UNICODESTRING</td>
<td>The file name concatenated with the line number from the source code from which the WPP trace message was traced.</td>
</tr>
<tr>
<td>SystemTime</td>
<td>TDH_INTYPE_SYSTEMTIME</td>
<td>The time when the WPP trace message was generated.</td>
</tr>
<tr>
<td>FlagsName</td>
<td>TDH_INTYPE_UNICODESTRING</td>
<td>The names of the trace flags enabling the trace message.</td>
</tr>
<tr>
<td>LevelName</td>
<td>TDH_INTYPE_UNICODESTRING</td>
<td>The value of the trace level enabling the trace message.</td>
</tr>
</table>
 


### -field ArrayIndex

Zero-based index for accessing elements of a property array. If the property data is not an array or if you want to address the entire array, specify ULONG_MAX (0xFFFFFFFF).


### -field Reserved

Reserved.


## -remarks



To describe a structure, set PropertyName to the name of the structure and ArrayIndex to ULONG_MAX. 

To describe a member of a structure, define an array of two <b>PROPERTY_DATA_DESCRIPTOR</b> structures. In the first descriptor, set  PropertyName to the name of the structure and ArrayIndex to 0. In the second descriptor, set PropertyName to the name of the member and ArrayIndex to ULONG_MAX.

If the structure is an element of an array of structures, set ArrayIndex in the first descriptor to the zero-based index of the structure in the array.




## -see-also




<a href="https://msdn.microsoft.com/3975792e-cc24-430a-914f-420f3a5ec1d6">TdhGetProperty</a>



<a href="https://msdn.microsoft.com/52b034db-b08b-4c79-973f-33800ca866f5">TdhGetPropertySize</a>
 

 

