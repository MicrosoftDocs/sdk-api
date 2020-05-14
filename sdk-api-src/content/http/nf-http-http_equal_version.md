---
UID: NF:http.HTTP_EQUAL_VERSION
title: HTTP_EQUAL_VERSION macro (http.h)
description: Returns a non-zero value if an HTTP_VERSION structure is equal to a specified major/minor version combination, or zero otherwise.helpviewer_keywords: ["HTTP_EQUAL_VERSION","HTTP_EQUAL_VERSION macro [HTTP]","_http_http_equal_version","http.http_equal_version","http/HTTP_EQUAL_VERSION"]
old-location: http\http_equal_version.htm
tech.root: http
ms.assetid: bcbe0e43-5164-4571-b672-2af547468f8f
ms.date: 12/05/2018
ms.keywords: HTTP_EQUAL_VERSION, HTTP_EQUAL_VERSION macro [HTTP], _http_http_equal_version, http.http_equal_version, http/HTTP_EQUAL_VERSION
f1_keywords:
- http/HTTP_EQUAL_VERSION
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Http.h
api_name:
- HTTP_EQUAL_VERSION
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# HTTP_EQUAL_VERSION macro


## -description


The 
<b>HTTP_EQUAL_VERSION</b> macro returns a non-zero value if an 
<a href="https://docs.microsoft.com/windows/desktop/api/http/ns-http-http_version">HTTP_VERSION</a> structure is equal to a specified major/minor version combination, or zero otherwise.


## -parameters




### -param version

The 
<a href="https://docs.microsoft.com/windows/desktop/api/http/ns-http-http_version">HTTP_VERSION</a> structure to be examined.


### -param major

A major portion of the version to be compared.


### -param minor

A minor portion of the version to be compared.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Http/http-server-api-version-1-0-macros">HTTP Server API Version 1.0 Macros</a>
 

 

