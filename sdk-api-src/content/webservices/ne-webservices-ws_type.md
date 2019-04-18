---
UID: NE:webservices.__unnamed_enum_81
title: WS_TYPE (webservices.h)
author: windows-sdk-content
description: The types supported for serialization.
old-location: wsw\ws_type.htm
tech.root: wsw
ms.assetid: eb3732fd-1197-4e1c-b5b5-9a34aaa0951e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WS_ANY_ATTRIBUTES_TYPE, WS_BOOL_TYPE, WS_BYTES_TYPE, WS_BYTE_ARRAY_TYPE, WS_CHAR_ARRAY_TYPE, WS_CUSTOM_TYPE, WS_DATETIME_TYPE, WS_DECIMAL_TYPE, WS_DESCRIPTION_TYPE, WS_DOUBLE_TYPE, WS_DURATION_TYPE, WS_ENDPOINT_ADDRESS_TYPE, WS_ENUM_TYPE, WS_FAULT_TYPE, WS_FLOAT_TYPE, WS_GUID_TYPE, WS_INT16_TYPE, WS_INT32_TYPE, WS_INT64_TYPE, WS_INT8_TYPE, WS_STRING_TYPE, WS_STRUCT_TYPE, WS_TIMESPAN_TYPE, WS_TYPE, WS_TYPE enumeration [Web Services for Windows], WS_UINT16_TYPE, WS_UINT32_TYPE, WS_UINT64_TYPE, WS_UINT8_TYPE, WS_UNION_TYPE, WS_UNIQUE_ID_TYPE, WS_UTF8_ARRAY_TYPE, WS_VOID_TYPE, WS_WSZ_TYPE, WS_XML_BUFFER_TYPE, WS_XML_QNAME_TYPE, WS_XML_STRING_TYPE, webservices/WS_ANY_ATTRIBUTES_TYPE, webservices/WS_BOOL_TYPE, webservices/WS_BYTES_TYPE, webservices/WS_BYTE_ARRAY_TYPE, webservices/WS_CHAR_ARRAY_TYPE, webservices/WS_CUSTOM_TYPE, webservices/WS_DATETIME_TYPE, webservices/WS_DECIMAL_TYPE, webservices/WS_DESCRIPTION_TYPE, webservices/WS_DOUBLE_TYPE, webservices/WS_DURATION_TYPE, webservices/WS_ENDPOINT_ADDRESS_TYPE, webservices/WS_ENUM_TYPE, webservices/WS_FAULT_TYPE, webservices/WS_FLOAT_TYPE, webservices/WS_GUID_TYPE, webservices/WS_INT16_TYPE, webservices/WS_INT32_TYPE, webservices/WS_INT64_TYPE, webservices/WS_INT8_TYPE, webservices/WS_STRING_TYPE, webservices/WS_STRUCT_TYPE, webservices/WS_TIMESPAN_TYPE, webservices/WS_TYPE, webservices/WS_UINT16_TYPE, webservices/WS_UINT32_TYPE, webservices/WS_UINT64_TYPE, webservices/WS_UINT8_TYPE, webservices/WS_UNION_TYPE, webservices/WS_UNIQUE_ID_TYPE, webservices/WS_UTF8_ARRAY_TYPE, webservices/WS_VOID_TYPE, webservices/WS_WSZ_TYPE, webservices/WS_XML_BUFFER_TYPE, webservices/WS_XML_QNAME_TYPE, webservices/WS_XML_STRING_TYPE, wsw.ws_type
ms.topic: enum
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - WebServices.h
api_name:
 - WS_TYPE
product: Windows
targetos: Windows
req.typenames: WS_TYPE
req.redist: 
ms.custom: 19H1
---

# WS_TYPE enumeration


## -description


The types supported for serialization.
            


## -enum-fields




### -field WS_BOOL_TYPE

Used when serializing a <b>BOOL</b> value.
                

The <a href="https://msdn.microsoft.com/2f013802-c564-4544-946f-534afd402474">WS_BOOL_DESCRIPTION</a> type description can optionally be
                    specified for this type in order to constrain the allowed values.
                

This type can be used with the following <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ATTRIBUTE_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_CONTENT_TYPE_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ATTRIBUTE_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_TEXT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
</ul>
A nil value is represented using a <b>NULL</b> pointer.
                

A <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a> may be specified for this type.
                    See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> to see
                    which field mapping values allow a default value to be specified.
               


### -field WS_INT8_TYPE

Used when serializing a signed 8-bit integer (<b>char</b>).
                

The <a href="https://msdn.microsoft.com/8085c256-fb1a-4537-bbad-9a1b3e8149ee">WS_INT8_DESCRIPTION</a> type description can optionally be
                    specified for this type in order to constrain the allowed values.
                

This type can be used with the following <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ATTRIBUTE_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_CONTENT_TYPE_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ATTRIBUTE_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_TEXT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
</ul>
A nil value is represented using a <b>NULL</b> pointer.
                

A <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a> may be specified for this type.
                    See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> to see
                    which field mapping values allow a default value to be specified.
                


### -field WS_INT16_TYPE

Used when serializing a signed 16-bit integer (<b>short</b>).
                

The <a href="https://msdn.microsoft.com/06cf286f-971b-46e1-92b4-655d6d55606a">WS_INT16_DESCRIPTION</a> type description can optionally be
                    specified for this type in order to constrain the allowed values.
                

This type can be used with the following <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ATTRIBUTE_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_CONTENT_TYPE_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ATTRIBUTE_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_TEXT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
</ul>
A nil value is represented using a <b>NULL</b> pointer.
                

A <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a> may be specified for this type.
                    See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> to see
                    which field mapping values allow a default value to be specified.
                


### -field WS_INT32_TYPE

Used when serializing a signed 32-bit integer.
                

The <a href="https://msdn.microsoft.com/98761df2-b195-4f22-90ba-3dac8920f3ef">WS_INT32_DESCRIPTION</a> type description can optionally be
                    specified for this type in order to constrain the allowed values.
                

This type can be used with the following <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ATTRIBUTE_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_CONTENT_TYPE_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ATTRIBUTE_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_TEXT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
</ul>
A nil value is represented using a <b>NULL</b> pointer.
                

A <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a> may be specified for this type.
                    See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> to see
                    which field mapping values allow a default value to be specified.
                


### -field WS_INT64_TYPE

Used when serializing a signed 64-bit integer.
                

The <a href="https://msdn.microsoft.com/b8e355c0-2695-4162-aa77-703367ee117e">WS_INT64_DESCRIPTION</a> type description can optionally be
                    specified for this type in order to constrain the allowed values.
                

This type can be used with the following <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ATTRIBUTE_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_CONTENT_TYPE_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ATTRIBUTE_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_TEXT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
</ul>
A nil value is represented using a <b>NULL</b> pointer.
                

A <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a> may be specified for this type.
                    See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> to see
                    which field mapping values allow a default value to be specified.
                


### -field WS_UINT8_TYPE

Used when serializing an unsigned 8-bit integer (<b>BYTE</b>).
                

The <a href="https://msdn.microsoft.com/0e878a19-8f64-4fa2-a6a7-9a12c2ec8efc">WS_UINT8_DESCRIPTION</a> type description can optionally be
                    specified for this type in order to constrain the allowed values.
                

This type can be used with the following <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ATTRIBUTE_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_CONTENT_TYPE_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ATTRIBUTE_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_TEXT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
</ul>
A nil value is represented using a <b>NULL</b> pointer.
                

A <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a> may be specified for this type.
                    See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> to see
                    which field mapping values allow a default value to be specified.
                


### -field WS_UINT16_TYPE

Used when serializing an unsigned 16-bit integer.
                

The <a href="https://msdn.microsoft.com/62bc0e6c-a8f0-4b57-89bc-a2832d785703">WS_UINT16_DESCRIPTION</a> type description can optionally be
                    specified for this type in order to constrain the allowed values.
                

This type can be used with the following <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ATTRIBUTE_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_CONTENT_TYPE_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ATTRIBUTE_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_TEXT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
</ul>
A nil value is represented using a <b>NULL</b> pointer.
                

A <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a> may be specified for this type.
                    See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> to see
                    which field mapping values allow a default value to be specified.
                


### -field WS_UINT32_TYPE

Used when serializing an unsigned 32-bit integer.
                

The <a href="https://msdn.microsoft.com/dcb864f2-f162-41ca-b3ef-5b592a311299">WS_UINT32_DESCRIPTION</a> type description can optionally be
                    specified for this type in order to constrain the allowed values.
                

This type can be used with the following <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ATTRIBUTE_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_CONTENT_TYPE_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ATTRIBUTE_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_TEXT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
</ul>
A nil value is represented using a <b>NULL</b> pointer.
                

A <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a> may be specified for this type.
                    See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> to see
                    which field mapping values allow a default value to be specified.
                


### -field WS_UINT64_TYPE

Used when serializing an unsigned 64-bit integer.
                

The <a href="https://msdn.microsoft.com/62a8da3a-3e5d-4ce8-bda5-08f84255ba3f">WS_UINT64_DESCRIPTION</a> type description can optionally be
                    specified for this type in order to constrain the allowed values.
                

This type can be used with the following <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ATTRIBUTE_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_CONTENT_TYPE_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ATTRIBUTE_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_TEXT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
</ul>
A nil value is represented using a <b>NULL</b> pointer.
                

A <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a> may be specified for this type.
                    See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> to see
                    which field mapping values allow a default value to be specified.
                


### -field WS_FLOAT_TYPE

Used when serializing a <b>float</b>.
                

The <a href="https://msdn.microsoft.com/54af331f-92bd-4970-945d-13f3a2e62c4b">WS_FLOAT_DESCRIPTION</a> type description can optionally be
                    specified for this type in order to constrain the allowed values.
                

This type can be used with the following <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ATTRIBUTE_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_CONTENT_TYPE_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ATTRIBUTE_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_TEXT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
</ul>
A nil value is represented using a <b>NULL</b> pointer.
                

A <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a> may be specified for this type.
                    See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> to see
                    which field mapping values allow a default value to be specified.
                


### -field WS_DOUBLE_TYPE

Used when serializing a <b>double</b>.
                

The <a href="https://msdn.microsoft.com/cc845d24-4bbd-4491-9d4e-7a39c6c251da">WS_DOUBLE_DESCRIPTION</a> type description can optionally be
                    specified for this type in order to constrain the allowed values.
                

This type can be used with the following <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ATTRIBUTE_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_CONTENT_TYPE_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ATTRIBUTE_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_TEXT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
</ul>
A nil value is represented using a <b>NULL</b> pointer.
                

A <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a> may be specified for this type.
                    See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> to see
                    which field mapping values allow a default value to be specified.
                


### -field WS_DECIMAL_TYPE

Used when serializing a <b>DECIMAL</b>.
                

The <a href="https://msdn.microsoft.com/c2e8fc81-1a09-456c-b8bb-9160bc286ec2">WS_DECIMAL_DESCRIPTION</a> type description can optionally be
                    specified for this type in order to constrain the allowed values.
                

This type can be used with the following <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ATTRIBUTE_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_CONTENT_TYPE_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ATTRIBUTE_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_TEXT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
</ul>
A nil value is represented using a <b>NULL</b> pointer.
                

A <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a> may be specified for this type.
                    See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> to see
                    which field mapping values allow a default value to be specified.
                


### -field WS_DATETIME_TYPE

Used when serializing a <a href="https://msdn.microsoft.com/635f8e0b-f994-4500-85ad-dd74fb4a6c22">WS_DATETIME</a>.
                

The <a href="https://msdn.microsoft.com/f6a7094f-56c0-4d8e-9050-fe41c4a82bf4">WS_DATETIME_DESCRIPTION</a> type description can optionally be
                    specified for this type in order to constrain the allowed values.
                

This type can be used with the following <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ATTRIBUTE_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_CONTENT_TYPE_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ATTRIBUTE_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_TEXT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
</ul>
A nil value is represented using a <b>NULL</b> pointer.
                

A <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a> may be specified for this type.
                    See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> to see
                    which field mapping values allow a default value to be specified.
                


### -field WS_TIMESPAN_TYPE

Used when serializing a <a href="https://msdn.microsoft.com/f8a42739-e395-4b20-bf3a-3d7c5e3a5495">WS_TIMESPAN</a>.
                

The <a href="https://msdn.microsoft.com/8c74c30e-6793-490b-bc36-b7c60ef35232">WS_TIMESPAN_DESCRIPTION</a> type description can optionally be
                    specified for this type in order to constrain the allowed values.
                

This type can be used with the following <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ATTRIBUTE_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_CONTENT_TYPE_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ATTRIBUTE_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_TEXT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
</ul>
A nil value is represented using a <b>NULL</b> pointer.
                

A <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a> may be specified for this type.
                    See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> to see
                    which field mapping values allow a default value to be specified.
                


### -field WS_GUID_TYPE

Used when serializing a <b>GUID</b>.
                

The <a href="https://msdn.microsoft.com/e0a98163-66c3-4b6d-a91c-f143b3aad864">WS_GUID_DESCRIPTION</a> type description can optionally be
                    specified for this type in order to constrain the allowed values.
                

This type can be used with the following <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ATTRIBUTE_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_CONTENT_TYPE_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ATTRIBUTE_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_TEXT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
</ul>
A nil value is represented using a <b>NULL</b> pointer.
                

A <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a> may be specified for this type.
                    See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> to see
                    which field mapping values allow a default value to be specified.
                


### -field WS_UNIQUE_ID_TYPE

Used when serializing a <a href="https://msdn.microsoft.com/b9fd4497-153f-45f9-8f23-0771ffc47830">WS_UNIQUE_ID</a>.
                

The <a href="https://msdn.microsoft.com/d00695e6-2c3d-4eff-b5cd-f4f81954fb0f">WS_UNIQUE_ID_DESCRIPTION</a> type description can optionally be
                    specified for this type in order to constrain the allowed values.
                

This type can be used with the following <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ATTRIBUTE_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_CONTENT_TYPE_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ATTRIBUTE_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_TEXT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
</ul>
A nil value is represented using a <b>NULL</b> pointer.
                

A <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a> may be specified for this type.
                    See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> to see
                    which field mapping values allow a default value to be specified.
                


### -field WS_STRING_TYPE

Used when serializing a <a href="https://msdn.microsoft.com/eb6c7397-6b15-4e79-89ec-585861113edf">WS_STRING</a>.
                

The <a href="https://msdn.microsoft.com/10abb773-ec10-4e72-bce8-13fe3c41cb52">WS_STRING_DESCRIPTION</a> type description can optionally be
                    specified for this type in order to constrain the allowed values.
                

This type can be used with the following <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ATTRIBUTE_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_CONTENT_TYPE_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ATTRIBUTE_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_TEXT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_XML_ATTRIBUTE_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a> | <b>WS_FIELD_OPTIONAL</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE_ITEM</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
</ul>
A nil value is represented by setting the chars field to <b>NULL</b> and specifying a length of 0.
                    A nil string is distinquished from an empty string based on whether or not the chars field 
                    is <b>NULL</b> or not when the length is zero.
                

A <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a> may be specified for this type.
                    See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> to see
                    which field mapping values allow a default value to be specified.
                


### -field WS_WSZ_TYPE

Used when serializing a zero-terminated <b>WCHAR</b>*.
                

The <a href="https://msdn.microsoft.com/12b6f630-7585-4c88-8c49-f37d1899d32b">WS_WSZ_DESCRIPTION</a> type description can optionally be
                    specified for this type in order to constrain the allowed values.
                

Deserialization will return an error if the wire form of the string 
                    contains an embedded zero.
                

This type can be used with the following <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ATTRIBUTE_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_CONTENT_TYPE_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ATTRIBUTE_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_TEXT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_XML_ATTRIBUTE_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a> | <b>WS_FIELD_OPTIONAL</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE_ITEM</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
</ul>
A nil value is represented using a <b>NULL</b> pointer.
                

A <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a> may be specified for this type.
                    See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> to see
                    which field mapping values allow a default value to be specified.
                    The default value should point to the address of a WCHAR*, and 
                    the size should be sizeof(WCHAR*).
                


### -field WS_BYTES_TYPE

Used when serializing a <a href="https://msdn.microsoft.com/0106e372-80bf-4a62-b941-1a4501c92a9c">WS_BYTES</a>.
                

The <a href="https://msdn.microsoft.com/0c5384f9-0f6c-4523-bacb-ec3dd7321648">WS_BYTES_DESCRIPTION</a> type description can optionally be
                    specified for this type in order to constrain the allowed values.
                

This type can be used with the following <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ATTRIBUTE_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_CONTENT_TYPE_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ATTRIBUTE_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_TEXT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a> | <b>WS_FIELD_OPTIONAL</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE_ITEM</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
</ul>
A nil value is represented by setting the bytes field to <b>NULL</b> and specifying a length of 0.  
                    A nil array is distinquished from an empty array based on whether or not the bytes field is 
                    <b>NULL</b> or not when the length is zero.
                

A <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a> may be specified for this type.
                    See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> to see
                    which field mapping values allow a default value to be specified.
                


### -field WS_XML_STRING_TYPE

Used when serializing a <a href="https://msdn.microsoft.com/3daa656f-7f97-4e29-a556-7ff72206f01c">WS_XML_STRING</a>.
                

The <a href="https://msdn.microsoft.com/5b3c28ed-ed2c-4d65-a641-a653eddd021e">WS_XML_STRING_DESCRIPTION</a> type description can optionally be
                    specified for this type in order to constrain the allowed values.
                

Embedded zeros are allowed in the array of utf8 bytes.
                

This type can be used with the following <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ATTRIBUTE_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_CONTENT_TYPE_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ATTRIBUTE_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_TEXT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a> | <b>WS_FIELD_OPTIONAL</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE_ITEM</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
</ul>
A nil value is represented by setting the bytes field to <b>NULL</b> and specifying a length of 0.  
                    A nil string is distinquished from an empty string based on whether or not the bytes field is 
                    <b>NULL</b> or not when the length is zero.
                

A <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a> may be specified for this type.
                    See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> to see
                    which field mapping values allow a default value to be specified.
                


### -field WS_XML_QNAME_TYPE

Used when serializing a <a href="https://msdn.microsoft.com/54095ad5-e9ba-4fa8-92e2-87b3a8950d5c">WS_XML_QNAME</a>.
                

The <a href="https://msdn.microsoft.com/300c5fd1-1a66-40b8-9f26-0f0711f7a527">WS_XML_QNAME_DESCRIPTION</a> type description can optionally be
                    specified for this type in order to constrain the allowed values.
                

This type can be used with the following <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ATTRIBUTE_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_CONTENT_TYPE_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ATTRIBUTE_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_TEXT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a> | <b>WS_FIELD_POINTER</b>.
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
</ul>
A nil value is represented using a <b>NULL</b> pointer.
                

A <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a> may be specified for this type.
                    See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> to see
                    which field mapping values allow a default value to be specified.
                


### -field WS_XML_BUFFER_TYPE

Used when serializing an <a href="https://msdn.microsoft.com/75f1df70-4dc9-4365-9005-5eaca6688f16">WS_XML_BUFFER</a>*.
                

This type has no associated type description structure.
                

This type can be used with the following <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ANY_ELEMENT_TYPE_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ANY_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ANY_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ANY_CONTENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a> | <b>WS_FIELD_OPTIONAL</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE_ITEM</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
</ul>
A nil value is represented using a <b>NULL</b> pointer.
                

This type does not support specifying a <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a>.
                

The interpretation of the contents of the <a href="https://msdn.microsoft.com/75f1df70-4dc9-4365-9005-5eaca6688f16">WS_XML_BUFFER</a> is as follows:
                

<ul>
<li>
When used at the top level or with <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>, the
                        <a href="https://msdn.microsoft.com/75f1df70-4dc9-4365-9005-5eaca6688f16">WS_XML_BUFFER</a> should contain a single element which represents
                        the attribute and element content.  The local name and namespace of the
                        element in the buffer is ignored; it is replaced with actual element
                        name and namespace when the buffer is written.  For example:
                    

<pre class="syntax" xml:space="preserve"><code>
// Element in WS_XML_BUFFER
&lt;PrefixInBuffer:LocalNameInBuffer xmlns:PrefixInBuffer="namespace-in-buffer" other-attributes&gt;
text-and-or-element-content
&lt;/PrefixInBuffer:LocalNameInBuffer&gt;

// Element that is written
&lt;NewPrefix:NewLocalName xmlns:NewPrefix="new-namespace" other-attributes&gt;
text-and-or-element-content
&lt;/NewPrefix:NewLocalName&gt;</code></pre>
To avoid problems with namespace collisions, it is a best practice to follow one of the
                        following rules when selecting a namespace for the element in the buffer:
                    

<ul>
<li>Use a namespace other than "" that is not otherwise used in the buffer.
                        </li>
<li>Use the same namespace as the element that will be written.
                    </li>
</ul>
When the value is deserialized, the element name and namespace will correspond
                        to the element that was read.
                    

</li>
<li>
When used with <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ANY_ELEMENT_FIELD_MAPPING</a>, the
                        <a href="https://msdn.microsoft.com/75f1df70-4dc9-4365-9005-5eaca6688f16">WS_XML_BUFFER</a> should contain a single element which 
                        represents a single element in the XML content.
                    

</li>
<li>
When used with <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>, each
                        of the <a href="https://msdn.microsoft.com/75f1df70-4dc9-4365-9005-5eaca6688f16">WS_XML_BUFFER</a>s that are serialized in the array
                        has the same convention as with <b>WS_ELEMENT_FIELD_MAPPING</b>described above (each WS_XML_BUFFER represents a single element
                        in the XML content).
                    

</li>
<li>
When used with <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ANY_ELEMENT_FIELD_MAPPING</a>, each
                        of the <a href="https://msdn.microsoft.com/75f1df70-4dc9-4365-9005-5eaca6688f16">WS_XML_BUFFER</a>s that are serialized in the array
                        represents a single element in the XML content.
                    

</li>
<li>
When used with <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ANY_CONTENT_FIELD_MAPPING</a>, the
                        <a href="https://msdn.microsoft.com/75f1df70-4dc9-4365-9005-5eaca6688f16">WS_XML_BUFFER</a> may contain zero or more top level elements
                        or text.  This content corresponds to the remaining XML content of the 
                        containing structure.
                    

</li>
</ul>

### -field WS_CHAR_ARRAY_TYPE

Used when serializing two fields of a structure as a unit: a <b>WCHAR</b>* field which
                    points to an array of WCHARs, and a ULONG field which contains the number
                    of characters in the array.  This type may only be used within a
                    <a href="https://msdn.microsoft.com/8b562fab-f3c5-4732-b993-f7f61ca14ab6">WS_FIELD_DESCRIPTION</a>.
                

<pre class="syntax" xml:space="preserve"><code>
struct
{
    ULONG count;    // array length, in characters
    WCHAR* chars;   // array of unicode characters
} value;</code></pre>
The fields can be anywhere in the contained structure and in any order, since
                    their offsets within the structure are specified separately as part of the
                    <a href="https://msdn.microsoft.com/8b562fab-f3c5-4732-b993-f7f61ca14ab6">WS_FIELD_DESCRIPTION</a>.
                    The offset of the count field is specified in the countOffset field, and the
                    offset of the chars field is specified in the offset field.
                

Embedded zeros are allowed in the array of characters.
                

The <a href="https://msdn.microsoft.com/3a489963-9ed3-40ca-be42-485415e7fa4a">WS_CHAR_ARRAY_DESCRIPTION</a> type description can optionally be
                    specified for this type in order to constrain the allowed values.
                

This type cannot be used with any <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values.
                

This type may only be used within a <a href="https://msdn.microsoft.com/8b562fab-f3c5-4732-b993-f7f61ca14ab6">WS_FIELD_DESCRIPTION</a>.
                

This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ATTRIBUTE_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_TEXT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_XML_ATTRIBUTE_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a> | <b>WS_FIELD_OPTIONAL</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE_ITEM</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
</ul>
A nil string is represented by setting the chars field to <b>NULL</b> and specifying a length of 0.
                    A nil string is distinquished from an empty string based on whether or not the chars field is
                    <b>NULL</b> or not (in both cases the length is zero).
                

This type does not support specifying a <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a>.
                


### -field WS_UTF8_ARRAY_TYPE

Used when serializing two fields of a structure as a unit: a BYTE* field which
                    points to an array of UTF8 bytes, and a ULONG field which contains the number
                    of bytes in the array.  This type may only be used within a
                    <a href="https://msdn.microsoft.com/8b562fab-f3c5-4732-b993-f7f61ca14ab6">WS_FIELD_DESCRIPTION</a>.
                

<pre class="syntax" xml:space="preserve"><code>
struct
{
    ULONG count; // array length, in bytes
    BYTE* bytes; // array of utf8 characters
} value;</code></pre>
The fields can be anywhere in the contained structure and in any order, since
                    their offsets within the structure are specified separately as part of the
                    <a href="https://msdn.microsoft.com/8b562fab-f3c5-4732-b993-f7f61ca14ab6">WS_FIELD_DESCRIPTION</a>.
                    The offset of the count field is specified in the countOffset field, and the
                    offset of the bytes field is specified in the offset field.
                

Embedded zeros are allowed in the array of utf8 bytes.
                

The <a href="https://msdn.microsoft.com/f4aa8194-06b0-4da7-b4cc-b59c0a046711">WS_UTF8_ARRAY_DESCRIPTION</a> type description can optionally be
                    specified for this type in order to constrain the allowed values.
                

This type cannot be used with any <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values.
                

This type may only be used within a <a href="https://msdn.microsoft.com/8b562fab-f3c5-4732-b993-f7f61ca14ab6">WS_FIELD_DESCRIPTION</a>.
                

This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ATTRIBUTE_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_TEXT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a> | <b>WS_FIELD_OPTIONAL</b></li>
</ul>
A nil string is represented by setting the bytes field to <b>NULL</b> and specifying a length of 0.
                    A nil string is distinquished from an empty string based on whether or not the bytes field is
                    <b>NULL</b> or not (in both cases the length is zero).
                

This type does not support specifying a <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a>.
                


### -field WS_BYTE_ARRAY_TYPE

Used when serializing two fields of a structure as a unit: a BYTE* field which
                    points to an array bytes, and a ULONG field which contains the number
                    of bytes in the array.  This type may only be used within a
                    <a href="https://msdn.microsoft.com/8b562fab-f3c5-4732-b993-f7f61ca14ab6">WS_FIELD_DESCRIPTION</a>.
                

<pre class="syntax" xml:space="preserve"><code>
struct
{
    ULONG count;    // array length, in bytes
    BYTE* bytes;    // array of bytes
} value;</code></pre>
The fields can be anywhere in the contained structure and in any order, since
                    their offsets within the structure are specified separately as part of the 
                    <a href="https://msdn.microsoft.com/8b562fab-f3c5-4732-b993-f7f61ca14ab6">WS_FIELD_DESCRIPTION</a>.
                    The offset of the count field is specified in the countOffset field, and the 
                    offset of the bytes field is specified in the offset field.
                

The <a href="https://msdn.microsoft.com/4bdc2956-387e-4cf6-93e1-3a3879c74ccf">WS_BYTE_ARRAY_DESCRIPTION</a> type description can optionally be
                    specified for this type in order to constrain the allowed values.
                

This type cannot be used with any <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values.
                

This type may only be used within a <a href="https://msdn.microsoft.com/8b562fab-f3c5-4732-b993-f7f61ca14ab6">WS_FIELD_DESCRIPTION</a>.
                

This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ATTRIBUTE_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_TEXT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a> | <b>WS_FIELD_OPTIONAL</b></li>
</ul>
A nil array is represented by setting the array pointer field to <b>NULL</b> and specifying a length of 0.
                    A nil array is distinquished from an empty array based on whether or not the array pointer field is
                    <b>NULL</b> or not (in both cases the length is zero).
                

This type does not support specifying a <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a>.
                


### -field WS_DESCRIPTION_TYPE

Used to represent the XML type of the structure being serialized.  This can be used
                    to identify sub-types using the xsi:type attribute from XML Schema.  The field of
                    the structure must be of type <a href="https://msdn.microsoft.com/b426a07e-9993-4cea-8847-fc80e9d0b451">WS_STRUCT_DESCRIPTION*</a>.
                

This type does not have an associated type description.
                

This type cannot be used with any <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values.
                

This type may only be used within a <a href="https://msdn.microsoft.com/8b562fab-f3c5-4732-b993-f7f61ca14ab6">WS_FIELD_DESCRIPTION</a>.
                

This type does not support specifying a <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a>.
                

This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_TYPE_ATTRIBUTE_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                </li>
</ul>

### -field WS_STRUCT_TYPE

Used when serializing a user-defined structure.  The associated type description points to a
                    <a href="https://msdn.microsoft.com/b426a07e-9993-4cea-8847-fc80e9d0b451">WS_STRUCT_DESCRIPTION</a> which provides information about how to serialize 
                    the fields of the structure.
                

This type requires a <a href="https://msdn.microsoft.com/b426a07e-9993-4cea-8847-fc80e9d0b451">WS_STRUCT_DESCRIPTION</a> type description
                    to be supplied which provides information about how to serialize the type.
                

This type can be used with the following <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values,
                    as long as the fields defined by the structure follow the stated restrictions:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_TYPE_MAPPING</a>.  All field mappings are supported.
                    </li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ATTRIBUTE_TYPE_MAPPING</a>.
                        Only the following mappings are supported:
                        <ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_TEXT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>
</li>
</ul>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_CONTENT_TYPE_MAPPING</a>.
                    Only the following mappings are supported:
                    <ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_TEXT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>
</li>
</ul>
</li>
<li></li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_TEXT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a> | <b>WS_FIELD_POINTER</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a> | <b>WS_FIELD_POINTER</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_POINTER</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
</ul>
A nil value is represented using a <b>NULL</b> pointer.
                

This type does not support specifying a <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a>.
                


### -field WS_CUSTOM_TYPE

Used when serializing a custom type.    The associated type description points to a
                    <a href="https://msdn.microsoft.com/7ae3d16c-0755-4226-844e-52cf96fa84fb">WS_CUSTOM_TYPE_DESCRIPTION</a> which provides information about how to serialize the type.
                

This type requires a <a href="https://msdn.microsoft.com/7ae3d16c-0755-4226-844e-52cf96fa84fb">WS_CUSTOM_TYPE_DESCRIPTION</a> type description
                    to be supplied which provides information about how to serialize the type, including
                    a <a href="https://msdn.microsoft.com/95df152c-69cb-4417-9e85-e7ecb54ed042">WS_READ_TYPE_CALLBACK</a> and <a href="https://msdn.microsoft.com/f94bdf80-abea-4a97-9d41-add498e314b1">WS_WRITE_TYPE_CALLBACK</a> which
                    are used to read and write the type.
                

The callbacks are passed the <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> and make the determination
                    as to whether the mapping is supported.
                

The support for each <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> value is dependent on the 
                    <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> support determined by the callback.  The rules
                    are as follows:
                

<ul>
<li>If <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_TYPE_MAPPING</a> is supported, then the following field mappings are supported:
                    <ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>
</li>
</ul>
</li>
<li>If <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ATTRIBUTE_TYPE_MAPPING</a> is supported, then the following field mappings are supported:
                    <ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ATTRIBUTE_FIELD_MAPPING</a>
</li>
</ul>
</li>
<li>If <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_CONTENT_TYPE_MAPPING</a> is supported, then the following field mappings are supported:
                    <ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_TEXT_FIELD_MAPPING</a>
</li>
</ul>
</li>
<li>If <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ANY_ELEMENT_TYPE_MAPPING</a> is supported, then the following field mappings are supported:
                    <ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ANY_ELEMENT_FIELD_MAPPING</a>
</li>
</ul>
</li>
</ul>
Regardless of what <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values are supported, the type
                    can always be used with <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>.
                

This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a> | <b>WS_FIELD_POINTER</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
</ul>
A nil value is represented using a <b>NULL</b> pointer.
                

A <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a> may be specified for this type.
                    See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> to see
                    which field mapping values allow a default value to be specified.
                


### -field WS_ENDPOINT_ADDRESS_TYPE

Used when serializing <a href="https://msdn.microsoft.com/4e9b5f3e-849f-46aa-a94a-3cd6ae16275f">WS_ENDPOINT_ADDRESS</a> .  The associated type description points to a
                    <a href="https://msdn.microsoft.com/en-us/library/Dd401829(v=VS.85).aspx">WS_ENDPOINT_ADDRESS_DESCRIPTION</a> which provides information about how to serialize the endpoint address.
                

This type requires a <a href="https://msdn.microsoft.com/en-us/library/Dd401829(v=VS.85).aspx">WS_ENDPOINT_ADDRESS_DESCRIPTION</a> type description
                    to be supplied which provides information about the serialization format.
                

This type can be used with the following <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_TYPE_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a> | <b>WS_FIELD_POINTER</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a> | <b>WS_FIELD_POINTER</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
</ul>
A nil value is represented using a <b>NULL</b> pointer.
                

This type does not support specifying a <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a>.
                


### -field WS_FAULT_TYPE

Used when serializing a <a href="https://msdn.microsoft.com/7fe0b142-04a1-4a92-99ca-523412f7c94e">WS_FAULT</a>.  The associated type description points to a
                    <a href="https://msdn.microsoft.com/6634faec-5491-4332-b815-be2effa263f8">WS_FAULT_DESCRIPTION</a> which provides information about how to serialize the fault.
                

This type requires a <a href="https://msdn.microsoft.com/6634faec-5491-4332-b815-be2effa263f8">WS_FAULT_DESCRIPTION</a> type description
                    to be supplied which provides information about the serialization format.
                

This type can be used with the following <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_TYPE_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a> | <b>WS_FIELD_POINTER</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a> | <b>WS_FIELD_POINTER</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_POINTER</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
</ul>
A nil value is represented using a <b>NULL</b> pointer.
                

This type does not support specifying a <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a>.
                


### -field WS_VOID_TYPE

This type is used to specify an arbitrary size field.
                

A <a href="https://msdn.microsoft.com/92373e0d-3fe1-4486-8e79-deb0fc24cb63">WS_VOID_DESCRIPTION</a> can optionally be supplied in order
                    to specify the size of the type.
                

This type cannot be used with any <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values.
                

This type can only be used within the <a href="https://msdn.microsoft.com/8b562fab-f3c5-4732-b993-f7f61ca14ab6">WS_FIELD_DESCRIPTION</a> of a
                    <a href="https://msdn.microsoft.com/b426a07e-9993-4cea-8847-fc80e9d0b451">WS_STRUCT_DESCRIPTION</a>.
                

This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a> | <b>WS_FIELD_POINTER</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>.  This is used to initialize a field of a structure 
                    to a default value when deserializing.  This is used for the case where the 
                    particular field does not have a mapping to the XML content, and the type 
                    is not one of the other <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_TYPE</a>s.  The value will be initialized as
                    follows:
                    <ul>
<li>If <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> is specified, then the field will
                        be set to <b>NULL</b>.
                        </li>
<li>If <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> is not specified, then the field will
                        be set to the <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a> if allowed for the type and 
                        specified, otherwise it will be set to all zeros.  The size of the field is specified as part of
                        the <a href="https://msdn.microsoft.com/92373e0d-3fe1-4486-8e79-deb0fc24cb63">WS_VOID_DESCRIPTION</a>.  If a <b>WS_VOID_DESCRIPTION</b>is not specified, the field is interpreted as being size 0.
                    </li>
</ul>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ANY_ELEMENT_FIELD_MAPPING</a>, <b>WS_REPEATING_ANY_ELEMENT_FIELD_MAPPING</b>,
                    <b>WS_ELEMENT_FIELD_MAPPING</b>, <b>WS_ATTRIBUTE_FIELD_MAPPING</b>, 
                    <b>WS_ANY_CONTENT_FIELD_MAPPING</b> or
                    <b>WS_ANY_ATTRIBUTES_FIELD_MAPPING</b>.   This is 
                    used to discard the XML content when deserializing, or ignore the field when serializing.  
                    Since the values are not stored, a field of the structure is not required.  The field 
                    offset should be zero and the field size should be zero (which is the default if a 
                    <a href="https://msdn.microsoft.com/92373e0d-3fe1-4486-8e79-deb0fc24cb63">WS_VOID_DESCRIPTION</a> is not specified).  The <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> 
                    option should not be used.
                </li>
</ul>

### -field WS_ENUM_TYPE

Used when serializing a signed 32-bit integer which corresponds
                    to an enumerated value.
                

This type requires a <a href="https://msdn.microsoft.com/cf7c9254-c806-4ada-8852-beb6be5e81d9">WS_ENUM_DESCRIPTION</a> type description
                    to be supplied which provides information about the enumeration values 
                    and their corresponding serialized form.
                

This type can be used with the following <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ATTRIBUTE_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_CONTENT_TYPE_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ATTRIBUTE_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_TEXT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_POINTER</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
</ul>
A nil value is represented using a <b>NULL</b> pointer.
                

A <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a> may be specified for this type.
                    See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> to see
                    which field mapping values allow a default value to be specified.
                


### -field WS_DURATION_TYPE

Used when serializing a <a href="https://msdn.microsoft.com/ccb08c23-8c6f-4ea7-a43b-c30a0df75805">WS_DURATION</a>.
                

The <a href="https://msdn.microsoft.com/51084a56-f666-4ca0-b98c-9f41e28b99c0">WS_DURATION_DESCRIPTION</a> type description can optionally be
                    specified for this type in order to constrain the allowed values.
                

This type can be used with the following <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ATTRIBUTE_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_CONTENT_TYPE_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ATTRIBUTE_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_TEXT_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_NO_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_NILLABLE</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_POINTER</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_POINTER</a> | <b>WS_FIELD_NILLABLE</b> | <b>WS_FIELD_OPTIONAL</b> | <b>WS_FIELD_NILLABLE_ITEM</b></li>
</ul>
A nil value is represented using a <b>NULL</b> pointer.
                

A <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a> may be specified for this type.
                    See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> to see
                    which field mapping values allow a default value to be specified.
                


### -field WS_UNION_TYPE

Used when serializing a set of choices which correspond to a tagged union.
                

<pre class="syntax" xml:space="preserve"><code>
enum EnumType
{
// values identifying each choice
} value;
struct StructType
{
// value indicating which choice is set currently
EnumType selector;
union
{
// values corresponding to each choice
} value;
};</code></pre>
This type requires a <a href="https://msdn.microsoft.com/04eddc88-f0ba-4a0b-8078-12c0d955d055">WS_UNION_DESCRIPTION</a> type description
                    to be supplied which provides information about the choices and
                    their corresponding serialized form.
                

This type can be used with the following <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_TYPE_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_CONTENT_TYPE_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_CHOICE_FIELD_MAPPING</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_CHOICE_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                    </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a>
</li>
</ul>
This type does not support nil values.
                

This type does not support specifying a <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a>.
                    When used with <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a>, the default value in the 
                    union is specified using the nonEnumValue of the <a href="https://msdn.microsoft.com/04eddc88-f0ba-4a0b-8078-12c0d955d055">WS_UNION_DESCRIPTION</a>.
                


### -field WS_ANY_ATTRIBUTES_TYPE

Used when serializing a set of attributes that are not mapped to fields
                    using <a href="https://msdn.microsoft.com/6c428c99-755f-40ab-bc9e-e1a7a3d70c1d">WS_ANY_ATTRIBUTES</a>.
                

This type does not have an associated type description.
                

This type cannot be used with any <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_TYPE_MAPPING</a> values.
                

This type may only be used within a <a href="https://msdn.microsoft.com/8b562fab-f3c5-4732-b993-f7f61ca14ab6">WS_FIELD_DESCRIPTION</a>.
                

This type can be used with the following <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> values:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ANY_ATTRIBUTES_FIELD_MAPPING</a>
</li>
</ul>
This type can be used with the following <a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONS</a> values.  See the documentation for <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_FIELD_MAPPING</a> for which options are supported for a given field mapping value:
                

<ul>
<li>0
                </li>
</ul>
This type does not support nil values.
                

This type does not support specifying a <a href="https://msdn.microsoft.com/496b9ea6-2979-4245-ad07-9c62c396ebde">WS_DEFAULT_VALUE</a>.
                


## -remarks



Many of the <b>WS_TYPE</b>s have a corresponding type description structure
                which allows for additional information used to serialize or deserialize the
                type.
            

For example, the <b>WS_INT32_TYPE</b> has a <a href="https://msdn.microsoft.com/98761df2-b195-4f22-90ba-3dac8920f3ef">WS_INT32_DESCRIPTION</a>structure which allows for constraints on the deserialized values.  This is an optional
                type description (if not specified, the full 32-bit integer space is allowed).
            

Another example is the <b>WS_STRUCT_TYPE</b>, which allows for the specification of
                a user-defined structure with fields.  The fields are described in a 
                <a href="https://msdn.microsoft.com/b426a07e-9993-4cea-8847-fc80e9d0b451">WS_STRUCT_DESCRIPTION</a>.  This type description is required.
            

Type description pointers accompany <b>WS_TYPE</b> in the various APIs and structures 
                that are based on serialization.  This should be <b>NULL</b> or non-<b>NULL</b> based on whether or not
                the type description is not defined, optional or required.
            



