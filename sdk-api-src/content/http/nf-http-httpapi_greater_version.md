---
UID: NF:http.HTTPAPI_GREATER_VERSION
title: HTTPAPI_GREATER_VERSION macro (http.h)
description: Returns a non-zero value if an HTTPAPI_VERSION structure is greater than a specified major/minor version combination, or zero otherwise.
helpviewer_keywords: ["HTTPAPI_GREATER_VERSION","HTTPAPI_GREATER_VERSION macro [HTTP]","http.httpapi_greater_version","http/HTTPAPI_GREATER_VERSION"]
old-location: http\httpapi_greater_version.htm
tech.root: http
ms.assetid: e70500dd-e750-437c-8652-280f9cc9de1d
ms.date: 07/01/2025
ms.keywords: HTTPAPI_GREATER_VERSION, HTTPAPI_GREATER_VERSION macro [HTTP], http.httpapi_greater_version, http/HTTPAPI_GREATER_VERSION
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HTTPAPI_GREATER_VERSION
 - http/HTTPAPI_GREATER_VERSION
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
 - HTTP_GREATER_VERSION
---

# HTTPAPI_GREATER_VERSION macro

## -syntax

```cpp
int HTTP_GREATER_VERSION(
    HTTPAPI_VERSION version,
    USHORT major,
    USHORT minor
);
```

## -returns

Type: **int**

Returns an integer that is either zero (false) or non-zero (true), that indicates whether or not the value of the _version_ parameter is greater than the version combination passed in the _major_ and _minor_ parameters.


## -description

The <b>HTTPAPI_GREATER_VERSION</b> returns a non-zero value if an <a href="/windows/desktop/api/http/ns-http-httpapi_version">HTTPAPI_VERSION</a> structure is greater than a specified major/minor version combination, or zero otherwise.

## -parameters

### -param version

The <a href="/windows/desktop/api/http/ns-http-httpapi_version">HTTPAPI_VERSION</a> structure to be examined.

### -param major

The major portion of the version to be compared.

### -param minor

The minor portion of the version to be compared.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-1-0-macros">HTTP Server API Version 1.0 Macros</a>
