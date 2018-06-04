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

# _CRYPT_XML_KEY_ECDSA_KEY_VALUE structure


## -description


The <b>CRYPT_XML_KEY_ECDSA_KEY_VALUE</b> structure defines an Elliptic Curve Digital Signature Algorithm (ECDSA) key value.  The <b>CRYPT_XML_KEY_ECDSA_KEY_VALUE</b> structure is used as an element of the key value union  in the <a href="https://msdn.microsoft.com/7aadd268-41bc-4ba3-babb-2ca7b13f378b">CRYPT_XML_KEY_VALUE</a> structure.


## -struct-fields




### -field wszNamedCurve

A pointer to a null-terminated Unicode string that contains the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) of the named curve.


### -field X

Defines the X value of an ECDSA curve.


### -field Y

Defines the Y value of an ECDSA curve.


### -field ExplicitPara

A   <b>CRYPT_XML_BLOB</b> value that defines the encoded parameters of an ECDSA curve.

