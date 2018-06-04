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

# _SEC_WINNT_AUTH_SHORT_VECTOR structure


## -description


Specifies the offset and number of characters in an array of <b>USHORT</b> values.


## -struct-fields




### -field ShortArrayOffset

The number of characters before the beginning of the data in a <a href="https://msdn.microsoft.com/33e42e35-e34c-4e89-90c7-8aee5176ae1b">SEC_WINNT_AUTH_PACKED_CREDENTIALS_EX</a> structure.


### -field ShortArrayCount

The  number of characters in the array.

