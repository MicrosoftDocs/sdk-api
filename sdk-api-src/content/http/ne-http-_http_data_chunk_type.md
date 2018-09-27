---
UID: NE:http._HTTP_DATA_CHUNK_TYPE
title: "_HTTP_DATA_CHUNK_TYPE"
author: windows-sdk-content
description: Defines the data source for a data chunk.
old-location: http\http_data_chunk_type.htm
tech.root: Http
ms.assetid: fbb04b0a-df1a-409d-aadc-c06b816924c5
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PHTTP_DATA_CHUNK_TYPE, HTTP_DATA_CHUNK_TYPE, HTTP_DATA_CHUNK_TYPE enumeration [HTTP], HttpDataChunkFromFileHandle, HttpDataChunkFromFragmentCache, HttpDataChunkFromFragmentCacheEx, HttpDataChunkFromMemory, _HTTP_DATA_CHUNK_TYPE, http.http_data_chunk_type, http/HTTP_DATA_CHUNK_TYPE, http/HttpDataChunkFromFileHandle, http/HttpDataChunkFromFragmentCache, http/HttpDataChunkFromFragmentCacheEx, http/HttpDataChunkFromMemory"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: http.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_DATA_CHUNK_TYPE
product: Windows
targetos: Windows
req.typenames: HTTP_DATA_CHUNK_TYPE, *PHTTP_DATA_CHUNK_TYPE
req.redist: 
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



