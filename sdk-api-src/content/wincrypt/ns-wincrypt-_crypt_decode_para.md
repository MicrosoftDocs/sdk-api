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

# _CRYPT_DECODE_PARA structure


## -description


The <b>CRYPT_DECODE_PARA</b> structure is used by the <a href="https://msdn.microsoft.com/bf1935f0-1ab0-4068-9ed5-8fbb2c286b8a">CryptDecodeObjectEx</a> function to provide access to memory allocation and memory freeing callback functions.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field pfnAlloc

This member is an optional pointer to a callback function used to allocate memory.


### -field pfnFree

This member is an optional pointer to a callback function used to free memory allocated by the allocate callback function.

