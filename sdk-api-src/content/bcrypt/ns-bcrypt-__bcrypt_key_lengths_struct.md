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

# __BCRYPT_KEY_LENGTHS_STRUCT structure


## -description


The <b>BCRYPT_KEY_LENGTHS_STRUCT</b> structure defines the range of key sizes that are supported by the provider. This structure is used with the <b>BCRYPT_KEY_LENGTHS</b> property.

This structure is also used with the <b>BCRYPT_AUTH_TAG_LENGTH</b> property to contain the minimum, maximum, and increment size of an authentication tag.


## -struct-fields




### -field dwMinLength

The minimum length, in bits, of a key.


### -field dwMaxLength

The maximum length, in bits, of a key.


### -field dwIncrement

The number of bits that the key size can be incremented between <b>dwMinLength</b> and <b>dwMaxLength</b>.


## -remarks



The key sizes are given in a range that is inclusive of the minimum and maximum values and are separated by the increment. For example, if the minimum key size is 8 bits, the maximum key size is 16 bits, and the increment is 2 bits, the provider would support key sizes of 8, 10, 12, 14, and 16 bits.



