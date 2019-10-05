---
UID: NF:http.HTTPAPI_GREATER_VERSION
title: HTTPAPI_GREATER_VERSION macro (http.h)
author: windows-sdk-content
description: Returns a non-zero value if an HTTPAPI_VERSION structure is greater than a specified major/minor version combination, or zero otherwise.
old-location: http\httpapi_greater_version.htm
tech.root: http
ms.assetid: e70500dd-e750-437c-8652-280f9cc9de1d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: HTTPAPI_GREATER_VERSION, HTTPAPI_GREATER_VERSION macro [HTTP], http.httpapi_greater_version, http/HTTPAPI_GREATER_VERSION
ms.topic: macro
f1_keywords:
- http/HTTP_GREATER_VERSION
dev_langs:
 - c++
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
- http.h
api_name:
- HTTP_GREATER_VERSION
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# HTTPAPI_GREATER_VERSION macro


## -description


The <b>HTTPAPI_GREATER_VERSION</b>returns a non-zero value if an 
<a href="https://docs.microsoft.com/windows/desktop/api/http/ns-http-httpapi_version">HTTPAPI_VERSION</a> structure is greater than a specified major/minor version combination, or zero otherwise.


## -parameters




### -param version

The 
<a href="https://docs.microsoft.com/windows/desktop/api/http/ns-http-httpapi_version">HTTPAPI_VERSION</a> structure to be examined.


### -param major

The major portion of the version to be compared.


### -param minor

The minor portion of the version to be compared.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Http/http-server-api-version-1-0-macros">HTTP Server API Version 1.0 Macros</a>
 

 

