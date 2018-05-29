---
UID: NF:http.HTTP_SET_VERSION
title: HTTP_SET_VERSION macro
author: windows-sdk-content
description: Sets a specified HTTP_VERSION structure to a specified major/minor version combination.
old-location: http\http_set_version.htm
old-project: Http
ms.assetid: e621ef1c-aa12-400e-ba57-754b8320c419
ms.author: windowssdkdev
ms.date: 04/12/2018
ms.keywords: HTTP_SET_VERSION, HTTP_SET_VERSION macro [HTTP], _http_http_set_version, http.http_set_version, http/HTTP_SET_VERSION
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
-	HTTP_SET_VERSION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# HTTP_SET_VERSION macro


## -description


The 
<b>HTTP_SET_VERSION</b> macro sets a specified 
<a href="https://msdn.microsoft.com/8f97410c-27b5-4225-849e-ee55e4c5f762">HTTP_VERSION</a> structure to a specified major/minor version combination.


## -parameters




### -param version

The 
<a href="https://msdn.microsoft.com/8f97410c-27b5-4225-849e-ee55e4c5f762">HTTP_VERSION</a> structure to be set.


### -param major

The major portion of the version to be used in the <a href="https://msdn.microsoft.com/8f97410c-27b5-4225-849e-ee55e4c5f762">HTTP_VERSION</a> structure.


### -param minor

The minor portion of the version to be used in the <a href="https://msdn.microsoft.com/8f97410c-27b5-4225-849e-ee55e4c5f762">HTTP_VERSION</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/9c5fb0a4-fda8-4489-8a1e-c232079bd501">HTTP Server API Version 1.0 Macros</a>



<a href="https://msdn.microsoft.com/8f97410c-27b5-4225-849e-ee55e4c5f762">HTTP_VERSION</a>
 

 

