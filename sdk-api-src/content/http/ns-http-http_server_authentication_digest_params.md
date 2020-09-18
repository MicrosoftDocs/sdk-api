---
UID: NS:http._HTTP_SERVER_AUTHENTICATION_DIGEST_PARAMS
title: HTTP_SERVER_AUTHENTICATION_DIGEST_PARAMS (http.h)
description: Contains the information for digest authentication on a URL Group.
helpviewer_keywords: ["*PHTTP_SERVER_AUTHENTICATION_DIGEST_PARAMS","*PHTTP_SERVER_AUTHENTICATION_DIGEST_PARAMS structure [HTTP]","HTTP_SERVER_AUTHENTICATION_DIGEST_PARAMS","HTTP_SERVER_AUTHENTICATION_DIGEST_PARAMS structure [HTTP]","http.http_server_authentication_digest_params","http/*PHTTP_SERVER_AUTHENTICATION_DIGEST_PARAMS","http/HTTP_SERVER_AUTHENTICATION_DIGEST_PARAMS"]
old-location: http\http_server_authentication_digest_params.htm
tech.root: http
ms.assetid: 923d06ed-8f34-46b6-98d8-96828848dca8
ms.date: 12/05/2018
ms.keywords: '*PHTTP_SERVER_AUTHENTICATION_DIGEST_PARAMS, *PHTTP_SERVER_AUTHENTICATION_DIGEST_PARAMS structure [HTTP], HTTP_SERVER_AUTHENTICATION_DIGEST_PARAMS, HTTP_SERVER_AUTHENTICATION_DIGEST_PARAMS structure [HTTP], http.http_server_authentication_digest_params, http/*PHTTP_SERVER_AUTHENTICATION_DIGEST_PARAMS, http/HTTP_SERVER_AUTHENTICATION_DIGEST_PARAMS'
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: HTTP_SERVER_AUTHENTICATION_DIGEST_PARAMS, *PHTTP_SERVER_AUTHENTICATION_DIGEST_PARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_SERVER_AUTHENTICATION_DIGEST_PARAMS
 - http/_HTTP_SERVER_AUTHENTICATION_DIGEST_PARAMS
 - PHTTP_SERVER_AUTHENTICATION_DIGEST_PARAMS
 - http/PHTTP_SERVER_AUTHENTICATION_DIGEST_PARAMS
 - HTTP_SERVER_AUTHENTICATION_DIGEST_PARAMS
 - http/HTTP_SERVER_AUTHENTICATION_DIGEST_PARAMS
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
 - HTTP_SERVER_AUTHENTICATION_DIGEST_PARAMS
---

# HTTP_SERVER_AUTHENTICATION_DIGEST_PARAMS structure


## -description

The <b>HTTP_SERVER_AUTHENTICATION_DIGEST_PARAMS</b> structure contains the information for digest authentication on a URL Group.

This structure is contained in the <a href="/windows/desktop/api/http/ns-http-http_server_authentication_info">HTTP_SERVER_AUTHENTICATION_INFO</a> structure.

## -struct-fields

### -field DomainNameLength

The length, in bytes, of the <b>DomainName</b> member.

### -field DomainName

The domain name used for Digest authentication.

If <b>NULL</b>, the client assumes the protection space consists of all the URIs under the responding server.

### -field RealmLength

The length, in bytes, of the <b>Realm</b> member.

### -field Realm

The realm used for Digest authentication.

The realm allows the  server to be partitioned into a set of protection spaces, each with its own set of authentication schemes from the authentication database.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-structures">HTTP Server API Version 2.0 Structures</a>



<a href="/windows/desktop/api/http/ns-http-http_server_authentication_info">HTTP_SERVER_AUTHENTICATION_INFO</a>