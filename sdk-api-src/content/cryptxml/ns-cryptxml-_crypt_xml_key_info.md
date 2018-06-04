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

# _CRYPT_XML_KEY_INFO structure


## -description


The <b>CRYPT_XML_KEY_INFO</b> structure encapsulates key information data.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field wszId

A pointer to a null-terminated wide character string that specifies the value of the <b>ID</b> attribute of the key information element.


### -field cKeyInfo

The number of items in the array pointed to by the <b>rgKeyInfo</b> member.


### -field rgKeyInfo

A pointer to an array of <a href="https://msdn.microsoft.com/3fbb1623-d493-49f1-a004-74ec8d22520e">CRYPT_XML_KEY_INFO_ITEM</a> structures that contain key information.


### -field hVerifyKey

Optional. The handle of data  derived from the first key value.

