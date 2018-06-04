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

# _HTTP_DATA_CHUNK_TYPE enumeration


## -description


The 
<a href="https://msdn.microsoft.com/07d9853f-d38c-4e5b-815a-3dc0157b4d8d">HTTP_DATA_CHUNK_TYPE</a> enumeration type defines the data source for a data chunk.


## -enum-fields




### -field HttpDataChunkFromMemory

The data source is a memory data block. The union should be interpreted as a <b>FromMemory</b> structure.


### -field HttpDataChunkFromFileHandle

The data source is a file handle data block. The union should be interpreted as a <b>FromFileHandle</b> structure.


### -field HttpDataChunkFromFragmentCache

The data source is a fragment cache data block. The union should be interpreted as a <b>FromFragmentCache</b> structure.


### -field HttpDataChunkFromFragmentCacheEx

The data source is a fragment cache data block. The union should be interpreted as a <b>FromFragmentCacheEx</b> structure.

<b>Windows Server 2003 with SP1 and Windows XP with SP2:  </b>This flag is not supported.


### -field HttpDataChunkMaximum



