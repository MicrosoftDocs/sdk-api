---
UID: NS:webservices._WS_XML_DICTIONARY
title: WS_XML_DICTIONARY (webservices.h)
description: Represents a set of unique strings. This information is used by the binary encoding to write a more compact xml document.
helpviewer_keywords: ["WS_XML_DICTIONARY","WS_XML_DICTIONARY structure [Web Services for Windows]","webservices/WS_XML_DICTIONARY","wsw.ws_xml_dictionary"]
old-location: wsw\ws_xml_dictionary.htm
tech.root: wsw
ms.assetid: 2cba47fd-a049-4e50-99dd-20ccf91c9e0f
ms.date: 12/05/2018
ms.keywords: WS_XML_DICTIONARY, WS_XML_DICTIONARY structure [Web Services for Windows], webservices/WS_XML_DICTIONARY, wsw.ws_xml_dictionary
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
targetos: Windows
req.typenames: WS_XML_DICTIONARY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_XML_DICTIONARY
 - webservices/_WS_XML_DICTIONARY
 - WS_XML_DICTIONARY
 - webservices/WS_XML_DICTIONARY
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
 - WS_XML_DICTIONARY
---

# WS_XML_DICTIONARY structure


## -description

Represents a set of unique strings.  This information is used by the binary
        encoding to write a more compact xml document.

## -struct-fields

### -field guid

A guid that uniquely identifies the set of strings represented by the dictionary.
          The guid is never transmitted or persisted, and needs to only be unique for the lifetime of the process.

### -field strings

The set of unique strings that comprise the dictionary.

### -field stringCount

Specifies the number of strings in the dictionary.

### -field isConst

Indicates if the dictionary and its contents are declared const and that they will be kept valid for the
          entire lifetime of any object with which strings in the dictionary are used.
        

If this is <b>TRUE</b>, then the strings can be manipulated more efficiently.

## -remarks

All strings and values within a dictionary must be unique.  Dictionaries are
        always assumed to be well-formed, so it is up to the creator of the dictionary
        to ensure that this is the case.
      

A dictionary might be declared as:

``` syntax
struct PurchaseOrderDictionary
{
    WS_XML_DICTIONARY dictionary;
    WS_XML_STRING quantity;
    WS_XML_STRING productName;
    WS_XML_STRING purchaseOrder;
    WS_XML_STRING purchaseOrderNamespace;
};

static PurchaseOrderDictionary purchaseOrderDictionary =
{
    { 
        { /* A unique GUID generated from uuidgen */ },
        &purchaseOrderDictionary.quantity,
        4, 
        TRUE 
    },
    WS_XML_STRING_DICTIONARY_VALUE("Quantity",           &purchaseOrderDictionary.dictionary, 0),
    WS_XML_STRING_DICTIONARY_VALUE("ProductName",        &purchaseOrderDictionary.dictionary, 1),
    WS_XML_STRING_DICTIONARY_VALUE("PurchaseOrder",      &purchaseOrderDictionary.dictionary, 2),
    WS_XML_STRING_DICTIONARY_VALUE("http://example.com", &purchaseOrderDictionary.dictionary, 3),
};

```

Strings from the dictionary might be used as:


``` syntax
WsWriteStartElement(xmlWriter, NULL, &purchaseOrderDictionary.purchaseOrder, &purchaseOrderDictionary.purchaseOrderNamespace, error);
```


