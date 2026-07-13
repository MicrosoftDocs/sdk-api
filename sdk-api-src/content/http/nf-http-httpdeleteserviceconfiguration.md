---
UID: NF:http.HttpDeleteServiceConfiguration
title: HttpDeleteServiceConfiguration function (http.h)
description: Deletes specified data, such as IP addresses or SSL Certificates, from the HTTP Server API configuration store, one record at a time.
helpviewer_keywords: ["HttpDeleteServiceConfiguration","HttpDeleteServiceConfiguration function [HTTP]","HttpServiceConfigIPListenList","HttpServiceConfigSSLCertInfo","HttpServiceConfigSslCcsCertInfo","HttpServiceConfigSslSniCertInfo","HttpServiceConfigTimeout","HttpServiceConfigTimeouts","HttpServiceConfigUrlAclInfo","_http_httpdeleteserviceconfiguration","http.httpdeleteserviceconfiguration","http/HttpDeleteServiceConfiguration"]
old-location: http\httpdeleteserviceconfiguration.htm
tech.root: http
ms.assetid: 0ae94936-4c6a-4c9f-adb8-5e3af75cf486
ms.date: 12/05/2018
ms.keywords: HttpDeleteServiceConfiguration, HttpDeleteServiceConfiguration function [HTTP], HttpServiceConfigIPListenList, HttpServiceConfigSSLCertInfo, HttpServiceConfigSslCcsCertInfo, HttpServiceConfigSslSniCertInfo, HttpServiceConfigTimeout, HttpServiceConfigTimeouts, HttpServiceConfigUrlAclInfo, _http_httpdeleteserviceconfiguration, http.httpdeleteserviceconfiguration, http/HttpDeleteServiceConfiguration
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
req.lib: Httpapi.lib
req.dll: Httpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HttpDeleteServiceConfiguration
 - http/HttpDeleteServiceConfiguration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Httpapi.dll
api_name:
 - HttpDeleteServiceConfiguration
---

# HttpDeleteServiceConfiguration function


## -description

The 
<b>HttpDeleteServiceConfiguration</b> function deletes specified data, such as IP addresses or SSL Certificates, from the HTTP Server API configuration store, one record at a time.

## -parameters

### -param ServiceHandle [in]

This parameter is reserved and must be zero.

### -param ConfigId [in]

Type of configuration. This parameter is one of the  values in 
the <a href="/windows/desktop/api/http/ne-http-http_service_config_id">HTTP_SERVICE_CONFIG_ID</a> enumeration.

<table>
<tr>
<th><i>ConfigId</i> value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigIPListenList"></a><a id="httpserviceconfigiplistenlist"></a><a id="HTTPSERVICECONFIGIPLISTENLIST"></a><dl>
<dt><b>HttpServiceConfigIPListenList</b></dt>
</dl>
</td>
<td width="60%">
Deletes a specified IP address from the IP Listen List.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigSSLCertInfo"></a><a id="httpserviceconfigsslcertinfo"></a><a id="HTTPSERVICECONFIGSSLCERTINFO"></a><dl>
<dt><b>HttpServiceConfigSSLCertInfo</b></dt>
</dl>
</td>
<td width="60%">
Deletes a specified SSL certificate record.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigUrlAclInfo"></a><a id="httpserviceconfigurlaclinfo"></a><a id="HTTPSERVICECONFIGURLACLINFO"></a><dl>
<dt><b>HttpServiceConfigUrlAclInfo</b></dt>
</dl>
</td>
<td width="60%">
Deletes a specified URL reservation record.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigTimeout"></a><a id="httpserviceconfigtimeout"></a><a id="HTTPSERVICECONFIGTIMEOUT"></a><dl>
<dt><b>HttpServiceConfigTimeout</b></dt>
</dl>
</td>
<td width="60%">
Deletes a specified connection timeout.


<b>Windows Vista and later:  </b>This enumeration is supported.



</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigSslSniCertInfo"></a><a id="httpserviceconfigsslsnicertinfo"></a><a id="HTTPSERVICECONFIGSSLSNICERTINFO"></a><dl>
<dt><b>HttpServiceConfigSslSniCertInfo</b></dt>
</dl>
</td>
<td width="60%">
Deletes a specified SSL Server Name Indication (SNI) certificate record.

<b>Windows 8 and later:  </b>This enumeration value is supported.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigSslCcsCertInfo"></a><a id="httpserviceconfigsslccscertinfo"></a><a id="HTTPSERVICECONFIGSSLCCSCERTINFO"></a><dl>
<dt><b>HttpServiceConfigSslCcsCertInfo</b></dt>
</dl>
</td>
<td width="60%">
Deletes the   SSL certificate record that specifies that Http.sys should consult the Centralized Certificate Store (CCS) store to find certificates if the port receives a Transport Layer Security (TLS) handshake.  The port is specified by the <b>KeyDesc</b> member of the <a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_ccs_set">HTTP_SERVICE_CONFIG_SSL_CCS_SET</a> structure that you  pass to the <i>pConfigInformation</i> parameter.

<b>Windows 8 and later:  </b>This enumeration value is supported.

</td>
</tr>
</table>

### -param pConfigInformation [in]

Pointer to a buffer that contains data required for the type of configuration specified in the <i>ConfigId</i> parameter.

<table>
<tr>
<th><i>ConfigId</i> value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigIPListenList"></a><a id="httpserviceconfigiplistenlist"></a><a id="HTTPSERVICECONFIGIPLISTENLIST"></a><dl>
<dt><b>HttpServiceConfigIPListenList</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/http/ns-http-http_service_config_ip_listen_param">HTTP_SERVICE_CONFIG_IP_LISTEN_PARAM</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigSSLCertInfo"></a><a id="httpserviceconfigsslcertinfo"></a><a id="HTTPSERVICECONFIGSSLCERTINFO"></a><dl>
<dt><b>HttpServiceConfigSSLCertInfo</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_set">HTTP_SERVICE_CONFIG_SSL_SET</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigUrlAclInfo"></a><a id="httpserviceconfigurlaclinfo"></a><a id="HTTPSERVICECONFIGURLACLINFO"></a><dl>
<dt><b>HttpServiceConfigUrlAclInfo</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/http/ns-http-http_service_config_urlacl_set">HTTP_SERVICE_CONFIG_URLACL_SET</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigTimeouts"></a><a id="httpserviceconfigtimeouts"></a><a id="HTTPSERVICECONFIGTIMEOUTS"></a><dl>
<dt><b>HttpServiceConfigTimeouts</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/http/ne-http-http_service_config_timeout_key">HTTP_SERVICE_CONFIG_TIMEOUT_KEY</a> structure.


<b>Windows Vista and later:  </b>This structure is supported.



</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigSslSniCertInfo"></a><a id="httpserviceconfigsslsnicertinfo"></a><a id="HTTPSERVICECONFIGSSLSNICERTINFO"></a><dl>
<dt><b>HttpServiceConfigSslSniCertInfo</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_sni_set">HTTP_SERVICE_CONFIG_SSL_SNI_SET</a> structure. The hostname will be "*" when the SSL central certificate store is queried and wildcard bindings are used, and a host name for regular SNI.


<b>Windows 8 and later:  </b>This structure is supported.



</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigSslCcsCertInfo"></a><a id="httpserviceconfigsslccscertinfo"></a><a id="HTTPSERVICECONFIGSSLCCSCERTINFO"></a><dl>
<dt><b>HttpServiceConfigSslCcsCertInfo</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_ccs_set">HTTP_SERVICE_CONFIG_SSL_CCS_SET</a> structure.


<b>Windows 8 and later:  </b>This structure is supported.



</td>
</tr>
</table>

### -param ConfigInformationLength [in]

Size, in bytes, of the <i>pConfigInformation</i> buffer.

### -param pOverlapped [in]

Reserved for future asynchronous operation. This parameter must be set to <b>NULL</b>.

## -returns

If the function succeeds, the function returns NO_ERROR.

If the function fails, it returns one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
A <a href="/windows/desktop/Debug/system-error-codes">system error code</a> defined in WinError.h.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-1-0-functions">HTTP Server API Version 1.0 Functions</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HttpQueryServiceConfiguration</a>



<a href="/windows/desktop/api/http/nf-http-httpsetserviceconfiguration">HttpSetServiceConfiguration</a>



<a href="/windows/desktop/api/http/nf-http-httpupdateserviceconfiguration">HttpUpdateServiceConfiguration</a>