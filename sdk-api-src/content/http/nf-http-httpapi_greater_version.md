---
UID: NF:http.HTTPAPI_GREATER_VERSION
title: HTTPAPI_GREATER_VERSION macro
author: windows-sdk-content
description: Returns a non-zero value if an HTTPAPI_VERSION structure is greater than a specified major/minor version combination, or zero otherwise.
old-location: http\httpapi_greater_version.htm
tech.root: Http
ms.assetid: e70500dd-e750-437c-8652-280f9cc9de1d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: HTTPAPI_GREATER_VERSION, HTTPAPI_GREATER_VERSION macro [HTTP], http.httpapi_greater_version, http/HTTPAPI_GREATER_VERSION
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - HTTP_GREATER_VERSION
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- http.h
: 
- HTTPAPI_GREATER_VERSION
: 
---

# HTTPAPI_GREATER_VERSION macro


## -description


The <b>HTTPAPI_GREATER_VERSION</b>returns a non-zero value if an 
<a href="https://msdn.microsoft.com/af89ecee-2636-4c61-b863-21fe56666ea8">HTTPAPI_VERSION</a> structure is greater than a specified major/minor version combination, or zero otherwise.


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
 

 

