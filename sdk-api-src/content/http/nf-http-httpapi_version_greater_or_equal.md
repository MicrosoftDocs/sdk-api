---
UID: NF:http.HTTPAPI_VERSION_GREATER_OR_EQUAL
title: HTTPAPI_VERSION_GREATER_OR_EQUAL macro
author: windows-sdk-content
description: The HTTPAPI_VERSION_GREATER_OR_EQUAL returns a non-zero value if an HTTPAPI_VERSION structure is greater than or equal to a specified major/minor version combination, or zero otherwise.
old-location: http\httpapi_version_greater_or_equal.htm
old-project: http
ms.assetid: d9ac035f-7085-417f-b7df-0607b95f4233
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: HTTPAPI_VERSION_GREATER_OR_EQUAL, HTTPAPI_VERSION_GREATER_OR_EQUAL macro [HTTP], http.httpapi_version_greater_or_equal, http/HTTPAPI_VERSION_GREATER_OR_EQUAL
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: http.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: HTTP_VERB, *PHTTP_VERB
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - http.h
api_name:
 - HTTP_GREATER_EQUAL_VERSION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# HTTPAPI_VERSION_GREATER_OR_EQUAL macro


## -description


The <b>HTTPAPI_VERSION_GREATER_OR_EQUAL</b>  returns a non-zero value if an 
<a href="https://msdn.microsoft.com/af89ecee-2636-4c61-b863-21fe56666ea8">HTTPAPI_VERSION</a> structure is greater than or equal to a specified major/minor version combination, or zero otherwise.


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
 

 

