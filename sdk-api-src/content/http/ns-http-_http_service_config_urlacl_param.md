---
UID: NS:http._HTTP_SERVICE_CONFIG_URLACL_PARAM
title: "_HTTP_SERVICE_CONFIG_URLACL_PARAM"
author: windows-driver-content
description: Used to specify the permissions associated with a particular record in the URL namespace reservation store.
old-location: http\http_service_config_urlacl_param.htm
old-project: Http
ms.assetid: 5fd50d77-cd2b-47d7-baa3-ed1d7fc934a7
ms.author: windowsdriverdev
ms.date: 4/12/2018
ms.keywords: "*PHTTP_SERVICE_CONFIG_URLACL_PARAM, HTTP_SERVICE_CONFIG_URLACL_PARAM, HTTP_SERVICE_CONFIG_URLACL_PARAM structure [HTTP], PHTTP_SERVICE_CONFIG_URLACL_PARAM, PHTTP_SERVICE_CONFIG_URLACL_PARAM structure pointer [HTTP], _HTTP_SERVICE_CONFIG_URLACL_PARAM, _http_http_service_config_urlacl_param, http.http_service_config_urlacl_param, http/HTTP_SERVICE_CONFIG_URLACL_PARAM, http/PHTTP_SERVICE_CONFIG_URLACL_PARAM"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: HTTP_SERVICE_CONFIG_URLACL_PARAM, *PHTTP_SERVICE_CONFIG_URLACL_PARAM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Http.h
api_name:
-	HTTP_SERVICE_CONFIG_URLACL_PARAM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _HTTP_SERVICE_CONFIG_URLACL_PARAM structure


## -description


The 
<b>HTTP_SERVICE_CONFIG_URLACL_PARAM</b> structure is used to specify the permissions associated with a particular record in the URL namespace reservation store. It is a member of the 
<a href="https://msdn.microsoft.com/92fc3f65-0153-4075-a61b-48a63c8e0ffe">HTTP_SERVICE_CONFIG_URLACL_SET</a> structure.


## -struct-fields




### -field pStringSecurityDescriptor

A pointer to a 
<a href="https://msdn.microsoft.com/0a226629-084c-40c5-bdd4-ad7355c807cf">Security Descriptor Definition Language (SDDL) string</a> that contains the permissions associated with this URL namespace reservation record.


## -remarks



The security descriptor string pointed to by the <b>pStringSecurityDescriptor</b> member has the following elements:



An example of a security descriptor string is:

<pre class="syntax" xml:space="preserve"><code>D:(A;;GX;;;S-1-0-0)(A;;GA;;;S-1-5-11)
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/92fc3f65-0153-4075-a61b-48a63c8e0ffe">HTTP_SERVICE_CONFIG_URLACL_SET</a>



<a href="https://msdn.microsoft.com/0a226629-084c-40c5-bdd4-ad7355c807cf">Security Descriptor String Format</a>
 

 

