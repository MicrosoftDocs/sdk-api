---
UID: NS:http._HTTP_SERVICE_CONFIG_URLACL_KEY
title: "_HTTP_SERVICE_CONFIG_URLACL_KEY"
author: windows-sdk-content
description: Used to specify a particular reservation record in the URL namespace reservation store.
old-location: http\http_service_config_urlacl_key.htm
old-project: http
ms.assetid: ab739046-c25c-43bd-8c1f-da3aab374a05
ms.author: windowssdkdev
ms.date: 04/13/2018
ms.keywords: "*PHTTP_SERVICE_CONFIG_URLACL_KEY, HTTP_SERVICE_CONFIG_URLACL_KEY, HTTP_SERVICE_CONFIG_URLACL_KEY structure [HTTP], PHTTP_SERVICE_CONFIG_URLACL_KEY, PHTTP_SERVICE_CONFIG_URLACL_KEY structure pointer [HTTP], _HTTP_SERVICE_CONFIG_URLACL_KEY, _http_http_service_config_urlacl_key, http.http_service_config_urlacl_key, http/HTTP_SERVICE_CONFIG_URLACL_KEY, http/PHTTP_SERVICE_CONFIG_URLACL_KEY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: HTTP_SERVICE_CONFIG_URLACL_KEY, *PHTTP_SERVICE_CONFIG_URLACL_KEY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_SERVICE_CONFIG_URLACL_KEY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _HTTP_SERVICE_CONFIG_URLACL_KEY structure


## -description


The 
<b>HTTP_SERVICE_CONFIG_URLACL_KEY</b> structure is used to specify a particular reservation record in the URL namespace reservation store. It is a member of the 
<a href="https://msdn.microsoft.com/92fc3f65-0153-4075-a61b-48a63c8e0ffe">HTTP_SERVICE_CONFIG_URLACL_SET</a> and 
<a href="https://msdn.microsoft.com/298edd6c-c036-4e45-88f3-84917c8a76ea">HTTP_SERVICE_CONFIG_URLACL_QUERY</a> structures.


## -struct-fields




### -field pUrlPrefix

A pointer to the 
<a href="https://msdn.microsoft.com/4f317bf6-ee6a-47a8-a531-78534217109d">UrlPrefix string</a> that defines the portion of the URL namespace to which this reservation pertains.


## -see-also




<a href="https://msdn.microsoft.com/298edd6c-c036-4e45-88f3-84917c8a76ea">HTTP_SERVICE_CONFIG_URLACL_QUERY</a>



<a href="https://msdn.microsoft.com/92fc3f65-0153-4075-a61b-48a63c8e0ffe">HTTP_SERVICE_CONFIG_URLACL_SET</a>



<a href="https://msdn.microsoft.com/4f317bf6-ee6a-47a8-a531-78534217109d">UrlPrefix Strings</a>
 

 

