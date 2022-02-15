---
UID: NS:webservices._WS_FIELD_DESCRIPTION
title: WS_FIELD_DESCRIPTION (webservices.h)
description: Represents serialization information about a field within a structure.
helpviewer_keywords: ["WS_FIELD_DESCRIPTION","WS_FIELD_DESCRIPTION structure [Web Services for Windows]","webservices/WS_FIELD_DESCRIPTION","wsw.ws_field_description"]
old-location: wsw\ws_field_description.htm
tech.root: wsw
ms.assetid: 8b562fab-f3c5-4732-b993-f7f61ca14ab6
ms.date: 12/05/2018
ms.keywords: WS_FIELD_DESCRIPTION, WS_FIELD_DESCRIPTION structure [Web Services for Windows], webservices/WS_FIELD_DESCRIPTION, wsw.ws_field_description
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: WS_FIELD_DESCRIPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_FIELD_DESCRIPTION
 - webservices/_WS_FIELD_DESCRIPTION
 - WS_FIELD_DESCRIPTION
 - webservices/WS_FIELD_DESCRIPTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_FIELD_DESCRIPTION
---

# WS_FIELD_DESCRIPTION structure


## -description

Represents serialization information about a field within a structure.

## -struct-fields

### -field mapping

Identifies how the field maps to the XML.  See <a href="/windows/desktop/api/webservices/ne-webservices-ws_field_mapping">WS_FIELD_MAPPING</a> for 
                    the ways that the field can be exposed in the XML content.

### -field localName

The XML local name to use for the field.
                

This field is required, except in the following case, where it may be <b>NULL</b>.
                    If the mapping field is <a href="/windows/desktop/api/webservices/ne-webservices-ws_field_mapping">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>, then
                    this identifies the local name of the "wrapper" element that is the parent element
                    of the array item elements.  Setting this field (and the ns field) to <b>NULL</b> will omit the wrapper element.  The ns and localName fields must be either both
                    specified or both <b>NULL</b>.

### -field ns

The XML namespace to use for the field.
                

This field is required, except in the following case, where it may be <b>NULL</b>.
                    If the mapping field is <a href="/windows/desktop/api/webservices/ne-webservices-ws_field_mapping">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>, then
                    this identifies the namespace of the "wrapper" element that is the parent element
                    of the array item elements.  Setting this field (and the localName field) to <b>NULL</b> will omit the wrapper element.  The ns and localName fields must be either both
                    specified or both <b>NULL</b>.

### -field type

The type of the field.  See <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_TYPE</a> for a list of supported types.

### -field typeDescription

Additional information about the type.  Each type has a different description
                    structure.  This may be <b>NULL</b>, depending on the <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_TYPE</a>.

### -field offset

The offset of the field within the containing structure.

### -field options

Additional flags for the field.  See <a href="/windows/win32/api/webservices/ne-webservices-ws_xml_reader_encoding_type">WS_FIELD_OPTIONS</a> for 
                    a list of flags.  If no flags are needed, this may be 0.

### -field defaultValue

Points to a default value for the field.  This is used in the following instances:
                

<ul>
<li>
<a href="/windows/win32/api/webservices/ne-webservices-ws_xml_reader_encoding_type">WS_FIELD_OPTIONAL</a> was specified, and the XML did not contain
                    the value.
                    </li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_field_mapping">WS_NO_FIELD_MAPPING</a> was specified.
                </li>
</ul>
If defaultValue is <b>NULL</b>, then it is the same as having a default value
                    of all zero's.

### -field countOffset

The structure offset of the ULONG field that represents the number of items in the array.
                

This field is used when using <a href="/windows/desktop/api/webservices/ne-webservices-ws_field_mapping">WS_REPEATING_ELEMENT_FIELD_MAPPING</a> or array types 
                    (<a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_CHAR_ARRAY_TYPE</a>, <b>WS_UTF8_ARRAY_TYPE</b>, <b>WS_BYTE_ARRAY_TYPE</b>).  
                    In other cases, it does not need to be specified (it can be 0).

### -field itemLocalName

The XML local name to use for the repeating elements when
                    using <a href="/windows/desktop/api/webservices/ne-webservices-ws_field_mapping">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>.
                

In other cases this field does not need to be specified (it can be <b>NULL</b>).

### -field itemNs

The XML namespace to use for the repeating elements when
                    using <a href="/windows/desktop/api/webservices/ne-webservices-ws_field_mapping">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>.
                

In other cases this field does not need to be specified (it can be <b>NULL</b>).

### -field itemRange

The minimum and maximum number of repeating elements
                    that may appear when using <a href="/windows/desktop/api/webservices/ne-webservices-ws_field_mapping">WS_REPEATING_ELEMENT_FIELD_MAPPING</a>,
                    <b>WS_REPEATING_ELEMENT_CHOICE_FIELD_MAPPING</b>,
                    or <b>WS_REPEATING_ANY_ELEMENT_FIELD_MAPPING</b>.
                If not specified (<b>NULL</b>), the minimum is 0, and the maximum is MAX ULONG.
            

In other cases this field does not need to be specified (it can be <b>NULL</b>).