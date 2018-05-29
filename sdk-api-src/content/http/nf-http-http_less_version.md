---
UID: NF:http.HTTP_LESS_VERSION
title: HTTP_LESS_VERSION macro
author: windows-sdk-content
description: Returns a non-zero value if an HTTP_VERSION structure is less than a specified major/minor version combination, or zero otherwise.
old-location: http\http_less_version.htm
old-project: Http
ms.assetid: 3a6486ad-04cb-416f-be5e-bd8f401b0836
ms.author: windowssdkdev
ms.date: 04/12/2018
ms.keywords: HTTP_LESS_VERSION, HTTP_LESS_VERSION macro [HTTP], _http_http_less_version, http.http_less_version, http/HTTP_LESS_VERSION
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
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
req.typenames: HTTP_VERB, *PHTTP_VERB
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Http.h
api_name:
-	HTTP_LESS_VERSION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# HTTP_LESS_VERSION macro


## -description


The 
<b>HTTP_LESS_VERSION</b> macro returns a non-zero value if an 
<a href="https://msdn.microsoft.com/8f97410c-27b5-4225-849e-ee55e4c5f762">HTTP_VERSION</a> structure is less than a specified major/minor version combination, or zero otherwise.


## -parameters




### -param version

The 
<a href="https://msdn.microsoft.com/8f97410c-27b5-4225-849e-ee55e4c5f762">HTTP_VERSION</a> structure to be examined.


### -param major

The major portion of the version to be compared.


### -param minor

The minor portion of the version to be compared.


## -see-also




<a href="https://msdn.microsoft.com/9c5fb0a4-fda8-4489-8a1e-c232079bd501">HTTP Server API Version 1.0 Macros</a>
 

 

