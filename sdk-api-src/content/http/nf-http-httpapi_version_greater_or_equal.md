---
UID: NF:http.HTTPAPI_VERSION_GREATER_OR_EQUAL
title: HTTPAPI_VERSION_GREATER_OR_EQUAL macro (http.h)
description: The HTTPAPI_VERSION_GREATER_OR_EQUAL returns a non-zero value if an HTTPAPI_VERSION structure is greater than or equal to a specified major/minor version combination, or zero otherwise.
helpviewer_keywords: ["HTTPAPI_VERSION_GREATER_OR_EQUAL","HTTPAPI_VERSION_GREATER_OR_EQUAL macro [HTTP]","http.httpapi_version_greater_or_equal","http/HTTPAPI_VERSION_GREATER_OR_EQUAL"]
old-location: http\httpapi_version_greater_or_equal.htm
tech.root: http
ms.assetid: d9ac035f-7085-417f-b7df-0607b95f4233
ms.date: 07/01/2025
ms.keywords: HTTPAPI_VERSION_GREATER_OR_EQUAL, HTTPAPI_VERSION_GREATER_OR_EQUAL macro [HTTP], http.httpapi_version_greater_or_equal, http/HTTPAPI_VERSION_GREATER_OR_EQUAL
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
 - HTTPAPI_VERSION_GREATER_OR_EQUAL
 - http/HTTPAPI_VERSION_GREATER_OR_EQUAL
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
 - HTTP_GREATER_EQUAL_VERSION
---

# HTTPAPI_VERSION_GREATER_OR_EQUAL macro

## -syntax

```cpp
int HTTP_GREATER_EQUAL_VERSION(
    HTTP_VERSION version,
    USHORT major,
    USHORT minor
);
```

## -returns

Type: **int**

Returns an integer that is either zero (false) or non-zero (true), that indicates whether or not the value of the _version_ parameter is greater than or equal to the version combination passed in the _major_ and _minor_ parameters.


## -description

The <b>HTTPAPI_VERSION_GREATER_OR_EQUAL</b>  returns a non-zero value if an <a href="/windows/desktop/api/http/ns-http-httpapi_version">HTTPAPI_VERSION</a> structure is greater than or equal to a specified major/minor version combination, or zero otherwise.

## -parameters

### -param version

The <a href="/windows/desktop/api/http/ns-http-httpapi_version">HTTPAPI_VERSION</a> structure to be examined.

### -param major

The major portion of the version to be compared.

### -param minor

The minor portion of the version to be compared.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-1-0-macros">HTTP Server API Version 1.0 Macros</a>
