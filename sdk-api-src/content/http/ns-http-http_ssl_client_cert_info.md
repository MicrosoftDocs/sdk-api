---
UID: NS:http._HTTP_SSL_CLIENT_CERT_INFO
title: HTTP_SSL_CLIENT_CERT_INFO (http.h)
description: Contains data about a Secure Sockets Layer (SSL) client certificate that can be used to determine whether the certificate is valid.
helpviewer_keywords: ["*PHTTP_SSL_CLIENT_CERT_INFO","CERT_E_CN_NO_MATCH","CERT_E_EXPIRED","CERT_E_REVOKED","CERT_E_UNTRUSTEDCA","CERT_E_UNTRUSTEDROOT","CERT_E_WRONG_USAGE","HTTP_SSL_CLIENT_CERT_INFO","HTTP_SSL_CLIENT_CERT_INFO structure [HTTP]","PHTTP_SSL_CLIENT_CERT_INFO","PHTTP_SSL_CLIENT_CERT_INFO structure pointer [HTTP]","_http_http_ssl_client_cert_info","http.http_ssl_client_cert_info","http/HTTP_SSL_CLIENT_CERT_INFO","http/PHTTP_SSL_CLIENT_CERT_INFO"]
old-location: http\http_ssl_client_cert_info.htm
tech.root: http
ms.assetid: bfe6a9a9-6117-4403-a83f-e9448615500b
ms.date: 12/05/2018
ms.keywords: '*PHTTP_SSL_CLIENT_CERT_INFO, CERT_E_CN_NO_MATCH, CERT_E_EXPIRED, CERT_E_REVOKED, CERT_E_UNTRUSTEDCA, CERT_E_UNTRUSTEDROOT, CERT_E_WRONG_USAGE, HTTP_SSL_CLIENT_CERT_INFO, HTTP_SSL_CLIENT_CERT_INFO structure [HTTP], PHTTP_SSL_CLIENT_CERT_INFO, PHTTP_SSL_CLIENT_CERT_INFO structure pointer [HTTP], _http_http_ssl_client_cert_info, http.http_ssl_client_cert_info, http/HTTP_SSL_CLIENT_CERT_INFO, http/PHTTP_SSL_CLIENT_CERT_INFO'
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
req.typenames: HTTP_SSL_CLIENT_CERT_INFO, *PHTTP_SSL_CLIENT_CERT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_SSL_CLIENT_CERT_INFO
 - http/_HTTP_SSL_CLIENT_CERT_INFO
 - PHTTP_SSL_CLIENT_CERT_INFO
 - http/PHTTP_SSL_CLIENT_CERT_INFO
 - HTTP_SSL_CLIENT_CERT_INFO
 - http/HTTP_SSL_CLIENT_CERT_INFO
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
 - HTTP_SSL_CLIENT_CERT_INFO
---

# HTTP_SSL_CLIENT_CERT_INFO structure


## -description

The 
<b>HTTP_SSL_CLIENT_CERT_INFO</b> structure contains data about a Secure Sockets Layer (SSL) client certificate that can be used to determine whether the certificate is valid.

## -struct-fields

### -field CertFlags

Flags that indicate whether the certificate is valid. The possible values for this member are 
a <a href="/windows/desktop/SecAuthN/sspi-status-codes">SSPI Status Code</a> returned from SSPI or one of the following flags from the <b>dwError</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_status">CERT_CHAIN_POLICY_STATUS</a> structure:

<a id="CERT_E_EXPIRED"></a>
<a id="cert_e_expired"></a>


#### CERT_E_EXPIRED

<a id="CERT_E_UNTRUSTEDCA"></a>
<a id="cert_e_untrustedca"></a>


#### CERT_E_UNTRUSTEDCA

<a id="CERT_E_WRONG_USAGE"></a>
<a id="cert_e_wrong_usage"></a>


#### CERT_E_WRONG_USAGE

<a id="CERT_E_UNTRUSTEDROOT"></a>
<a id="cert_e_untrustedroot"></a>


#### CERT_E_UNTRUSTEDROOT

<a id="CERT_E_REVOKED"></a>
<a id="cert_e_revoked"></a>


#### CERT_E_REVOKED

<a id="CERT_E_CN_NO_MATCH"></a>
<a id="cert_e_cn_no_match"></a>


#### CERT_E_CN_NO_MATCH

### -field CertEncodedSize

The size, in bytes, of the certificate.

### -field pCertEncoded

A pointer to the actual certificate.

### -field Token

A handle to an access token. If the HTTP_SERVICE_CONFIG_SSL_FLAG_USE_DS_MAPPER flag is set using the 
<a href="/windows/desktop/api/http/nf-http-httpsetserviceconfiguration">HttpSetServiceConfiguration</a> function, and the client certificate was successfully mapped to an operating-system user account, then this member contains the handle to a valid 
<a href="/windows/desktop/SecAuthZ/access-tokens">access token</a>. When the 
<b>HTTP_SSL_CLIENT_CERT_INFO</b> structure is no longer required, release this token explicitly by closing the handle.

### -field CertDeniedByMapper

Reserved.

## -remarks

An 
<b>HTTP_SSL_CLIENT_CERT_INFO</b> structure is pointed to by the <b>pClientCertInfo</b> member of the 
<a href="/windows/desktop/api/http/ns-http-http_ssl_info">HTTP_SSL_INFO</a> structure, and is used by the 
<a href="/windows/desktop/api/http/nf-http-httpreceiveclientcertificate">HttpReceiveClientCertificate</a> function to return data about the client certificate through the <i>pSslClientCertInfo</i> parameter.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-1-0-structures">HTTP Server API Version 1.0 Structures</a>



<a href="/windows/desktop/api/http/ns-http-http_ssl_info">HTTP_SSL_INFO</a>



<a href="/windows/desktop/api/http/nf-http-httpreceiveclientcertificate">HttpReceiveClientCertificate</a>