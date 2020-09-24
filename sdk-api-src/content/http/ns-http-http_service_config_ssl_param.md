---
UID: NS:http._HTTP_SERVICE_CONFIG_SSL_PARAM
title: HTTP_SERVICE_CONFIG_SSL_PARAM (http.h)
description: Defines a record in the SSL configuration store.
helpviewer_keywords: ["*PHTTP_SERVICE_CONFIG_SSL_PARAM","0","0x10000","1","2","4","HTTP_SERVICE_CONFIG_SSL_FLAG_NEGOTIATE_CLIENT_CERT","HTTP_SERVICE_CONFIG_SSL_FLAG_NO_RAW_FILTER","HTTP_SERVICE_CONFIG_SSL_FLAG_USE_DS_MAPPER","HTTP_SERVICE_CONFIG_SSL_PARAM","HTTP_SERVICE_CONFIG_SSL_PARAM structure [HTTP]","PHTTP_SERVICE_CONFIG_SSL_PARAM","PHTTP_SERVICE_CONFIG_SSL_PARAM structure pointer [HTTP]","_http_http_service_config_ssl_param","http.http_service_config_ssl_param","http/HTTP_SERVICE_CONFIG_SSL_PARAM","http/PHTTP_SERVICE_CONFIG_SSL_PARAM"]
old-location: http\http_service_config_ssl_param.htm
tech.root: http
ms.assetid: 2bb3bfe0-9bac-4eb5-80b1-c883503a30b3
ms.date: 12/05/2018
ms.keywords: '*PHTTP_SERVICE_CONFIG_SSL_PARAM, 0, 0x10000, 1, 2, 4, HTTP_SERVICE_CONFIG_SSL_FLAG_NEGOTIATE_CLIENT_CERT, HTTP_SERVICE_CONFIG_SSL_FLAG_NO_RAW_FILTER, HTTP_SERVICE_CONFIG_SSL_FLAG_USE_DS_MAPPER, HTTP_SERVICE_CONFIG_SSL_PARAM, HTTP_SERVICE_CONFIG_SSL_PARAM structure [HTTP], PHTTP_SERVICE_CONFIG_SSL_PARAM, PHTTP_SERVICE_CONFIG_SSL_PARAM structure pointer [HTTP], _http_http_service_config_ssl_param, http.http_service_config_ssl_param, http/HTTP_SERVICE_CONFIG_SSL_PARAM, http/PHTTP_SERVICE_CONFIG_SSL_PARAM'
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
req.typenames: HTTP_SERVICE_CONFIG_SSL_PARAM, *PHTTP_SERVICE_CONFIG_SSL_PARAM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_SERVICE_CONFIG_SSL_PARAM
 - http/_HTTP_SERVICE_CONFIG_SSL_PARAM
 - PHTTP_SERVICE_CONFIG_SSL_PARAM
 - http/PHTTP_SERVICE_CONFIG_SSL_PARAM
 - HTTP_SERVICE_CONFIG_SSL_PARAM
 - http/HTTP_SERVICE_CONFIG_SSL_PARAM
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
 - HTTP_SERVICE_CONFIG_SSL_PARAM
---

# HTTP_SERVICE_CONFIG_SSL_PARAM structure


## -description

The 
<b>HTTP_SERVICE_CONFIG_SSL_PARAM</b> structure defines a record in the SSL configuration store.

## -struct-fields

### -field SslHashLength

The size, in bytes,  of the SSL hash.

### -field pSslHash

A pointer to the SSL certificate hash.

### -field AppId

A unique identifier of the application setting this record.

### -field pSslCertStoreName

A pointer to a wide-character string that contains the name of the store from which the server certificate is to be read. If set to <b>NULL</b>, "MY" is assumed as the default name. The specified certificate store name must be present in the Local System store location.

### -field DefaultCertCheckMode

Determines how client certificates are checked. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
Enables the client certificate revocation check.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Client certificate is not to be verified for revocation.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Only cached certificate revocation is to be used.

</td>
</tr>
<tr>
<td width="40%"><a id="4"></a><dl>
<dt><b>4</b></dt>
</dl>
</td>
<td width="60%">
The <b>DefaultRevocationFreshnessTime</b> setting is enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="0x10000"></a><a id="0X10000"></a><dl>
<dt><b>0x10000</b></dt>
</dl>
</td>
<td width="60%">
No usage check is to be performed.

</td>
</tr>
</table>

### -field DefaultRevocationFreshnessTime

The number of seconds after which to check for an updated certificate revocation list (CRL). If this value is zero, the new CRL is updated only when the previous one expires.

### -field DefaultRevocationUrlRetrievalTimeout

The timeout interval, in milliseconds,  for an attempt to retrieve a certificate revocation list from the remote URL.

### -field pDefaultSslCtlIdentifier

A pointer to an SSL control identifier, which enables an application to restrict the group of certificate issuers to be trusted. This group must be a subset of the certificate issuers trusted by the machine on which the application is running.

### -field pDefaultSslCtlStoreName

The name of the store where the control identifier pointed to by <b>pDefaultSslCtlIdentifier</b> is stored.

### -field DefaultFlags

A combination of zero or more of the following flag values can be combined with OR as appropriate.

<table>
<tr>
<th>Flags</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HTTP_SERVICE_CONFIG_SSL_FLAG_NEGOTIATE_CLIENT_CERT"></a><a id="http_service_config_ssl_flag_negotiate_client_cert"></a><dl>
<dt><b>HTTP_SERVICE_CONFIG_SSL_FLAG_NEGOTIATE_CLIENT_CERT</b></dt>
</dl>
</td>
<td width="60%">
Enables a client certificate to be cached locally for subsequent use.

</td>
</tr>
<tr>
<td width="40%"><a id="HTTP_SERVICE_CONFIG_SSL_FLAG_NO_RAW_FILTER"></a><a id="http_service_config_ssl_flag_no_raw_filter"></a><dl>
<dt><b>HTTP_SERVICE_CONFIG_SSL_FLAG_NO_RAW_FILTER</b></dt>
</dl>
</td>
<td width="60%">
Prevents SSL requests from being passed to low-level ISAPI filters.

</td>
</tr>
<tr>
<td width="40%"><a id="HTTP_SERVICE_CONFIG_SSL_FLAG_USE_DS_MAPPER"></a><a id="http_service_config_ssl_flag_use_ds_mapper"></a><dl>
<dt><b>HTTP_SERVICE_CONFIG_SSL_FLAG_USE_DS_MAPPER</b></dt>
</dl>
</td>
<td width="60%">
Client certificates are mapped where possible to corresponding operating-system user accounts based on the certificate mapping rules stored in Active Directory. 




If this flag is set and the mapping is successful, the <b>Token</b> member of the 
<a href="/windows/desktop/api/http/ns-http-http_ssl_client_cert_info">HTTP_SSL_CLIENT_CERT_INFO</a> structure is a handle to an 
<a href="/windows/desktop/SecAuthZ/access-tokens">access token</a>. Release this token explicitly by closing the handle when the 
<b>HTTP_SSL_CLIENT_CERT_INFO</b> structure is no longer required.

</td>
</tr>
</table>

## -remarks

Together with a 
<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_key">HTTP_SERVICE_CONFIG_SSL_KEY</a> structure, the <b>HTTP_SERVICE_CONFIG_SSL_PARAM</b> structure makes up the 
<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_set">HTTP_SERVICE_CONFIG_SSL_SET</a> structure passed to 
<a href="/windows/desktop/api/http/nf-http-httpsetserviceconfiguration">HttpSetServiceConfiguration</a> function in the <i>pConfigInformation</i> parameter when the <i>ConfigId</i> parameter is set to <b>HttpServiceConfigSSLCertInfo</b>.

Together with a 
<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_ccs_key">HTTP_SERVICE_CONFIG_SSL_CCS_KEY</a> structure, the <b>HTTP_SERVICE_CONFIG_SSL_PARAM</b> structure makes up the 
<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_ccs_set">HTTP_SERVICE_CONFIG_SSL_CCS_SET</a> structure passed to 
<a href="/windows/desktop/api/http/nf-http-httpsetserviceconfiguration">HttpSetServiceConfiguration</a> function in the <i>pConfigInformation</i> parameter when the <i>ConfigId</i> parameter is set to <b>HttpServiceConfigSslCcsCertInfo</b>.

## -see-also

<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_ccs_set">HTTP_SERVICE_CONFIG_SSL_CCS_SET</a>



<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_set">HTTP_SERVICE_CONFIG_SSL_SET</a>



<a href="/windows/desktop/api/http/nf-http-httpsetserviceconfiguration">HttpSetServiceConfiguration</a>