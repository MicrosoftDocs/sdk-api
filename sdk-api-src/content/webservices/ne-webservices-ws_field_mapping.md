---
UID: NE:webservices.__unnamed_enum_82
title: WS_FIELD_MAPPING (webservices.h)
description: Specifies how a field of a structure is represented in XML. This is used within a WS_FIELD_DESCRIPTION.
helpviewer_keywords: ["WS_ANY_ATTRIBUTES_FIELD_MAPPING","WS_ANY_CONTENT_FIELD_MAPPING","WS_ATTRIBUTE_FIELD_MAPPING","WS_ELEMENT_CHOICE_FIELD_MAPPING","WS_ELEMENT_FIELD_MAPPING","WS_FIELD_MAPPING","WS_FIELD_MAPPING enumeration [Web Services for Windows]","WS_NO_FIELD_MAPPING","WS_REPEATING_ANY_ELEMENT_FIELD_MAPPING","WS_REPEATING_ELEMENT_CHOICE_FIELD_MAPPING","WS_REPEATING_ELEMENT_FIELD_MAPPING","WS_TEXT_FIELD_MAPPING","WS_TYPE_ATTRIBUTE_FIELD_MAPPING","WS_XML_ATTRIBUTE_FIELD_MAPPING","webservices/WS_ANY_ATTRIBUTES_FIELD_MAPPING","webservices/WS_ANY_CONTENT_FIELD_MAPPING","webservices/WS_ATTRIBUTE_FIELD_MAPPING","webservices/WS_ELEMENT_CHOICE_FIELD_MAPPING","webservices/WS_ELEMENT_FIELD_MAPPING","webservices/WS_FIELD_MAPPING","webservices/WS_NO_FIELD_MAPPING","webservices/WS_REPEATING_ANY_ELEMENT_FIELD_MAPPING","webservices/WS_REPEATING_ELEMENT_CHOICE_FIELD_MAPPING","webservices/WS_REPEATING_ELEMENT_FIELD_MAPPING","webservices/WS_TEXT_FIELD_MAPPING","webservices/WS_TYPE_ATTRIBUTE_FIELD_MAPPING","webservices/WS_XML_ATTRIBUTE_FIELD_MAPPING","wsw.ws_field_mapping"]
old-location: wsw\ws_field_mapping.htm
tech.root: wsw
ms.assetid: 14f4dbc6-0870-4b1c-8f6b-544f771771e8
ms.date: 12/05/2018
ms.keywords: WS_ANY_ATTRIBUTES_FIELD_MAPPING, WS_ANY_CONTENT_FIELD_MAPPING, WS_ATTRIBUTE_FIELD_MAPPING, WS_ELEMENT_CHOICE_FIELD_MAPPING, WS_ELEMENT_FIELD_MAPPING, WS_FIELD_MAPPING, WS_FIELD_MAPPING enumeration [Web Services for Windows], WS_NO_FIELD_MAPPING, WS_REPEATING_ANY_ELEMENT_FIELD_MAPPING, WS_REPEATING_ELEMENT_CHOICE_FIELD_MAPPING, WS_REPEATING_ELEMENT_FIELD_MAPPING, WS_TEXT_FIELD_MAPPING, WS_TYPE_ATTRIBUTE_FIELD_MAPPING, WS_XML_ATTRIBUTE_FIELD_MAPPING, webservices/WS_ANY_ATTRIBUTES_FIELD_MAPPING, webservices/WS_ANY_CONTENT_FIELD_MAPPING, webservices/WS_ATTRIBUTE_FIELD_MAPPING, webservices/WS_ELEMENT_CHOICE_FIELD_MAPPING, webservices/WS_ELEMENT_FIELD_MAPPING, webservices/WS_FIELD_MAPPING, webservices/WS_NO_FIELD_MAPPING, webservices/WS_REPEATING_ANY_ELEMENT_FIELD_MAPPING, webservices/WS_REPEATING_ELEMENT_CHOICE_FIELD_MAPPING, webservices/WS_REPEATING_ELEMENT_FIELD_MAPPING, webservices/WS_TEXT_FIELD_MAPPING, webservices/WS_TYPE_ATTRIBUTE_FIELD_MAPPING, webservices/WS_XML_ATTRIBUTE_FIELD_MAPPING, wsw.ws_field_mapping
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
req.typenames: WS_FIELD_MAPPING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_FIELD_MAPPING
 - webservices/WS_FIELD_MAPPING
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
 - WS_FIELD_MAPPING
---

# WS_FIELD_MAPPING enumeration


## -description

Specifies how a field of a structure is represented in XML.  This is used within
                a <a href="/windows/desktop/api/webservices/ns-webservices-ws_field_description">WS_FIELD_DESCRIPTION</a>.

## -enum-fields

### -field WS_TYPE_ATTRIBUTE_FIELD_MAPPING:0

The field corresponds to the XML type attribute (xsi:type).  This
                    can only be used with <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_DESCRIPTION_TYPE</a>.  
                


``` syntax

struct Base
{
    WS_STRUCT_DESCRIPTION* type;

    // ... base fields ...
};

struct Derived : Base
{
    // ... derived fields ...
};

struct Struct
{
    Base* field;
};

Derived derived;
derived.type = &amp;DerivedStructDescription;
Struct s;
s.field = &amp;derived;

&lt;Struct&gt;
    &lt;field xsi:type='Derived'&gt;
        // ... base fields ...
        // ... derived fields ...
    &lt;/field&gt;
&lt;/Struct&gt;

```

This mapping does not support specifying a <a href="/windows/desktop/api/webservices/ns-webservices-ws_default_value">WS_DEFAULT_VALUE</a>.

### -field WS_ATTRIBUTE_FIELD_MAPPING:1

The field corresponds to a single attribute.
                

The field's localName/ns are used as the XML attribute name and namespace.
                

Unless specified, the attribute must appear in the XML.
                    If <a href="/windows/win32/api/webservices/ne-webservices-ws_xml_reader_encoding_type">WS_FIELD_OPTIONAL</a> is specified, then the attribute
                    is not required to appear in the XML.  If optional and not
                    present, then the field is set to the <a href="/windows/desktop/api/webservices/ns-webservices-ws_default_value">WS_DEFAULT_VALUE</a>,
                    or zero if the default value is not specified.
                


``` syntax

struct Struct
{
    int field;
};

Struct s;
s.field = 1;

&lt;Struct field='1'/&gt;

```

To discard the attribute, a <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_VOID_TYPE</a> should be used.
                    In this case, a field is not required in the structure.
                    See <b>WS_VOID_TYPE</b> for more information.

### -field WS_ELEMENT_FIELD_MAPPING:2

The field corresponds to a single element.
                

The field's localName/ns are used as the XML element name and namespace.
                

Unless specified, the element must appear in the XML.
                    If <a href="/windows/win32/api/webservices/ne-webservices-ws_xml_reader_encoding_type">WS_FIELD_OPTIONAL</a> is specified, then the element
                    is not required to appear in the XML.  If optional and not
                    present, then the field is set to the <a href="/windows/desktop/api/webservices/ns-webservices-ws_default_value">WS_DEFAULT_VALUE</a>,
                    or zero if the default value is not specified.
                


``` syntax

struct Struct
{
    int field;
};

Struct s;
s.field = 1;

&lt;Struct&gt;
    &lt;field&gt;1&lt;/field&gt;
&lt;/Struct&gt;

```

To discard the element, a <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_VOID_TYPE</a> should be used.
                    In this case, a field is not required in the structure.
                    See <b>WS_VOID_TYPE</b> for more information.

### -field WS_REPEATING_ELEMENT_FIELD_MAPPING:3

The field corresponds to a repeating set of elements.
                

The field's localName/ns are used as the XML element
                    name and namespace to use for the wrapper element (the element
                    which is the parent of the repeating elements).  If no wrapper
                    element is desired, then both localName/ns should be <b>NULL</b>.
                

If a wrapper element has been specified, the wrapper element must appear
                  in the XML if repeating element count is not 0.  A <a href="/windows/desktop/api/webservices/ns-webservices-ws_default_value">WS_DEFAULT_VALUE</a> may 
                  not be specified for this field mapping. 
                

The itemLocalName and itemNs are used as the XML element
                    name and namespace for the repeating element.
                


``` syntax

struct Struct
{
    int* field;
    ULONG fieldCount;
};

int values[] = { 1, 2 };
Struct s;
s.field = values;
s.fieldCount = 2;

// with wrapper element specified
&lt;Struct&gt;
    &lt;field&gt;
        &lt;item&gt;1&lt;/item&gt;
        &lt;item&gt;2&lt;/item&gt;
    &lt;/field&gt;
&lt;/Struct&gt;

// with no wrapper element specified
&lt;Struct&gt;
    &lt;item&gt;1&lt;/item&gt;
    &lt;item&gt;2&lt;/item&gt;
&lt;/Struct&gt;
```

The number of elements in the deserialized array can be constrained
                    by specifying a non-<b>NULL</b><a href="/windows/desktop/api/webservices/ns-webservices-ws_item_range">WS_ITEM_RANGE</a> structure that is
                    part of the <a href="/windows/desktop/api/webservices/ns-webservices-ws_field_description">WS_FIELD_DESCRIPTION</a>.

### -field WS_TEXT_FIELD_MAPPING:4

The field corresponds to the entire character content of the element.
                    When this mapping is used, child elements are not allowed.
                

This mapping is commonly used in conjunction with <a href="/windows/desktop/api/webservices/ne-webservices-ws_field_mapping">WS_ATTRIBUTE_FIELD_MAPPING</a> to define a structure which maps to an element containing some text and attributes (but no
                    child elements).
                


``` syntax

struct Struct
{
    int field;
};

Struct s;
s.field = 1;

&lt;Struct&gt;1&lt;/Struct&gt;

```

This mapping does not support specifying a <a href="/windows/desktop/api/webservices/ns-webservices-ws_default_value">WS_DEFAULT_VALUE</a>.

### -field WS_NO_FIELD_MAPPING:5

The field is neither serialized or deserialized.
                

The field is ignored when serializing, and is initialized to the
                    default value when deserializing.
                

If the field maps to one of the existing types (for example <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_INT32_TYPE</a>),
                    then the type can be specified.  If the type of the field is not one of
                    the existing types, then <b>WS_VOID_TYPE</b> can be used to specify
                    a field of an arbitrary type and size.
                

A <a href="/windows/desktop/api/webservices/ns-webservices-ws_default_value">WS_DEFAULT_VALUE</a> may be specified to provide the value
                    to initialize the field to when deserializing the field.  If a default
                    value is not specified, then the field will be initialized to zero.
                

The field mapping can be used with <a href="/windows/win32/api/webservices/ne-webservices-ws_xml_reader_encoding_type">WS_FIELD_OPTIONS</a> value of 0 only.
                


``` syntax

struct Struct
{
    int field;
};

Struct s;
s.field = 1;

&lt;Struct/&gt;

```


### -field WS_XML_ATTRIBUTE_FIELD_MAPPING:6

The field corresponds to a reserved xml attribute (such as xml:lang).
                

The field's localName is used to identify the XML attribute name.
                

Unless <a href="/windows/win32/api/webservices/ne-webservices-ws_xml_reader_encoding_type">WS_FIELD_OPTIONAL</a>  is specified, the attribute must 
                    appear in the XML.  If <b>WS_FIELD_OPTIONAL</b> is specified, 
                    then the attribute is not required to appear in the XML.  If optional and not
                    present, then the field is set to the <a href="/windows/desktop/api/webservices/ns-webservices-ws_default_value">WS_DEFAULT_VALUE</a>,
                    or zero if the default value is not specified.
                


``` syntax

struct Struct
{
    WS_STRING field;
};

Struct s;
s.field = ...; // 'us-en';

// Example of xml:lang
&lt;Struct xml:lang='us-en'/&gt;

s.field = ...; // 'true'

// Example of xml:space
&lt;Struct xml:space='true'&gt;
```


### -field WS_ELEMENT_CHOICE_FIELD_MAPPING:7

The field corresponds to a choice among a set of possible
                    elements.  Each element maps to one of the fields of a union.
                    Each field of the union has a corresponding enum value, which is 
                    used to identify the current choice.
                


``` syntax

// Enumeration of choices of different values
enum Choice
{
    ChoiceA = 10,
    ChoiceB = 20,
    None = 0,
};

// Struct containing union of values, and enum 'selector'
struct Struct
{
    Choice choice;
    union
    {
        int a;          // valid when choice is ChoiceA
        WS_STRING b;    // valid when choice is ChoiceB
    } value;
};                    

```

This field mapping must be used with <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_UNION_TYPE</a>.
                    The names and namespaces of the element choices are specified in the
                    <a href="/windows/desktop/api/webservices/ns-webservices-ws_union_description">WS_UNION_DESCRIPTION</a>.  The field's localName 
                    and ns should be <b>NULL</b>.
                

Unless <a href="/windows/win32/api/webservices/ne-webservices-ws_xml_reader_encoding_type">WS_FIELD_OPTIONAL</a>  is specified, one of the 
                    elements must appear in the XML.  If <b>WS_FIELD_OPTIONAL</b> is specified,
                    then none of the elements are required to appear in the XML.  If optional and none
                    of the elements are present, then the field's selector value is set to the
                    none value of the enumeration (as specified in the noneEnumValue field of
                    the <a href="/windows/desktop/api/webservices/ns-webservices-ws_union_description">WS_UNION_DESCRIPTION</a>).  Due to the fact that the nonEnumValue
                    is used as the default value, this mapping value does not support 
                    specifying a <a href="/windows/desktop/api/webservices/ns-webservices-ws_default_value">WS_DEFAULT_VALUE</a>.
                


``` syntax

Struct s;
s.choice = ChoiceA;
s.value.a = 123;

&lt;Struct&gt;
    &lt;choiceA&gt;123&lt;/choiceA&gt;
&lt;/Struct&gt;

Struct S;
s.choice = ChoiceB;
s.value.b = ...; // 'hello'

&lt;Struct&gt;
    &lt;choiceB&gt;hello&lt;/choiceB&gt;
&lt;/Struct&gt;

Struct S;
s.choice = None;

&lt;Struct&gt;
&lt;/Struct&gt;                    
```

The field corresponds to a choice among a set of possible
                    elements.  Each element maps to one of the fields of a union.
                    Each field of the union has a corresponding enum value, which is 
                    used to identify the current choice.
                


``` syntax

// Enumeration of choices of different values
enum Choice
{
    ChoiceA = 10,
    ChoiceB = 20,
    None = 0,
};

// Struct containing union of values, and enum &amp;quot;selector&amp;quot;
struct Struct
{
    Choice choice;
    union
    {
        int a;          // valid when choice is ChoiceA
        WS_STRING b;    // valid when choice is ChoiceB
    } value;
};
```

This field mapping must be used with <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_UNION_TYPE</a>.
                    The names and namespaces of the element choices are specified in the
                    <a href="/windows/desktop/api/webservices/ns-webservices-ws_union_description">WS_UNION_DESCRIPTION</a>.  The field's localName 
                    and ns should be <b>NULL</b>.
                

Unless <a href="/windows/win32/api/webservices/ne-webservices-ws_xml_reader_encoding_type">WS_FIELD_OPTIONAL</a>  is specified, one of the 
                    elements must appear in the XML.  If <b>WS_FIELD_OPTIONAL</b> is specified,
                    then none of the elements are required to appear in the XML.  If optional and none
                    of the elements are present, then the field's selector value is set to the
                    none value of the enumeration (as specified in the noneEnumValue field of
                    the <a href="/windows/desktop/api/webservices/ns-webservices-ws_union_description">WS_UNION_DESCRIPTION</a>).  Due to the fact that the nonEnumValue
                    is used as the default value, this mapping value does not support 
                    specifying a <a href="/windows/desktop/api/webservices/ns-webservices-ws_default_value">WS_DEFAULT_VALUE</a>.
                


``` syntax

Struct s;
s.choice = ChoiceA;
s.value.a = 123;

&lt;Struct&gt;
    &lt;choiceA&gt;123&lt;/choiceA&gt;
&lt;/Struct&gt;

Struct S;
s.choice = ChoiceB;
s.value.b = ...; // &amp;quot;hello&amp;quot;

&lt;Struct&gt;
    &lt;choiceB&gt;hello&lt;/choiceB&gt;
&lt;/Struct&gt;

Struct S;
s.choice = None;

&lt;Struct&gt;
&lt;/Struct&gt;
```

The selector value indicates which of the fields of the
                    union are set.  Other fields are left uninitialized when
                    the value is deserialized.  An application should always
                    consult the selector value to verify that a field of the
                    union is accessible.

### -field WS_REPEATING_ELEMENT_CHOICE_FIELD_MAPPING:8

The field corresponds to a repeating set of element choices.
                

Each item is represented by a union with selector value.
                    This mapping must be used with <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_UNION_TYPE</a>.
                

The field's localName/ns are used as the XML element
                    name and namespace to use for the wrapper element (the element
                    which is the parent of the repeating elements).  If no wrapper
                    element is desired, then both localName/ns should be <b>NULL</b>.
                

If a wrapper element has been specified, the wrapper element must appear
                  in the XML if repeating element count is not 0.  A <a href="/windows/desktop/api/webservices/ns-webservices-ws_default_value">WS_DEFAULT_VALUE</a> may
                  not be specified for this field mapping.
                

The itemLocalName and itemNs fields must be <b>NULL</b>.  The XML element
                    name and namespace are defined in the <a href="/windows/desktop/api/webservices/ns-webservices-ws_union_description">WS_UNION_DESCRIPTION</a>.
                


``` syntax

struct Struct2
{
    Struct* field;      // see WS_UNION_DESCRIPTION for definition of Struct
    ULONG fieldCount;
};

StructType values[2];
values[0].choice = ChoiceA;
values[0].values.a = 123;
values[1].choice = ChoiceB;
values[1].values.b = ...; // hello

Struct2 s2;
s2.field = values;
s2.fieldCount = 2;

// with wrapper element specified
&lt;Struct2&gt;
    &lt;field&gt;
        &lt;item&gt;123&lt;/item&gt;
        &lt;item&gt;hello&lt;/item&gt;
    &lt;/field&gt;
&lt;/Struct2&gt;

// with no wrapper element specified
&lt;Struct2&gt;
    &lt;item&gt;123&lt;/item&gt;
    &lt;item&gt;hello&lt;/item&gt;
&lt;/Struct2&gt;

```

The number of elements in the deserialized array can be constrained
                    by specifying a non-<b>NULL</b><a href="/windows/desktop/api/webservices/ns-webservices-ws_item_range">WS_ITEM_RANGE</a> structure that is
                    part of the <a href="/windows/desktop/api/webservices/ns-webservices-ws_field_description">WS_FIELD_DESCRIPTION</a>.

### -field WS_ANY_ELEMENT_FIELD_MAPPING:9

### -field WS_REPEATING_ANY_ELEMENT_FIELD_MAPPING:10

The field is used to discard or store a sequence of elements
                    with any name and namespace.
                

To store the elements, a <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_XML_BUFFER_TYPE</a> should
                    be used.  This corresponds to an array of <a href="/windows/desktop/wsw/ws-xml-buffer">WS_XML_BUFFER</a>s,
                    as follows:
                


``` syntax

struct Struct
{
    // ... known fields ...
    WS_XML_BUFFER** fields;
    ULONG fieldCount;
    // ... known fields ...
};

Struct s;
s.fields = ...; // { '&lt;unknown1/&gt;', '&lt;unknown2/&gt;'; }
s.fieldCount = 2;

&lt;Struct&gt;
    ... known fields ...
    &lt;unknown1/&gt;
    &lt;unknown2/&gt;
    ... known fields ...
&lt;/Struct&gt;

```

To discard the elements, a <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_VOID_TYPE</a> should be used.
                    In this case, a field is not required in the structure.  See <b>WS_VOID_TYPE</b> for
                    more information.
                

The number of elements allowed during deserialization can be constrained
                    by specifying a non-<b>NULL</b><a href="/windows/desktop/api/webservices/ns-webservices-ws_item_range">WS_ITEM_RANGE</a> structure that is
                    part of the <a href="/windows/desktop/api/webservices/ns-webservices-ws_field_description">WS_FIELD_DESCRIPTION</a>.
                

This mapping does not support specifying a <a href="/windows/desktop/api/webservices/ns-webservices-ws_default_value">WS_DEFAULT_VALUE</a>.

### -field WS_ANY_CONTENT_FIELD_MAPPING:11

The field is used to discard or store any remaining content
                    (any mixture of text or elements) that occurs before the end 
                    of an element.
                

To store the elements, a <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_XML_BUFFER_TYPE</a> should
                    be used, as follows:
                


``` syntax

struct Struct
{
    // ... known fields ...
    WS_XML_BUFFER* field;
};

Struct s;
s.field = ...; // 'text1&lt;unknown1/&gt;text2&lt;unknown2/&gt;'

&lt;Struct&gt;
    ... known fields ...
    text1
    &lt;unknown1/&gt;
    text2
    &lt;unknown2/&gt;
&lt;/Struct&gt;

```

To discard the elements, a <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_VOID_TYPE</a> should be used.
                    In this case, a field is not required in the structure.  
                    See <b>WS_VOID_TYPE</b> for more information.
                

This mapping does not support specifying a <a href="/windows/desktop/api/webservices/ns-webservices-ws_default_value">WS_DEFAULT_VALUE</a>.

### -field WS_ANY_ATTRIBUTES_FIELD_MAPPING:12

The field is used to discard or store any attributes which were not
                    mapped using other <a href="/windows/desktop/api/webservices/ne-webservices-ws_field_mapping">WS_FIELD_MAPPING</a> values. 
                

If this field mapping is not specified, then unmapped attributes
                    will cause an error when deserializing.
                

The name field of the <a href="/windows/desktop/api/webservices/ns-webservices-ws_field_description">WS_FIELD_DESCRIPTION</a> must be <b>NULL</b>.
                

The ns field of the <a href="/windows/desktop/api/webservices/ns-webservices-ws_field_description">WS_FIELD_DESCRIPTION</a> restricts the
                    namespace of the attributes allowed as follows:
                    <ul>
<li>If the ns field is <b>NULL</b>, then there is no restriction.  The
                        <a href="/windows/win32/api/webservices/ne-webservices-ws_xml_reader_encoding_type">WS_FIELD_OTHER_NAMESPACE</a> field option must be not set in this
                        case.
                        </li>
<li>If the ns field is non-<b>NULL</b>, and the field option
                        <a href="/windows/win32/api/webservices/ne-webservices-ws_xml_reader_encoding_type">WS_FIELD_OTHER_NAMESPACE</a> is not set for the field, then
                        the attribute must have the same namespace as was specified in the ns field.
                        </li>
<li>If the ns field is non-<b>NULL</b>, and the field option
                        <a href="/windows/win32/api/webservices/ne-webservices-ws_xml_reader_encoding_type">WS_FIELD_OTHER_NAMESPACE</a> is set for the field, then the
                        attribute must have a different namespace than was specified
                        in the ns field.
                    </li>
</ul>


To store the attributes, <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_ANY_ATTRIBUTES_TYPE</a> should be
                    used.  This correspond to <a href="/windows/desktop/api/webservices/ns-webservices-ws_any_attributes">WS_ANY_ATTRIBUTES</a> as follows:
                


``` syntax

struct Struct
{
    // ... known attributes ...
    WS_ANY_ATTRIBUTES field;
    // ... other content ...
};

Struct s;
s.field = ...; // 'unknown'/'http://example.com'/'value'

&lt;Struct 
    ... known attributes ... 
    xmlns:a='http://example.com' a:unknown='value'&gt;

    ... other content ...
&lt;/Struct&gt;

```

To discard the unmapped attributes, a <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_VOID_TYPE</a> should be used.
                    In this case, a field is not required in the structure.
                    See <b>WS_VOID_TYPE</b> for more information.
                

This mapping does not support specifying a <a href="/windows/desktop/api/webservices/ns-webservices-ws_default_value">WS_DEFAULT_VALUE</a>.

## -remarks

The <b>WS_FIELD_MAPPING</b> indicates how different parts of the XML content
                maps to the fields of a structure.  For example, <b>WS_ELEMENT_FIELD_MAPPING</b> can
                be used to map the value of a child element, and <b>WS_ATTRIBUTE_FIELD_MAPPING</b> can be used to map an attribute.  Any XML content that is read that is not explicitly
                mapped will cause <b>WS_E_INVALID_FORMAT</b> to be returned when the XML
                is deserialized.
             (See <a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.)

The order of the <a href="/windows/desktop/api/webservices/ns-webservices-ws_field_description">WS_FIELD_DESCRIPTION</a> within a <a href="/windows/desktop/api/webservices/ns-webservices-ws_struct_description">WS_STRUCT_DESCRIPTION</a> is determined by the <b>WS_FIELD_MAPPING</b> value of the <b>WS_FIELD_DESCRIPTION</b>.
                See <b>WS_STRUCT_DESCRIPTION</b> for more information on the ordering.
