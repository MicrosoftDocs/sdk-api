---
UID: NS:http._HTTP_SERVICE_CONFIG_URLACL_PARAM
title: HTTP_SERVICE_CONFIG_URLACL_PARAM (http.h)
description: Used to specify the permissions associated with a particular record in the URL namespace reservation store.
helpviewer_keywords: ["*PHTTP_SERVICE_CONFIG_URLACL_PARAM","HTTP_SERVICE_CONFIG_URLACL_PARAM","HTTP_SERVICE_CONFIG_URLACL_PARAM structure [HTTP]","PHTTP_SERVICE_CONFIG_URLACL_PARAM","PHTTP_SERVICE_CONFIG_URLACL_PARAM structure pointer [HTTP]","_http_http_service_config_urlacl_param","http.http_service_config_urlacl_param","http/HTTP_SERVICE_CONFIG_URLACL_PARAM","http/PHTTP_SERVICE_CONFIG_URLACL_PARAM"]
old-location: http\http_service_config_urlacl_param.htm
tech.root: http
ms.assetid: 5fd50d77-cd2b-47d7-baa3-ed1d7fc934a7
ms.date: 12/05/2018
ms.keywords: '*PHTTP_SERVICE_CONFIG_URLACL_PARAM, HTTP_SERVICE_CONFIG_URLACL_PARAM, HTTP_SERVICE_CONFIG_URLACL_PARAM structure [HTTP], PHTTP_SERVICE_CONFIG_URLACL_PARAM, PHTTP_SERVICE_CONFIG_URLACL_PARAM structure pointer [HTTP], _http_http_service_config_urlacl_param, http.http_service_config_urlacl_param, http/HTTP_SERVICE_CONFIG_URLACL_PARAM, http/PHTTP_SERVICE_CONFIG_URLACL_PARAM'
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
req.typenames: HTTP_SERVICE_CONFIG_URLACL_PARAM, *PHTTP_SERVICE_CONFIG_URLACL_PARAM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_SERVICE_CONFIG_URLACL_PARAM
 - http/_HTTP_SERVICE_CONFIG_URLACL_PARAM
 - PHTTP_SERVICE_CONFIG_URLACL_PARAM
 - http/PHTTP_SERVICE_CONFIG_URLACL_PARAM
 - HTTP_SERVICE_CONFIG_URLACL_PARAM
 - http/HTTP_SERVICE_CONFIG_URLACL_PARAM
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
 - HTTP_SERVICE_CONFIG_URLACL_PARAM
---

# HTTP_SERVICE_CONFIG_URLACL_PARAM structure


## -description

The 
<b>HTTP_SERVICE_CONFIG_URLACL_PARAM</b> structure is used to specify the permissions associated with a particular record in the URL namespace reservation store. It is a member of the 
<a href="/windows/desktop/api/http/ns-http-http_service_config_urlacl_set">HTTP_SERVICE_CONFIG_URLACL_SET</a> structure.

## -struct-fields

### -field pStringSecurityDescriptor

A pointer to a 
<a href="/windows/desktop/SecAuthZ/security-descriptor-string-format">Security Descriptor Definition Language (SDDL) string</a> that contains the permissions associated with this URL namespace reservation record.

## -remarks

The security descriptor string pointed to by the <b>pStringSecurityDescriptor</b> member has the following elements:



An example of a security descriptor string is:


``` syntax
D:(A;;GX;;;S-1-0-0)(A;;GA;;;S-1-5-11)

```


## -see-also

<a href="/windows/desktop/api/http/ns-http-http_service_config_urlacl_set">HTTP_SERVICE_CONFIG_URLACL_SET</a>



<a href="/windows/desktop/SecAuthZ/security-descriptor-string-format">Security Descriptor String Format</a>
