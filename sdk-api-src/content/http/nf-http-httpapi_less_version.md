---
UID: NF:http.HTTPAPI_LESS_VERSION
title: HTTPAPI_LESS_VERSION macro (http.h)
description: Returns a non-zero value if an HTTPAPI_VERSION structure is less than a specified major/minor version combination, or zero otherwise.
helpviewer_keywords: ["HTTPAPI_LESS_VERSION","HTTPAPI_LESS_VERSION macro [HTTP]","http.httpapi_less_version","http/HTTPAPI_LESS_VERSION"]
old-location: http\httpapi_less_version.htm
tech.root: http
ms.assetid: e53d1866-7e5a-43aa-a1b3-287e7cfe3ad8
ms.date: 12/05/2018
ms.keywords: HTTPAPI_LESS_VERSION, HTTPAPI_LESS_VERSION macro [HTTP], http.httpapi_less_version, http/HTTPAPI_LESS_VERSION
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
 - HTTPAPI_LESS_VERSION
 - http/HTTPAPI_LESS_VERSION
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
 - HTTP_LESS_VERSION
---

# HTTPAPI_LESS_VERSION macro


## -description

The <b>HTTPAPI_LESS_VERSION</b> returns a non-zero value if an 
<a href="/windows/desktop/api/http/ns-http-httpapi_version">HTTPAPI_VERSION</a> structure is less than a specified major/minor version combination, or zero otherwise.

## -parameters

### -param version

The 
<a href="/windows/desktop/api/http/ns-http-httpapi_version">HTTPAPI_VERSION</a> structure to be examined.

### -param major

The major portion of the version to be compared.

### -param minor

The minor portion of the version to be compared.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-1-0-macros">HTTP Server API Version 1.0 Macros</a>