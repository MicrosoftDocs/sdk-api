---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _WS_ENUM_DESCRIPTION structure


## -description



                A type description that is used with <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_ENUM_TYPE</a> and is required. 
                It provides information used in serializing and deserializing
                values of an enumeration.
            


## -struct-fields




### -field values


                    Points to an array of enumeration values and their
                    corresponding names.
                


                    There must not be duplicate values or names in
                    the array.
                


### -field valueCount


                    The number of items in the values array.
                


### -field maxByteCount


                    The length, in UTF8 bytes, of the longest name
                    in the values array.
                


### -field nameIndices

An optional array that provides information which can improve
                    the performance of mapping enumeration values to names and back.
                    This array may <b>NULL</b>, in which case an O(n) lookup is used,
                    which may be sufficient for small numbers of enumerated values.
                


                    If non-<b>NULL</b>, the following must be true:
                

<ul>
<li>The values array is required to be sorted by value, in ascending order.
                    </li>
<li>The nameIndices array points to an array that has valueCount items. 
                    </li>
<li>The nameIndices array provides the indices of the items in
                    the values array as if they were sorted by name in ascending order.
                    The names should by sorted by performing a byte-wise comparison of the utf-8 string.
                </li>
</ul>

## -remarks




                The following examples illustrates initializing an enum description.  This 
                example illustrates the use of the nameIndices field, but this field could
                be <b>NULL</b> instead.
            

<pre class="syntax" xml:space="preserve"><code>
enum
{
    Red = 10,
    Green = 20,
    Blue = 30,
};

WS_XML_STRING redString = WS_XML_STRING_VALUE("red");
WS_XML_STRING greenString = WS_XML_STRING_VALUE("green");
WS_XML_STRING blueString = WS_XML_STRING_VALUE("blue");

// sorted by ascending numeric value
WS_ENUM_VALUE valueArray[3] =
{
    { Red, &amp;redString },
    { Green, &amp;greenString },
    { Blue, &amp;blueString },
};

// sorted by ascending name
ULONG nameIndices[3] =
{
    2, // "blue"
    1, // "green"
    0, // "red"
};

WS_ENUM_DESCRIPTION enumDescription;
enumDescription.maxByteCount = 5; // "green"
enumDescription.values = valueArray;
enumDescription.valueCount = 3;
enumDescription.nameIndices = nameIndices;
</code></pre>


