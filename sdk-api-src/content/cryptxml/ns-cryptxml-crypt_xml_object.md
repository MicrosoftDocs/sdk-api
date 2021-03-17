---
UID: NS:cryptxml._CRYPT_XML_OBJECT
title: CRYPT_XML_OBJECT (cryptxml.h)
description: Describes an Object element in the signature.
helpviewer_keywords: ["*PCRYPT_XML_OBJECT","CRYPT_XML_OBJECT","CRYPT_XML_OBJECT structure [Security]","PCRYPT_XML_OBJECT","PCRYPT_XML_OBJECT structure pointer [Security]","cryptxml/CRYPT_XML_OBJECT","cryptxml/PCRYPT_XML_OBJECT","security.crypt_xml_object"]
old-location: security\crypt_xml_object.htm
tech.root: security
ms.assetid: b151efb2-8801-451a-83ec-e9045c2e0b81
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_XML_OBJECT, CRYPT_XML_OBJECT, CRYPT_XML_OBJECT structure [Security], PCRYPT_XML_OBJECT, PCRYPT_XML_OBJECT structure pointer [Security], cryptxml/CRYPT_XML_OBJECT, cryptxml/PCRYPT_XML_OBJECT, security.crypt_xml_object'
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
targetos: Windows
req.typenames: CRYPT_XML_OBJECT, *PCRYPT_XML_OBJECT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_XML_OBJECT
 - cryptxml/_CRYPT_XML_OBJECT
 - PCRYPT_XML_OBJECT
 - cryptxml/PCRYPT_XML_OBJECT
 - CRYPT_XML_OBJECT
 - cryptxml/CRYPT_XML_OBJECT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Cryptxml.h
api_name:
 - CRYPT_XML_OBJECT
---

# CRYPT_XML_OBJECT structure


## -description

The <b>CRYPT_XML_OBJECT</b> structure describes an <b>Object</b> element in the signature.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field hObject

The handle of the object.

### -field wszId

Optional. A pointer to a null-terminated wide character string that contains the value of the unique identifier attribute of the <b>Object</b> element.

### -field wszMimeType

Optional. A pointer to a null-terminated wide character string that contains the value of the MIME-type attribute of the <b>Object</b> element.

### -field wszEncoding

Optional. A pointer to a null-terminated wide character string that contains the value of the encoding method attribute of the <b>Object</b> element.

### -field Manifest

Optional. A <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_references">CRYPT_XML_REFERENCES</a> structure that specifies an array of references.

### -field Encoded

Optional. A <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_blob">CRYPT_XML_BLOB</a> structure that contains the XML part of the entire <b>Object</b> element.

<div class="alert"><b>Note</b>  This field is empty when the <b>Object</b> element does not contain
    any elements.
    Applications can use the <b>CRYPT_XML_FLAG_ALWAYS_RETURN_ENCODED_OBJECT</b> flag
    to always receive an encoded <b>Object</b> element.</div>
<div> </div>