---
UID: NF:http.HTTPAPI_LESS_VERSION
title: HTTPAPI_LESS_VERSION macro
author: windows-sdk-content
description: Returns a non-zero value if an HTTPAPI_VERSION structure is less than a specified major/minor version combination, or zero otherwise.
old-location: http\httpapi_less_version.htm
old-project: Http
ms.assetid: e53d1866-7e5a-43aa-a1b3-287e7cfe3ad8
ms.author: windowssdkdev
ms.date: 04/12/2018
ms.keywords: HTTPAPI_LESS_VERSION, HTTPAPI_LESS_VERSION macro [HTTP], http.httpapi_less_version, http/HTTPAPI_LESS_VERSION
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: HTTP_VERB, *PHTTP_VERB
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	http.h
api_name:
-	HTTP_LESS_VERSION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# HTTPAPI_LESS_VERSION macro


## -description


The <b>HTTPAPI_LESS_VERSION</b>returns a non-zero value if an 
<a href="https://msdn.microsoft.com/af89ecee-2636-4c61-b863-21fe56666ea8">HTTPAPI_VERSION</a> structure is less than a specified major/minor version combination, or zero otherwise.


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
 

 

