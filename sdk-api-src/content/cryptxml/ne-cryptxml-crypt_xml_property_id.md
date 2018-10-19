---
UID: NE:cryptxml.CRYPT_XML_PROPERTY_ID
title: CRYPT_XML_PROPERTY_ID
author: windows-sdk-content
description: Specifies the type and usage of the XML property.
old-location: security\crypt_xml_property_id.htm
tech.root: seccrypto
ms.assetid: 7b396245-6dc5-4018-821e-a70db5f0d068
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: CRYPT_XML_PROPERTY_DOC_DECLARATION, CRYPT_XML_PROPERTY_ID, CRYPT_XML_PROPERTY_ID enumeration [Security], CRYPT_XML_PROPERTY_MAX_HEAP_SIZE, CRYPT_XML_PROPERTY_MAX_SIGNATURES, CRYPT_XML_PROPERTY_SIGNATURE_LOCATION, CRYPT_XML_PROPERTY_XML_OUTPUT_CHARSET, cryptxml/CRYPT_XML_PROPERTY_DOC_DECLARATION, cryptxml/CRYPT_XML_PROPERTY_ID, cryptxml/CRYPT_XML_PROPERTY_MAX_HEAP_SIZE, cryptxml/CRYPT_XML_PROPERTY_MAX_SIGNATURES, cryptxml/CRYPT_XML_PROPERTY_SIGNATURE_LOCATION, cryptxml/CRYPT_XML_PROPERTY_XML_OUTPUT_CHARSET, security.crypt_xml_property_id
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: cryptxml.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Cryptxml.h
api_name:
 - CRYPT_XML_PROPERTY_ID
product: Windows
targetos: Windows
req.typenames: CRYPT_XML_PROPERTY_ID
req.redist: 
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




