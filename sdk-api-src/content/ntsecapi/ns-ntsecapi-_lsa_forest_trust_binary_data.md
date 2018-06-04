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

# _LSA_FOREST_TRUST_BINARY_DATA structure


## -description


The <b>LSA_FOREST_TRUST_BINARY_DATA</b> structure contains binary data used in <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> forest trust operations.


## -struct-fields




### -field Length.range

 


### -field Length.range.0

 


### -field Length.range.MAX_FOREST_TRUST_BINARY_DATA_SIZE

 


### -field Buffer.size_is

 


### -field Buffer.size_is.Length

 


### -field Length

Size of the structure in bytes.


### -field Buffer

Pointer to an array of type <b>UCHAR</b> that contains the binary data. The buffer can contain at most 128 KB of data.

