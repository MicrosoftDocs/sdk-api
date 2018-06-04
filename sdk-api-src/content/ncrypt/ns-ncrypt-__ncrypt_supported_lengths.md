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

# __NCRYPT_SUPPORTED_LENGTHS structure


## -description


The <b>NCRYPT_SUPPORTED_LENGTHS</b> structure is used with the <a href="https://msdn.microsoft.com/407f0e42-07c8-4ec6-81c6-f8bde005adb0">NCRYPT_LENGTHS_PROPERTY</a> property to contain length information for a key.


## -struct-fields




### -field dwMinLength

The minimum length, in bits, of a key.


### -field dwMaxLength

The maximum length, in bits, of a key.


### -field dwIncrement

The number of bits that the key size can be incremented between <b>dwMinLength</b> and <b>dwMaxLength</b>.


### -field dwDefaultLength

The default length, in bits, of a key.

