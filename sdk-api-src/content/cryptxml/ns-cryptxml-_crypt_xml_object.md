---
UID: NS:cryptxml._CRYPT_XML_OBJECT
title: "_CRYPT_XML_OBJECT"
author: windows-sdk-content
description: Describes an Object element in the signature.
old-location: security\crypt_xml_object.htm
tech.root: seccrypto
ms.assetid: b151efb2-8801-451a-83ec-e9045c2e0b81
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: "*PCRYPT_XML_OBJECT, CRYPT_XML_OBJECT, CRYPT_XML_OBJECT structure [Security], PCRYPT_XML_OBJECT, PCRYPT_XML_OBJECT structure pointer [Security], _CRYPT_XML_OBJECT, cryptxml/CRYPT_XML_OBJECT, cryptxml/PCRYPT_XML_OBJECT, security.crypt_xml_object"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - CRYPT_XML_OBJECT
product: Windows
targetos: Windows
req.typenames: CRYPT_XML_OBJECT, *PCRYPT_XML_OBJECT
req.redist: 
---

# _CRYPT_XML_OBJECT structure


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

Optional. A <a href="https://msdn.microsoft.com/25414b2d-3283-4e2f-a23c-ccebff1409e2">CRYPT_XML_REFERENCES</a> structure that specifies an array of references.


### -field Encoded

Optional. A <a href="https://msdn.microsoft.com/b70aae53-919b-4d4a-b284-ea6bc223842f">CRYPT_XML_BLOB</a> structure that contains the XML part of the entire <b>Object</b> element.

<div class="alert"><b>Note</b>  This field is empty when the <b>Object</b> element does not contain
    any elements.
    Applications can use the <b>CRYPT_XML_FLAG_ALWAYS_RETURN_ENCODED_OBJECT</b> flag
    to always receive an encoded <b>Object</b> element.</div>
<div> </div>
