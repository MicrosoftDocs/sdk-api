---
UID: NS:webservices._WS_UNION_DESCRIPTION
title: "_WS_UNION_DESCRIPTION"
author: windows-sdk-content
description: Information about the choices within a union type. This is used with WS_UNION_TYPE.
old-location: wsw\ws_union_description.htm
old-project: wsw
ms.assetid: 04eddc88-f0ba-4a0b-8078-12c0d955d055
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WS_UNION_DESCRIPTION, WS_UNION_DESCRIPTION structure [Web Services for Windows], _WS_UNION_DESCRIPTION, webservices/WS_UNION_DESCRIPTION, wsw.ws_union_description
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: WS_UNION_DESCRIPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_UNION_DESCRIPTION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_UNION_DESCRIPTION structure


## -description



                Information about the choices within a union type.
                This is used with <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_UNION_TYPE</a>.
            


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
                    field is optional (<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a> was specified).
                


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
                    The field that uses <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ANY_ELEMENT_FIELD_MAPPING</a>, if present, should always
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
            

<pre class="syntax" xml:space="preserve"><code>// Enumeration of choices of different values
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
};</code></pre>

                The following examples illustrates initializing a union description
                for the previous example.  This example fills out the nameIndices 
                field, but this field could be <b>NULL</b> instead.
            

<pre class="syntax" xml:space="preserve"><code>WS_XML_STRING choiceAString = WS_XML_STRING_VALUE("choiceA");
WS_XML_STRING choiceANs = WS_XML_STRING_VALUE("http://examples.org/a");

WS_UNION_FIELD_DESCRIPTION fieldA = { };
fieldA.value = ChoiceA;
fieldA.field.localName = &amp;choiceAString;
fieldA.field.ns = &amp;choiceANs;
fieldA.field.type = WS_INT32_TYPE;
fieldA.field.offset = WsOffsetOf(StructType, value.a);

WS_XML_STRING choiceBString = WS_XML_STRING_VALUE("choiceB");
WS_XML_STRING choiceBNs = WS_XML_STRING_VALUE("http://examples.org/b");

WS_UNION_FIELD_DESCRIPTION fieldB = { };
fieldB.value = ChoiceB;
fieldB.field.localName = &amp;choiceBString;
fieldB.field.ns = &amp;choiceBNs;
fieldB.field.type = WS_STRING_TYPE;
fieldB.field.offset = WsOffsetOf(StructType, value.b);

// Sorted by ascending element name (first ns, then localName)
WS_UNION_FIELD_DESCRIPTION* fieldsArray[] =
{
    &amp;fieldA, // "http://example.com/a", "choiceA"
    &amp;fieldB, // "http://example.com/b", "choiceB"
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
</code></pre>

                The above would allow either of the following elements to
                appear:
            

<pre class="syntax" xml:space="preserve"><code>
&lt;choiceA xmlns="http://example.com/a"&gt;123&lt;/choiceA&gt;
&lt;choiceB xmlns="http://example.com/b"&gt;hello&lt;/choiceB&gt;
</code></pre>

                The following is an example of setting values:
            

<pre class="syntax" xml:space="preserve"><code>StructType structType;

// Set ChoiceA
structType.choice = ChoiceA;
structType.value.a = 123;

// Set ChoiceB
static const WS_STRING = WS_STRING_VALUE(L"hello");
structType.choice = ChoiceB;
structType.value.b = helloString;

// Set "none" choice
structType.choice = None;
</code></pre>

                The following is the grammar describing the order of the <a href="https://msdn.microsoft.com/8b562fab-f3c5-4732-b993-f7f61ca14ab6">WS_FIELD_DESCRIPTION</a>
                that make up a <b>WS_UNION_DESCRIPTION</b>.  The order is defined based on the
                mapping field of the <b>WS_FIELD_DESCRIPTION</b>.
            

<pre class="syntax" xml:space="preserve"><code>
Fields := ElementContentFields AnyElementField?
ElementContentFields := (ElementField | RepeatingElementField)*
ElementField := WS_ELEMENT_FIELD_MAPPING
RepeatingElementField := WS_REPEATING_ELEMENT_FIELD_MAPPING
AnyElementField := WS_ANY_ELEMENT_FIELD_MAPPING</code></pre>

                The <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ELEMENT_FIELD_MAPPING</a> and <b>WS_REPEATING_ELEMENT_FIELD_MAPPING</b>
                represent the element choices and their corresponding fields in the union.
            


                The <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ANY_ELEMENT_FIELD_MAPPING</a> is the field used when none of the
                other elements matched.
            


               The following restrictions apply to the field descriptions:
            

<ul>
<li>
<a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_REPEATING_ELEMENT_FIELD_MAPPING</a> may only be used when 
                a wrapper element name and namespace has been specified.
                </li>
<li>
<a href="https://msdn.microsoft.com/85271aa4-665e-413a-be42-da6f91706bf0">WS_FIELD_OPTIONAL</a> may not be used.
            </li>
</ul>


