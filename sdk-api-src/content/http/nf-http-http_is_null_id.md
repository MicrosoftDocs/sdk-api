---
UID: NF:http.HTTP_IS_NULL_ID
title: HTTP_IS_NULL_ID macro (http.h)
description: Determines if the HTTP_OPAQUE_ID is NULL.
helpviewer_keywords: ["HTTP_IS_NULL_ID","HTTP_IS_NULL_ID macro [HTTP]","http.http_is_null_id","http/HTTP_IS_NULL_ID"]
old-location: http\http_is_null_id.htm
tech.root: http
ms.assetid: 8a73585a-e531-4c5d-9ed3-9e6e1fef93ac
ms.date: 07/01/2025
ms.keywords: HTTP_IS_NULL_ID, HTTP_IS_NULL_ID macro [HTTP], http.http_is_null_id, http/HTTP_IS_NULL_ID
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HTTP_IS_NULL_ID
 - http/HTTP_IS_NULL_ID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - http.h
api_name:
 - HTTP_IS_NULL_ID
---

# HTTP_IS_NULL_ID macro

## -syntax

```cpp
void HTTP_IS_NULL_ID(
    pid pid
);
```


## -description

The <b>HTTP_IS_NULL_ID</b> macro determines if the <a href="/windows/desktop/Http/http-server-api-version-2-0-data-types">HTTP_OPAQUE_ID</a> is <b>NULL</b>.

## -parameters

### -param pid

The parameter determined to be <b>NULL</b>.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-macros">HTTP Server API Version 2.0 Macros</a>



<a href="/previous-versions/windows/desktop/legacy/aa364541(v=vs.85)">HTTP_NULL_ID</a>



<a href="/windows/desktop/api/http/nf-http-http_set_null_id">HTTP_SET_NULL_ID</a>
