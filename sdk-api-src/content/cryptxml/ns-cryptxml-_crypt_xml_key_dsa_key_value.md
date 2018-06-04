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

# _CRYPT_XML_KEY_DSA_KEY_VALUE structure


## -description


The <b>CRYPT_XML_KEY_DSA_KEY_VALUE</b> structure defines a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Digital Signature Algorithm</a> (DSA) key value.  The <b>CRYPT_XML_KEY_DSA_KEY_VALUE</b> structure is used as an element of the key value union  in the <a href="https://msdn.microsoft.com/7aadd268-41bc-4ba3-babb-2ca7b13f378b">CRYPT_XML_KEY_VALUE</a> structure.


## -struct-fields




### -field P

Defines the  P part of the DSA key.


### -field Q

Defines the  Q part of the DSA key.


### -field G

Defines the  G part of the DSA key.


### -field Y

Defines the Y  part of the DSA key.


### -field J

Defines the J part of the DSA key.


### -field Seed

The seed value, in big-endian format.


### -field Counter

The count value, in big-endian format.

