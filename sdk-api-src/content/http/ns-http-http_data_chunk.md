---
UID: NS:http._HTTP_DATA_CHUNK
title: HTTP_DATA_CHUNK (http.h)
description: Represents an individual block of data either in memory, in a file, or in the HTTP Server API response-fragment cache.
helpviewer_keywords: ["*PHTTP_DATA_CHUNK","HTTP_DATA_CHUNK","HTTP_DATA_CHUNK structure [HTTP]","PHTTP_DATA_CHUNK","PHTTP_DATA_CHUNK structure pointer [HTTP]","_http_http_data_chunk","http.http_data_chunk","http/HTTP_DATA_CHUNK","http/PHTTP_DATA_CHUNK"]
old-location: http\http_data_chunk.htm
tech.root: http
ms.assetid: ae67c066-c8bd-483f-829f-30192f49593d
ms.date: 12/05/2018
ms.keywords: '*PHTTP_DATA_CHUNK, HTTP_DATA_CHUNK, HTTP_DATA_CHUNK structure [HTTP], PHTTP_DATA_CHUNK, PHTTP_DATA_CHUNK structure pointer [HTTP], _http_http_data_chunk, http.http_data_chunk, http/HTTP_DATA_CHUNK, http/PHTTP_DATA_CHUNK'
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
targetos: Windows
req.typenames: HTTP_DATA_CHUNK, *PHTTP_DATA_CHUNK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_DATA_CHUNK
 - http/_HTTP_DATA_CHUNK
 - PHTTP_DATA_CHUNK
 - http/PHTTP_DATA_CHUNK
 - HTTP_DATA_CHUNK
 - http/HTTP_DATA_CHUNK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_DATA_CHUNK
---

# HTTP_DATA_CHUNK structure


## -description

The <b>HTTP_DATA_CHUNK</b> structure represents an individual block of data either in memory, in a file, or in the HTTP Server API response-fragment cache.

## -struct-fields

### -field DataChunkType

Type of data store. This member can be one of the values from the <b>HTTP_DATA_CHUNK_TYPE</b> enumeration.

### -field FromMemory

### -field FromMemory.pBuffer

Pointer to the starting memory address of the data block.

### -field FromMemory.BufferLength

Length, in bytes, of the data block.

### -field FromFileHandle

### -field FromFileHandle.ByteRange

An 
<a href="/windows/desktop/api/http/ns-http-http_byte_range">HTTP_BYTE_RANGE</a> structure that specifies all or part of the file. To specify the entire file, set the <b>StartingOffset</b> member to zero and the <b>Length</b> member to <b>HTTP_BYTE_RANGE_TO_EOF</b>.

### -field FromFileHandle.FileHandle

Open handle to the file in question.

### -field FromFragmentCache

### -field FromFragmentCache.FragmentNameLength

Length, in bytes, of the fragment name not including the terminating null character.

### -field FromFragmentCache.pFragmentName

Pointer to a string that contains the fragment name assigned when the fragment was added to the response-fragment cache using 
the <a href="/windows/desktop/api/http/nf-http-httpaddfragmenttocache">HttpAddFragmentToCache</a> function.

### -field FromFragmentCacheEx

### -field FromFragmentCacheEx.ByteRange

An <a href="/windows/desktop/api/http/ns-http-http_byte_range">HTTP_BYTE_RANGE</a> structure specifying the byte range in the cached fragment.

### -field FromFragmentCacheEx.pFragmentName

Pointer to a string that contains the fragment name assigned when the fragment was added to the response-fragment cache using 
the <a href="/windows/desktop/api/http/nf-http-httpaddfragmenttocache">HttpAddFragmentToCache</a> function. The length of the string cannot exceed 65532 bytes.

<div class="alert"><b>Note</b>  This string must be NULL terminated.</div>
<div> </div>

### -field Trailers

### -field Trailers.TrailerCount

Count of the number of <a href="/windows/desktop/api/http/ns-http-http_unknown_header">HTTP_UNKNOWN_HEADER</a> structures in the array pointed to by <b>pTrailers</b>.

### -field Trailers.pTrailers

Pointer to an array of <a href="/windows/desktop/api/http/ns-http-http_unknown_header">HTTP_UNKNOWN_HEADER</a> structures containing the trailers.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-1-0-structures">HTTP Server API Version 1.0 Structures</a>



<a href="/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)">HTTP_REQUEST</a>



<a href="/windows/desktop/Http/http-response">HTTP_RESPONSE</a>



<a href="/windows/desktop/api/http/nf-http-httpaddfragmenttocache">HttpAddFragmentToCache</a>



<a href="/windows/desktop/api/http/nf-http-httpsendresponseentitybody">HttpSendResponseEntityBody</a>