---
UID: NE:tdh._PROPERTY_FLAGS
title: "_PROPERTY_FLAGS"
author: windows-sdk-content
description: Defines if the property is contained in a structure or array.
old-location: etw\property_flags_enum.htm
old-project: ETW
ms.assetid: 517c1662-4230-44dc-94f0-a1996291bbee
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: PROPERTY_FLAGS, PROPERTY_FLAGS enumeration [ETW], PropertyHasCustomSchema, PropertyHasTags, PropertyParamCount, PropertyParamFixedCount, PropertyParamFixedLength, PropertyParamLength, PropertyStruct, PropertyWBEMXmlFragment, _PROPERTY_FLAGS, etw.property_flags_enum, tdh.property_flags_enum, tdh/, tdh/PROPERTY_FLAGS, tdh/PropertyHasCustomSchema, tdh/PropertyHasTags, tdh/PropertyParamCount, tdh/PropertyParamFixedCount, tdh/PropertyParamFixedLength, tdh/PropertyParamLength, tdh/PropertyStruct, tdh/PropertyWBEMXmlFragment
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: tdh.h
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
req.typenames: PROPERTY_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tdh.h
api_name:
 - PROPERTY_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# _PROPERTY_FLAGS enumeration


## -description


Defines if the property is contained in a structure or array.


## -enum-fields




### -field PropertyStruct

The property information is contained in the <b>structType</b> member of the <a href="https://msdn.microsoft.com/06b82b31-1f0e-45d5-88ec-9b9835af10df">EVENT_PROPERTY_INFO</a> structure.


### -field PropertyParamLength

Use the <b>lengthPropertyIndex</b> member of the <a href="https://msdn.microsoft.com/06b82b31-1f0e-45d5-88ec-9b9835af10df">EVENT_PROPERTY_INFO</a> structure to locate the property that contains the length value of the property. 


### -field PropertyParamCount

Use the <b>countPropertyIndex</b> member of the <a href="https://msdn.microsoft.com/06b82b31-1f0e-45d5-88ec-9b9835af10df">EVENT_PROPERTY_INFO</a> structure to locate the property that contains the size of the array. 


### -field PropertyWBEMXmlFragment

Indicates that the MOF data is in XML format (the event data contains within itself a fully-rendered XML description). This flag is set if the MOF property contains the XMLFragment qualifier.


### -field PropertyParamFixedLength

Indicates that the length member of the <a href="https://msdn.microsoft.com/06b82b31-1f0e-45d5-88ec-9b9835af10df">EVENT_PROPERTY_INFO</a> structure contains a fixed length, e.g. as specified in the provider manifest with &lt;data length="12" … /&gt;. This flag will not be set for a variable-length field, e.g. &lt;data length="LengthField" … /&gt;, nor will this flag be set for fields where the length is not specified in the manifest, e.g. int32 or null-terminated string. As an example, if <i>PropertyParamLength</i> is unset, length is 0, and InType is <b>TDH_INTYPE_UNICODESTRING</b>, we must check the <i>PropertyParamFixedLength</i> flag to determine the length of the string. If <i>PropertyParamFixedLength</i> is set, the string length is fixed at 0. If <i>PropertyParamFixedLength</i> is unset, the string is null-terminated.


### -field PropertyParamFixedCount

Indicates that the count member of the <a href="https://msdn.microsoft.com/06b82b31-1f0e-45d5-88ec-9b9835af10df">EVENT_PROPERTY_INFO</a> structure contains a fixed array count, e.g. as specified in the provider manifest with &lt;data count="12" … /&gt;. This flag will not be set for a variable-length array, e.g. &lt;data count="ArrayCount" … /&gt;, nor will this flag be set for non-array fields. As an example, if <i>PropertyParamCount</i> is unset and count is 1, PropertyParamFixedCount flag must be checked to determine whether the field is a scalar value or a single-element array. If <i>PropertyParamFixedCount</i> is set, the field is a single-element array. If PropertyParamFixedCount is unset, the field is a scalar value, not an array.

<div class="alert"><b>Caution</b>  This flag is new in the Windows 10 SDK. Earlier versions of the manifest compiler did not set this flag. For compatibility with manifests compiled with earlier versions of the compiler, event processing tools should only use this flag when determining whether to present a field with a fixed count of 1 as an array or a scalar.</div>
<div> </div>

### -field PropertyHasTags

Indicates that the <b>Tags</b> field contains valid field tag data. 


### -field PropertyHasCustomSchema

Indicates that the <b>Type</b> is described with a custom schema. 

<div class="alert"><b>Note</b>  This flag is new in the Windows 10 SDK.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/06b82b31-1f0e-45d5-88ec-9b9835af10df">EVENT_PROPERTY_INFO</a>
 

 

