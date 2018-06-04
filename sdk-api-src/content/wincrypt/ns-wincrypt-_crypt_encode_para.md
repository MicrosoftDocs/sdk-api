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

# _CRYPT_ENCODE_PARA structure


## -description


The <b>CRYPT_ENCODE_PARA</b> structure is used by the <a href="https://msdn.microsoft.com/45134db8-059b-43d3-90c2-9b6cc970fca0">CryptEncodeObjectEx</a> function to provide access to memory allocation and memory freeing callback functions.


## -struct-fields




### -field cbSize

Indicates the size, in bytes, of the structure.


### -field pfnAlloc

This member is an optional pointer to a callback function used to allocate memory.


### -field pfnFree

This member is an optional pointer to a callback function used to free memory allocated by the allocate callback function.

