---
UID: NF:http.HTTPAPI_EQUAL_VERSION
title: HTTPAPI_EQUAL_VERSION macro (http.h)
author: windows-sdk-content
description: Returns a non-zero value if an HTTPAPI_VERSION structure is exactly equal to a specified major/minor version combination, or zero otherwise.
old-location: http\httpapi_equal_version.htm
tech.root: http
ms.assetid: e6af7b3a-2e2f-4a50-bef6-9e5b6503cd71
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: HTTPAPI_EQUAL_VERSION, HTTPAPI_EQUAL_VERSION macro [HTTP], http.httpapi_equal_version, http/HTTPAPI_EQUAL_VERSION
ms.topic: macro
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
 - HTTP_EQUAL_VERSION
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# HTTPAPI_EQUAL_VERSION macro


## -description


The <b>HTTPAPI_EQUAL_VERSION</b>returns a non-zero value if an 
<a href="https://msdn.microsoft.com/af89ecee-2636-4c61-b863-21fe56666ea8">HTTPAPI_VERSION</a> structure is exactly equal to a specified major/minor version combination, or zero otherwise.


## -parameters




### -param version

The 
<a href="https://msdn.microsoft.com/af89ecee-2636-4c61-b863-21fe56666ea8">HTTPAPI_VERSION</a> structure to be examined.


### -param major

The major portion of the version to be compared.


### -param minor

The minor portion of the version to be compared.


## -see-also




<a href="https://msdn.microsoft.com/9c5fb0a4-fda8-4489-8a1e-c232079bd501">HTTP Server API Version 1.0 Macros</a>
 

 

