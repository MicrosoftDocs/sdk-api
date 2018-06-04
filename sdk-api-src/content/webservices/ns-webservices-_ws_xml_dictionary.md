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

# _WS_XML_DICTIONARY structure


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
      

<pre class="syntax" xml:space="preserve"><code>struct PurchaseOrderDictionary
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
        &amp;purchaseOrderDictionary.quantity,
        4, 
        TRUE 
    },
    WS_XML_STRING_DICTIONARY_VALUE("Quantity",           &amp;purchaseOrderDictionary.dictionary, 0),
    WS_XML_STRING_DICTIONARY_VALUE("ProductName",        &amp;purchaseOrderDictionary.dictionary, 1),
    WS_XML_STRING_DICTIONARY_VALUE("PurchaseOrder",      &amp;purchaseOrderDictionary.dictionary, 2),
    WS_XML_STRING_DICTIONARY_VALUE("http://example.com", &amp;purchaseOrderDictionary.dictionary, 3),
};
</code></pre>

        Strings from the dictionary might be used as:
      

<pre class="syntax" xml:space="preserve"><code>WsWriteStartElement(xmlWriter, NULL, &amp;purchaseOrderDictionary.purchaseOrder, &amp;purchaseOrderDictionary.purchaseOrderNamespace, error);</code></pre>


