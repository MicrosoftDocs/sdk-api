---
UID: NF:http.HTTP_SET_NULL_ID
title: HTTP_SET_NULL_ID macro (http.h)
description: The HTTP_SET_NULL_ID macro sets the HTTP_OPAQUE_ID to NULL.
helpviewer_keywords: ["HTTP_SET_NULL_ID","HTTP_SET_NULL_ID macro [HTTP]","http.http_set_null_id","http/HTTP_SET_NULL_ID"]
old-location: http\http_set_null_id.htm
tech.root: http
ms.assetid: d4a15361-3346-4c05-a3df-4503da183549
ms.date: 07/01/2025
ms.keywords: HTTP_SET_NULL_ID, HTTP_SET_NULL_ID macro [HTTP], http.http_set_null_id, http/HTTP_SET_NULL_ID
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
 - HTTP_SET_NULL_ID
 - http/HTTP_SET_NULL_ID
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
 - HTTP_SET_NULL_ID
---

# HTTP_SET_NULL_ID macro

## -syntax

```cpp
void HTTP_SET_NULL_ID(
    pid pid
);
```


## -description

The <b>HTTP_SET_NULL_ID</b> macro sets the <a href="/windows/desktop/Http/http-server-api-version-2-0-data-types">HTTP_OPAQUE_ID</a> to <b>NULL</b>.

## -parameters

### -param pid

The identifier that is set to <b>NULL</b>.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-macros">HTTP Server API Version 2.0 Macros</a>



<a href="/windows/desktop/api/http/nf-http-http_is_null_id">HTTP_IS_NULL_ID</a>



<a href="/previous-versions/windows/desktop/legacy/aa364541(v=vs.85)">HTTP_NULL_ID</a>
