---
UID: NS:http._HTTP_SSL_INFO
title: HTTP_SSL_INFO (http.h)
description: Contains data for a connection that uses Secure Sockets Layer (SSL), obtained through the SSL handshake.
helpviewer_keywords: ["*PHTTP_SSL_INFO","HTTP_SSL_INFO","HTTP_SSL_INFO structure [HTTP]","PHTTP_SSL_INFO","PHTTP_SSL_INFO structure pointer [HTTP]","_http_http_ssl_info","http.http_ssl_info","http/HTTP_SSL_INFO","http/PHTTP_SSL_INFO"]
old-location: http\http_ssl_info.htm
tech.root: http
ms.assetid: 35aac36d-87a1-45b2-acb1-6969c992d0cf
ms.date: 12/05/2018
ms.keywords: '*PHTTP_SSL_INFO, HTTP_SSL_INFO, HTTP_SSL_INFO structure [HTTP], PHTTP_SSL_INFO, PHTTP_SSL_INFO structure pointer [HTTP], _http_http_ssl_info, http.http_ssl_info, http/HTTP_SSL_INFO, http/PHTTP_SSL_INFO'
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
req.typenames: HTTP_SSL_INFO, *PHTTP_SSL_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_SSL_INFO
 - http/_HTTP_SSL_INFO
 - PHTTP_SSL_INFO
 - http/PHTTP_SSL_INFO
 - HTTP_SSL_INFO
 - http/HTTP_SSL_INFO
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
 - HTTP_SSL_INFO
---

# HTTP_SSL_INFO structure


## -description

The 
<b>HTTP_SSL_INFO</b> structure contains data for a connection that uses Secure Sockets Layer (SSL), obtained through the SSL handshake.

## -struct-fields

### -field ServerCertKeySize

The size, in bytes, of the public key used to sign the server certificate.

### -field ConnectionKeySize

The size, in bytes, of the cipher key used to encrypt the current session.

### -field ServerCertIssuerSize

The size, in bytes, of the string pointed to by the <b>pServerCertIssuer</b> member not including the terminating null character.

### -field ServerCertSubjectSize

The size, in bytes, of the string pointed to by the <b>pServerCertSubject</b> member not including the terminating null character.

### -field pServerCertIssuer

A pointer to a null-terminated string of octets that specifies the name of the entity that issued the certificate.

### -field pServerCertSubject

A pointer to a null-terminated string of octets that specifies the name of the entity to which the certificate belongs.

### -field pClientCertInfo

A pointer to an 
<a href="/windows/desktop/api/http/ns-http-http_ssl_client_cert_info">HTTP_SSL_CLIENT_CERT_INFO</a> structure that specifies the client certificate.

### -field SslClientCertNegotiated

If non-zero, indicates that the client certificate is already present locally.

## -remarks

An 
<b>HTTP_SSL_INFO</b> structure can be pointed to by the <b>pSslInfo</b> member of an 
<a href="/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)">HTTP_REQUEST</a> structure.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-1-0-structures">HTTP Server API Version 1.0 Structures</a>



<a href="/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)">HTTP_REQUEST</a>



<a href="/windows/desktop/api/http/ns-http-http_ssl_client_cert_info">HTTP_SSL_CLIENT_CERT_INFO</a>