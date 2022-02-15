---
UID: NS:webservices._WS_STRUCT_DESCRIPTION
title: WS_STRUCT_DESCRIPTION (webservices.h)
description: Information about C struct type, and how it maps to an XML element. This is used with WS_STRUCT_TYPE.
helpviewer_keywords: ["WS_STRUCT_DESCRIPTION","WS_STRUCT_DESCRIPTION structure [Web Services for Windows]","webservices/WS_STRUCT_DESCRIPTION","wsw.ws_struct_description"]
old-location: wsw\ws_struct_description.htm
tech.root: wsw
ms.assetid: b426a07e-9993-4cea-8847-fc80e9d0b451
ms.date: 12/05/2018
ms.keywords: WS_STRUCT_DESCRIPTION, WS_STRUCT_DESCRIPTION structure [Web Services for Windows], webservices/WS_STRUCT_DESCRIPTION, wsw.ws_struct_description
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
req.typenames: WS_STRUCT_DESCRIPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_STRUCT_DESCRIPTION
 - webservices/_WS_STRUCT_DESCRIPTION
 - WS_STRUCT_DESCRIPTION
 - webservices/WS_STRUCT_DESCRIPTION
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
 - WS_STRUCT_DESCRIPTION
---

# WS_STRUCT_DESCRIPTION structure


## -description

Information about C struct type, and how it maps to an XML element.
                This is used with <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_STRUCT_TYPE</a>.

## -struct-fields

### -field size

The size of the structure, in bytes.

### -field alignment

The alignment requirement of the structure.  This must be a power
                    of two between 1 and 8.

### -field fields

An array of pointers to the descriptions of the fields of the structure.
                

See the Remarks section for information about ordering of the fields
                    in this array.

### -field fieldCount

The number of fields in the fields array.  Any part of the structure
                    that is not represented by a field will be left uninitialized.
                    No two fields descriptions may reference the same offset of the structure.

### -field typeLocalName

The XML type name of the structure.  This is only used when 
                    structures derive from other structures, and may be <b>NULL</b> otherwise.

### -field typeNs

The XML type namespace of the structure.  This is only used when 
                    structures derive from other structures, and may be <b>NULL</b> otherwise.

### -field parentType

The type this type is derived from.  This is only used when 
                    structures derive from other structures, and may be <b>NULL</b> otherwise.

### -field subTypes

An array of pointers to derived types.  This is only used when 
                    structures derive from other structures, and may be <b>NULL</b> otherwise.

### -field subTypeCount

The number of types in the subTypes array.  This is only used when 
                    structures derive from other structures, and may be <b>NULL</b> otherwise.

### -field structOptions

## -remarks

The following is the grammar describing the order of the fields
                within a structure.  The order is defined based on the
                mapping field of each <a href="/windows/desktop/api/webservices/ns-webservices-ws_field_description">WS_FIELD_DESCRIPTION</a>.
            


``` syntax

Fields := TypeAttributeField? AttributeField* ContentFields UnmappedFields*
ContentFields := TextContentField | ElementContentFields
ElementContentFields := ElementContentField* ? AnyElementField?
ElementContentField := ElementField | RepeatingElementField | ElementChoiceField | RepeatingElementChoiceField
ElementField := WS_ELEMENT_FIELD_MAPPING
RepeatingElementField := WS_REPEATING_ELEMENT_FIELD_MAPPING
ElementChoiceField := WS_ELEMENT_CHOICE_FIELD_MAPPING
RepeatingElementChoiceField := WS_REPEATING_ELEMENT_CHOICE_FIELD_MAPPING
AnyElementField := WS_ANY_ELEMENT_FIELD_MAPPING
TextContentField := WS_TEXT_FIELD_MAPPING
UnmappedField := WS_NO_FIELD_MAPPING
TypeAttributeField := WS_TYPE_ATTRIBUTE_FIELD_MAPPING
AttributeField := WS_ATTRIBUTE_FIELD_MAPPING
```

Note that the fields descriptions of a structure are serialized and deserialized in
                the order specified.  The deserialization process is "greedy", that is, as much content
                as will match the definition a specific field description will be consumed before
                the next field description will be considered.  This approach resolves any ambiguity
                when content could match the current field description or a following one.
            

The deserialization process is also restrictive. All the content must be deserialized according
                to the field descriptions. By default any unhandled elements and attributes will cause the deserialization
                process to fail. However, trailing contents of the element are ignored and discarded when
                <a href="/windows/win32/api/webservices/ne-webservices-ws_xml_reader_input_type">WS_STRUCT_IGNORE_TRAILING_ELEMENT_CONTENT</a> flag is set. Similarly, unhandled attributes are
                ignored and discarded when <b>WS_STRUCT_IGNORE_UNHANDLED_ATTRIBUTES</b> flag is set.
            

Note that since the <a href="/windows/desktop/api/webservices/ns-webservices-ws_field_description">WS_FIELD_DESCRIPTION</a> structures determine the location
                of the actual field within the structure using an offset, there is no restriction
                as to the actual order of the fields within the structure.
            

When one structure derives from (extends) another, the fields for both structures
                must be included in the derived struct description, and the above grammar must be
                maintained.  For example:
            


``` syntax
struct BaseStructure
{
    const WS_STRUCT_DESCRIPTION* _type;
    int baseAttribute;
    int baseElement;
};

// BaseStructure field descriptions:
//    WS_TYPE_ATTRIBUTE_FIELD_MAPPING       // _type
//    WS_ATTRIBUTE_FIELD_MAPPING            // baseAttribute
//    WS_ELEMENT_FIELD_MAPPING              // baseElement

struct DerivedStructure
{
    struct BaseStructure _base;
    int derivedAttribute;
    int derivedElement;
};

// DerivedStructure field descriptions:
//    WS_TYPE_ATTRIBUTE_FIELD_MAPPING       // _type
//    WS_ATTRIBUTE_FIELD_MAPPING            // baseAttribute
//    WS_ATTRIBUTE_FIELD_MAPPING            // derivedAttribute
//    WS_ELEMENT_FIELD_MAPPING              // baseElement
//    WS_ELEMENT_FIELD_MAPPING              // derivedElement
```

