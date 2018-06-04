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

# _CRYPT_XML_KEY_RSA_KEY_VALUE structure


## -description


The <b>CRYPT_XML_KEY_RSA_KEY_VALUE</b> structure defines an RSA key value.  The <b>CRYPT_XML_KEY_RSA_KEY_VALUE</b> structure is used as element of the key value union  in the <a href="https://msdn.microsoft.com/7aadd268-41bc-4ba3-babb-2ca7b13f378b">CRYPT_XML_KEY_VALUE</a> structure.


## -struct-fields




### -field Modulus

A <a href="https://msdn.microsoft.com/dc7e23d6-923c-40d2-9cf7-9a529c0634ce">CRYPT_XML_DATA_BLOB</a> structure that contains the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> modulus data.


### -field Exponent

A <a href="https://msdn.microsoft.com/dc7e23d6-923c-40d2-9cf7-9a529c0634ce">CRYPT_XML_DATA_BLOB</a> structure that contains the public key exponent data.

