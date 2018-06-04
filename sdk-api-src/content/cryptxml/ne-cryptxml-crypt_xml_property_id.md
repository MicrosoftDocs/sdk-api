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

# CRYPT_XML_PROPERTY_ID enumeration


## -description


The <b>CRYPT_XML_PROPERTY_ID</b> enumeration 
  specifies the type and usage of the XML property.


## -enum-fields




### -field CRYPT_XML_PROPERTY_MAX_HEAP_SIZE

Specifies the maximum heap size, in bytes, that the  XML layer can use.
      This property is applied to intermediate buffers used to parse or construct XML parts. 
      By default, the limit is equal to <b>CRYPT_XML_BLOB_MAX</b>.


### -field CRYPT_XML_PROPERTY_SIGNATURE_LOCATION

Specifies the location in the XML document where the signature is to be created.



The following formats are supported:



<dl>
<dt><a id="_id"></a><a id="_ID"></a>#id</dt>
<dd>
The Id attribute of the element to insert the signature.

</dd>
<dt><a id="_a_b_c"></a><a id="_A_B_C"></a>/a/b/c</dt>
<dd>
The absolute path of the element to insert the signature.

</dd>
</dl>



### -field CRYPT_XML_PROPERTY_MAX_SIGNATURES

Specifies the maximum number of <b>Signature</b> elements when parsing an XML document. 
     This property overrides the default <b>CRYPT_XML_SIGNATURES_MAX</b> value.


### -field CRYPT_XML_PROPERTY_DOC_DECLARATION

Specifies whether to write an XML document declaration. This property is used with the 
     <a href="https://msdn.microsoft.com/fb0cd00c-f410-486e-8910-41c0463f6a74">CryptXmlEncode</a> function. The default property is <b>TRUE</b>.


### -field CRYPT_XML_PROPERTY_XML_OUTPUT_CHARSET

Specifies an encoding character set of XML fragments for custom elements. This property is used with the 
     <a href="https://msdn.microsoft.com/b6a77d62-b92d-4b83-949f-14a0ce3ce025">CryptXmlOpenToDecode</a> function. 
     The default character set is inherited from the opened document.


## -remarks



If a property value is defined as a pointer to data, then the pointer must be valid 
  for the entire period of the signature operation.




