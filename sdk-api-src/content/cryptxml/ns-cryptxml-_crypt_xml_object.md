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
