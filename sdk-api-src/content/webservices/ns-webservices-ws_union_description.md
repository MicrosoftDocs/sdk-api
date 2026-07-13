---
UID: NS:webservices._WS_UNION_DESCRIPTION
title: WS_UNION_DESCRIPTION (webservices.h)
description: Information about the choices within a union type. This is used with WS_UNION_TYPE.
helpviewer_keywords: ["WS_UNION_DESCRIPTION","WS_UNION_DESCRIPTION structure [Web Services for Windows]","webservices/WS_UNION_DESCRIPTION","wsw.ws_union_description"]
old-location: wsw\ws_union_description.htm
tech.root: wsw
ms.assetid: 04eddc88-f0ba-4a0b-8078-12c0d955d055
ms.date: 12/05/2018
ms.keywords: WS_UNION_DESCRIPTION, WS_UNION_DESCRIPTION structure [Web Services for Windows], webservices/WS_UNION_DESCRIPTION, wsw.ws_union_description
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
req.typenames: WS_UNION_DESCRIPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_UNION_DESCRIPTION
 - webservices/_WS_UNION_DESCRIPTION
 - WS_UNION_DESCRIPTION
 - webservices/WS_UNION_DESCRIPTION
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
 - WS_UNION_DESCRIPTION
---

# WS_UNION_DESCRIPTION structure


## -description

Information about the choices within a union type.
                This is used with <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_UNION_TYPE</a>.

## -struct-fields

### -field size

The size in bytes of the structure.

### -field alignment

The alignment requirement of the structure.  This must be a power
                    of two between 1 and 8.

### -field fields

An array of pointers to the descriptions of the fields of the union.
                

See the Remarks section for information about ordering of the fields
                    in this array.

### -field fieldCount

The number of fields in the fields array.  Any part of the structure
                    that is not represented by a field will be left uninitialized.
                    Fields descriptions may reference the same offset of the structure
                    (for example if they are all part of a single union).

### -field enumOffset

The offset of the enumeration field which controls which choice is
                    selected within the union.  The size of the field is assumed to be
                    the size of an enumeration (32-bit signed integer).

### -field noneEnumValue

This value corresponds to the enum value used when none of the
                    choices are currently set.  This field is only used when the
                    field is optional (<a href="/windows/win32/api/webservices/ne-webservices-ws_xml_reader_encoding_type">WS_FIELD_OPTIONAL</a> was specified).

### -field valueIndices

This optional array provides information which can improve
                    the performance of looking up fields of the union either by
                    element or by enum value.  This array may <b>NULL</b>, in which case 
                    an O(n) lookup is used, which may be sufficient for small 
                    numbers of fields.
                

If non-<b>NULL</b>, the following must be true:
                

<ul>
<li>The fields array is required to be sorted by element, in ascending order.
                    When comparing an element the namespace should be compared first, then the local name.
                    Each of the names should be compared by performing a byte-wide comparison of the utf-8 string.
                    The field that uses <a href="/windows/desktop/api/webservices/ne-webservices-ws_field_mapping">WS_ANY_ELEMENT_FIELD_MAPPING</a>, if present, should always
                    be last in the fields array.
                    </li>
<li>The valueIndices array points to an array that has fieldCount items.  The valueIndices
                    array provides the indices of the items in the fields array as if they were sorted by 
                    value in ascending order.
                </li>
</ul>

## -remarks

This description assumes a structure which contains both the 
                selector value (an integer enumerated value) and a union which
                contains a field which corresponds to each of the possible
                choices, for example:
            


``` syntax
// Enumeration of choices of different values
enum Choice
{
    ChoiceA = 20,
    ChoiceB = 10,
    None = 0,
};

// Struct containing union of values, and enum "selector"
struct StructType
{
    Choice choice;
    union
    {
        int a;
        WS_STRING b;
    } value;
};
```

The following examples illustrates initializing a union description
for the previous example.  This example fills out the nameIndices 
field, but this field could be <b>NULL</b> instead.

``` syntax
WS_XML_STRING choiceAString = WS_XML_STRING_VALUE("choiceA");
WS_XML_STRING choiceANs = WS_XML_STRING_VALUE("http://examples.org/a");

WS_UNION_FIELD_DESCRIPTION fieldA = { };
fieldA.value = ChoiceA;
fieldA.field.localName = &choiceAString;
fieldA.field.ns = &choiceANs;
fieldA.field.type = WS_INT32_TYPE;
fieldA.field.offset = WsOffsetOf(StructType, value.a);

WS_XML_STRING choiceBString = WS_XML_STRING_VALUE("choiceB");
WS_XML_STRING choiceBNs = WS_XML_STRING_VALUE("http://examples.org/b");

WS_UNION_FIELD_DESCRIPTION fieldB = { };
fieldB.value = ChoiceB;
fieldB.field.localName = &choiceBString;
fieldB.field.ns = &choiceBNs;
fieldB.field.type = WS_STRING_TYPE;
fieldB.field.offset = WsOffsetOf(StructType, value.b);

// Sorted by ascending element name (first ns, then localName)
WS_UNION_FIELD_DESCRIPTION* fieldsArray[] =
{
    &fieldA, // "http://example.com/a", "choiceA"
    &fieldB, // "http://example.com/b", "choiceB"
};

// Sorted by ascending enum value
ULONG valueIndices[] =
{
    1, // ChoiceB (10)
    0, // ChoiceA (20)
};

WS_UNION_DESCRIPTION unionDescription;
unionDescription.size = sizeof(StructType);
unionDescription.alignment = __alignof(StructType);
unionDescription.fields = fieldsArray;
unionDescription.fieldCount = WsCountOf(fieldsArray);
unionDescription.enumOffset = WsOffsetOf(StructType, choice);
unionDescription.noneEnumValue = None;
unionDescription.valueIndices = valueIndices;

```

The above would allow either of the following elements to appear:

``` syntax
<choiceA xmlns="http://example.com/a">123</choiceA>
<choiceB xmlns="http://example.com/b">hello</choiceB>

```

The following is an example of setting values:

``` syntax
StructType structType;

// Set ChoiceA
structType.choice = ChoiceA;
structType.value.a = 123;

// Set ChoiceB
static const WS_STRING = WS_STRING_VALUE(L"hello");
structType.choice = ChoiceB;
structType.value.b = helloString;

// Set "none" choice
structType.choice = None;

```

The following is the grammar describing the order of the <a href="/windows/desktop/api/webservices/ns-webservices-ws_field_description">WS_FIELD_DESCRIPTION</a> that make up a <b>WS_UNION_DESCRIPTION</b>.  The order is defined based on the
                mapping field of the <b>WS_FIELD_DESCRIPTION</b>.
            


``` syntax

Fields := ElementContentFields AnyElementField?
ElementContentFields := (ElementField | RepeatingElementField)*
ElementField := WS_ELEMENT_FIELD_MAPPING
RepeatingElementField := WS_REPEATING_ELEMENT_FIELD_MAPPING
AnyElementField := WS_ANY_ELEMENT_FIELD_MAPPING
```

The <a href="/windows/desktop/api/webservices/ne-webservices-ws_field_mapping">WS_ELEMENT_FIELD_MAPPING</a> and <b>WS_REPEATING_ELEMENT_FIELD_MAPPING</b> represent the element choices and their corresponding fields in the union.
            

The <a href="/windows/desktop/api/webservices/ne-webservices-ws_field_mapping">WS_ANY_ELEMENT_FIELD_MAPPING</a> is the field used when none of the
                other elements matched.
            

The following restrictions apply to the field descriptions:
            

<ul>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_field_mapping">WS_REPEATING_ELEMENT_FIELD_MAPPING</a> may only be used when 
                a wrapper element name and namespace has been specified.
                </li>
<li>
<a href="/windows/win32/api/webservices/ne-webservices-ws_xml_reader_encoding_type">WS_FIELD_OPTIONAL</a> may not be used.
            </li>
</ul>
