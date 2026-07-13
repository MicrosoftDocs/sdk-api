---
UID: NF:http.HttpSetServiceConfiguration
title: HttpSetServiceConfiguration function (http.h)
description: Creates and sets a configuration record for the HTTP Server API configuration store.
helpviewer_keywords: ["HttpServiceConfigIPListenList","HttpServiceConfigSSLCertInfo","HttpServiceConfigSslCcsCertInfo","HttpServiceConfigSslSniCertInfo","HttpServiceConfigTimeout","HttpServiceConfigUrlAclInfo","HttpSetServiceConfiguration","HttpSetServiceConfiguration function [HTTP]","_http_httpsetserviceconfiguration","http.httpsetserviceconfiguration","http/HttpSetServiceConfiguration"]
old-location: http\httpsetserviceconfiguration.htm
tech.root: http
ms.assetid: b0a6d442-2ff4-4e00-8301-696fb0864d8c
ms.date: 12/05/2018
ms.keywords: HttpServiceConfigIPListenList, HttpServiceConfigSSLCertInfo, HttpServiceConfigSslCcsCertInfo, HttpServiceConfigSslSniCertInfo, HttpServiceConfigTimeout, HttpServiceConfigUrlAclInfo, HttpSetServiceConfiguration, HttpSetServiceConfiguration function [HTTP], _http_httpsetserviceconfiguration, http.httpsetserviceconfiguration, http/HttpSetServiceConfiguration
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
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
 - HttpSetServiceConfiguration
 - http/HttpSetServiceConfiguration
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
 - HttpSetServiceConfiguration
---

# HttpSetServiceConfiguration function


## -description

The 
<b>HttpSetServiceConfiguration</b> function creates and sets a configuration record for the HTTP Server API configuration store. The call fails if the specified record already exists. To change a given configuration record, delete it and then recreate it with a different value.

## -parameters

### -param ServiceHandle [in]

Reserved. Must be zero.

### -param ConfigId [in]

Type of configuration record to be set. This parameter can be one of the following values from the <a href="/windows/desktop/api/http/ne-http-http_service_config_id">HTTP_SERVICE_CONFIG_ID</a> enumeration.

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
Sets a record in the IP Listen List.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigSSLCertInfo"></a><a id="httpserviceconfigsslcertinfo"></a><a id="HTTPSERVICECONFIGSSLCERTINFO"></a><dl>
<dt><b>HttpServiceConfigSSLCertInfo</b></dt>
</dl>
</td>
<td width="60%">
Sets a specified SSL certificate record.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigUrlAclInfo"></a><a id="httpserviceconfigurlaclinfo"></a><a id="HTTPSERVICECONFIGURLACLINFO"></a><dl>
<dt><b>HttpServiceConfigUrlAclInfo</b></dt>
</dl>
</td>
<td width="60%">
Sets a URL reservation record.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigTimeout"></a><a id="httpserviceconfigtimeout"></a><a id="HTTPSERVICECONFIGTIMEOUT"></a><dl>
<dt><b>HttpServiceConfigTimeout</b></dt>
</dl>
</td>
<td width="60%">
Sets a specified HTTP Server API wide connection time-out.


<b>Windows Vista and later:  </b>This enumeration value is supported.



</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigSslSniCertInfo"></a><a id="httpserviceconfigsslsnicertinfo"></a><a id="HTTPSERVICECONFIGSSLSNICERTINFO"></a><dl>
<dt><b>HttpServiceConfigSslSniCertInfo</b></dt>
</dl>
</td>
<td width="60%">
Sets a specified SSL Server Name Indication (SNI) certificate record.

<b>Windows 8 and later:  </b>This enumeration value is supported.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigSslCcsCertInfo"></a><a id="httpserviceconfigsslccscertinfo"></a><a id="HTTPSERVICECONFIGSSLCCSCERTINFO"></a><dl>
<dt><b>HttpServiceConfigSslCcsCertInfo</b></dt>
</dl>
</td>
<td width="60%">
Sets the   SSL certificate record that specifies that Http.sys should consult the Centralized Certificate Store (CCS) store to find certificates if the  port receives a Transport Layer Security (TLS) handshake. The port is specified by the <b>KeyDesc</b> member of the <a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_ccs_set">HTTP_SERVICE_CONFIG_SSL_CCS_SET</a> structure that you  pass to the <i>pConfigInformation</i> parameter.

<b>Windows 8 and later:  </b>This enumeration value is supported.

</td>
</tr>
</table>

### -param pConfigInformation [in]

A pointer to a buffer that contains the appropriate data to specify the type of record to be set.

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
<td width="40%"><a id="HttpServiceConfigTimeout"></a><a id="httpserviceconfigtimeout"></a><a id="HTTPSERVICECONFIGTIMEOUT"></a><dl>
<dt><b>HttpServiceConfigTimeout</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/http/ns-http-http_service_config_timeout_set">HTTP_SERVICE_CONFIG_TIMEOUT_SET</a> structure.


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

This parameter is reserved and must be  <b>NULL</b>.

## -returns

If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The specified record already exists, and must be deleted in order for its value to be re-set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer size specified in the <i>ConfigInformationLength</i> parameter is insufficient.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>ServiceHandle</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the supplied parameters is in an unusable form.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SUCH_LOGON_SESSION</b></dt>
</dl>
</td>
<td width="60%">
The SSL Certificate used is invalid.  This can occur only if the <i>HttpServiceConfigSSLCertInfo</i> parameter is used.

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

## -remarks

The configuration parameters set with <b>HttpSetServiceConfiguration</b> are applied to all the HTTP Server API applications on the machine, and persist when the HTTP Server API shuts down, or when the computer is restarted.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-1-0-functions">HTTP Server API Version 1.0 Functions</a>



<a href="/windows/desktop/api/http/nf-http-httpdeleteserviceconfiguration">HttpDeleteServiceConfiguration</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HttpQueryServiceConfiguration</a>



<a href="/windows/desktop/api/http/nf-http-httpupdateserviceconfiguration">HttpUpdateServiceConfiguration</a>