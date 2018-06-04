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

# _CRYPT_XML_SIGNATURE structure


## -description


The <b>CRYPT_XML_SIGNATURE</b> structure contains information used to populate the <b>Signature</b> element.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field hSignature

The handle of the signature to encode.


### -field wszId

A pointer to a null-terminated Unicode string that contains the value of the <b>Id</b> attribute.


### -field SignedInfo

A <a href="https://msdn.microsoft.com/34f7f3be-8bf8-4863-9c94-79ee14a7ebea">CRYPT_XML_SIGNED_INFO</a> structure that contains the canonicalization algorithm, 
    a signature algorithm, and one or more references. 
    The <b>SignedInfo</b> element can contain an optional ID attribute that will allow 
    the structure to be referenced by other signatures and objects. 


### -field SignatureValue

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that contains a cryptographic signature value  used to populate the <b>Signature</b> element.


### -field pKeyInfo

Optional. A pointer to a <a href="https://msdn.microsoft.com/0fd4a80f-52c1-4ff8-9e49-87ddc1f2521d">CRYPT_XML_KEY_INFO</a> structure that contains information that is encoded in the <b>KeyInfo</b> element.


### -field cObject

The number of  items in the array pointed to by the <b>rgpObject</b> member.


### -field rgpObject

Optional. A pointer to an array of  pointers to <a href="https://msdn.microsoft.com/b151efb2-8801-451a-83ec-e9045c2e0b81">CRYPT_XML_OBJECT</a> structures that  contain information that is encoded in <b>Object</b> elements.

