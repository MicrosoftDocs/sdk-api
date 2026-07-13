---
UID: NS:webservices._WS_ENUM_DESCRIPTION
title: WS_ENUM_DESCRIPTION (webservices.h)
description: A type description that is used with WS_ENUM_TYPE and is required. It provides information used in serializing and deserializing values of an enumeration.
helpviewer_keywords: ["WS_ENUM_DESCRIPTION","WS_ENUM_DESCRIPTION structure [Web Services for Windows]","webservices/WS_ENUM_DESCRIPTION","wsw.ws_enum_description"]
old-location: wsw\ws_enum_description.htm
tech.root: wsw
ms.assetid: cf7c9254-c806-4ada-8852-beb6be5e81d9
ms.date: 12/05/2018
ms.keywords: WS_ENUM_DESCRIPTION, WS_ENUM_DESCRIPTION structure [Web Services for Windows], webservices/WS_ENUM_DESCRIPTION, wsw.ws_enum_description
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
req.typenames: WS_ENUM_DESCRIPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_ENUM_DESCRIPTION
 - webservices/_WS_ENUM_DESCRIPTION
 - WS_ENUM_DESCRIPTION
 - webservices/WS_ENUM_DESCRIPTION
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
 - WS_ENUM_DESCRIPTION
---

# WS_ENUM_DESCRIPTION structure


## -description

A type description that is used with <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_ENUM_TYPE</a> and is required. 
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
            


``` syntax
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
    { Red, &redString },
    { Green, &greenString },
    { Blue, &blueString },
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

```

