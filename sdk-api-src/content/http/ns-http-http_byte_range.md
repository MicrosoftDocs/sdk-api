---
UID: NS:http._HTTP_BYTE_RANGE
title: HTTP_BYTE_RANGE (http.h)
description: The HTTP_BYTE_RANGE structure is used to specify a byte range within a cached response fragment, file, or other data block.
helpviewer_keywords: ["*PHTTP_BYTE_RANGE","HTTP_BYTE_RANGE","HTTP_BYTE_RANGE structure [HTTP]","PHTTP_BYTE_RANGE","PHTTP_BYTE_RANGE structure pointer [HTTP]","_http_http_byte_range","http.http_byte_range","http/HTTP_BYTE_RANGE","http/PHTTP_BYTE_RANGE"]
old-location: http\http_byte_range.htm
tech.root: http
ms.assetid: a57d23cd-1e91-401a-b242-6549b1457594
ms.date: 12/05/2018
ms.keywords: '*PHTTP_BYTE_RANGE, HTTP_BYTE_RANGE, HTTP_BYTE_RANGE structure [HTTP], PHTTP_BYTE_RANGE, PHTTP_BYTE_RANGE structure pointer [HTTP], _http_http_byte_range, http.http_byte_range, http/HTTP_BYTE_RANGE, http/PHTTP_BYTE_RANGE'
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
req.typenames: HTTP_BYTE_RANGE, *PHTTP_BYTE_RANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_BYTE_RANGE
 - http/_HTTP_BYTE_RANGE
 - PHTTP_BYTE_RANGE
 - http/PHTTP_BYTE_RANGE
 - HTTP_BYTE_RANGE
 - http/HTTP_BYTE_RANGE
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
 - HTTP_BYTE_RANGE
---

# HTTP_BYTE_RANGE structure


## -description

The 
<b>HTTP_BYTE_RANGE</b> structure is used to specify a byte range within a cached response fragment, file, or other data block.

## -struct-fields

### -field StartingOffset

Starting offset of the byte range.

### -field Length

Size, in bytes, of the range. If this member is HTTP_BYTE_RANGE_TO_EOF, the range extends from the starting offset to the end of the file or data block.

## -see-also

<a href="/windows/desktop/api/http/ns-http-http_data_chunk">HTTP_DATA_CHUNK</a>



<a href="/windows/desktop/api/http/nf-http-httpreadfragmentfromcache">HttpReadFragmentFromCache</a>