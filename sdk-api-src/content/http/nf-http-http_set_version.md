---
UID: NF:http.HTTP_SET_VERSION
title: HTTP_SET_VERSION macro (http.h)
description: Sets a specified HTTP_VERSION structure to a specified major/minor version combination.helpviewer_keywords: ["HTTP_SET_VERSION","HTTP_SET_VERSION macro [HTTP]","_http_http_set_version","http.http_set_version","http/HTTP_SET_VERSION"]
old-location: http\http_set_version.htm
tech.root: http
ms.assetid: e621ef1c-aa12-400e-ba57-754b8320c419
ms.date: 12/05/2018
ms.keywords: HTTP_SET_VERSION, HTTP_SET_VERSION macro [HTTP], _http_http_set_version, http.http_set_version, http/HTTP_SET_VERSION
f1_keywords:
- http/HTTP_SET_VERSION
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
- HTTP_SET_VERSION
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# HTTP_SET_VERSION macro


## -description


The 
<b>HTTP_SET_VERSION</b> macro sets a specified 
<a href="https://docs.microsoft.com/windows/desktop/api/http/ns-http-http_version">HTTP_VERSION</a> structure to a specified major/minor version combination.


## -parameters




### -param version

The 
<a href="https://docs.microsoft.com/windows/desktop/api/http/ns-http-http_version">HTTP_VERSION</a> structure to be set.


### -param major

The major portion of the version to be used in the <a href="https://docs.microsoft.com/windows/desktop/api/http/ns-http-http_version">HTTP_VERSION</a> structure.


### -param minor

The minor portion of the version to be used in the <a href="https://docs.microsoft.com/windows/desktop/api/http/ns-http-http_version">HTTP_VERSION</a> structure.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Http/http-server-api-version-1-0-macros">HTTP Server API Version 1.0 Macros</a>



<a href="https://docs.microsoft.com/windows/desktop/api/http/ns-http-http_version">HTTP_VERSION</a>
 

 

