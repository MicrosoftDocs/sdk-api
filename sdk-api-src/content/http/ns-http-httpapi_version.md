---
UID: NS:http._HTTPAPI_VERSION
title: HTTPAPI_VERSION (http.h)
description: Defines the version of the HTTP Server API.
helpviewer_keywords: ["*PHTTPAPI_VERSION","HTTPAPI_VERSION","HTTPAPI_VERSION structure [HTTP]","PHTTPAPI_VERSION","PHTTPAPI_VERSION structure pointer [HTTP]","_http_httpapi_version","http.httpapi_version","http/HTTPAPI_VERSION","http/PHTTPAPI_VERSION"]
old-location: http\httpapi_version.htm
tech.root: http
ms.assetid: af89ecee-2636-4c61-b863-21fe56666ea8
ms.date: 12/05/2018
ms.keywords: '*PHTTPAPI_VERSION, HTTPAPI_VERSION, HTTPAPI_VERSION structure [HTTP], PHTTPAPI_VERSION, PHTTPAPI_VERSION structure pointer [HTTP], _http_httpapi_version, http.httpapi_version, http/HTTPAPI_VERSION, http/PHTTPAPI_VERSION'
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
req.typenames: HTTPAPI_VERSION, *PHTTPAPI_VERSION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTPAPI_VERSION
 - http/_HTTPAPI_VERSION
 - PHTTPAPI_VERSION
 - http/PHTTPAPI_VERSION
 - HTTPAPI_VERSION
 - http/HTTPAPI_VERSION
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
 - HTTPAPI_VERSION
---

# HTTPAPI_VERSION structure


## -description

The 
<b>HTTPAPI_VERSION</b> structure defines the version of the HTTP Server API. This is not to be confused with the version of the HTTP protocol used, which is stored in an 
<b>HTTP_VERSION</b> structure.

## -struct-fields

### -field HttpApiMajorVersion

Major version of the HTTP Server API.

### -field HttpApiMinorVersion

Minor version of the HTTP Server API.

## -remarks

Constants that represents the version of the API  are pre-defined in the Http.h header file as follows:

"#define HTTPAPI_VERSION_1 {1, 0}"

"#define HTTPAPI_VERSION_2 {2, 0}"

