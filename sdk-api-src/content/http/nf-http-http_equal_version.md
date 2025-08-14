---
UID: NF:http.HTTP_EQUAL_VERSION
title: HTTP_EQUAL_VERSION macro (http.h)
description: Returns a non-zero value if an HTTP_VERSION structure is equal to a specified major/minor version combination, or zero otherwise.
helpviewer_keywords: ["HTTP_EQUAL_VERSION","HTTP_EQUAL_VERSION macro [HTTP]","_http_http_equal_version","http.http_equal_version","http/HTTP_EQUAL_VERSION"]
old-location: http\http_equal_version.htm
tech.root: http
ms.assetid: bcbe0e43-5164-4571-b672-2af547468f8f
ms.date: 07/01/2025
ms.keywords: HTTP_EQUAL_VERSION, HTTP_EQUAL_VERSION macro [HTTP], _http_http_equal_version, http.http_equal_version, http/HTTP_EQUAL_VERSION
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HTTP_EQUAL_VERSION
 - http/HTTP_EQUAL_VERSION
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
 - HTTP_EQUAL_VERSION
---

# HTTP_EQUAL_VERSION macro

## -syntax

```cpp
int HTTP_EQUAL_VERSION(
    HTTP_VERSION version,
    USHORT major,
    USHORT minor
);
```

## -returns

Type: **int**

Returns an integer that is either zero (false) or non-zero (true), that indicates if the version combination, passed in the _major_ and _minor_ parameters is, exactly equal to the value of the _version_ parameter.


## -description

The 
<b>HTTP_EQUAL_VERSION</b> macro returns a non-zero value if an <a href="/windows/desktop/api/http/ns-http-http_version">HTTP_VERSION</a> structure is equal to a specified major/minor version combination, or zero otherwise.

## -parameters

### -param version

The <a href="/windows/desktop/api/http/ns-http-http_version">HTTP_VERSION</a> structure to be examined.

### -param major

A major portion of the version to be compared.

### -param minor

A minor portion of the version to be compared.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-1-0-macros">HTTP Server API Version 1.0 Macros</a>
