---
UID: NF:http.HttpUpdateServiceConfiguration
title: HttpUpdateServiceConfiguration function (http.h)
description: Updates atomically a service configuration parameter that specifies a Transport Layer Security (TLS) certificate in a configuration record within the HTTP Server API configuration store.
helpviewer_keywords: ["HttpServiceConfigSSLCertInfo","HttpServiceConfigSslCcsCertInfo","HttpServiceConfigSslSniCertInfo","HttpUpdateServiceConfiguration","HttpUpdateServiceConfiguration function [HTTP]","http.httpupdateserviceconfiguration","http/HttpUpdateServiceConfiguration"]
old-location: http\httpupdateserviceconfiguration.htm
tech.root: http
ms.assetid: B2102444-1183-4133-A83F-A58587FB6B89
ms.date: 12/05/2018
ms.keywords: HttpServiceConfigSSLCertInfo, HttpServiceConfigSslCcsCertInfo, HttpServiceConfigSslSniCertInfo, HttpUpdateServiceConfiguration, HttpUpdateServiceConfiguration function [HTTP], http.httpupdateserviceconfiguration, http/HttpUpdateServiceConfiguration
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
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
 - HttpUpdateServiceConfiguration
 - http/HttpUpdateServiceConfiguration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - httpapi.dll
api_name:
 - HttpUpdateServiceConfiguration
---

# HttpUpdateServiceConfiguration function


## -description

Updates atomically a service configuration parameter that specifies a Transport Layer Security (TLS) certificate in a  configuration record within the HTTP Server API configuration store.

## -parameters

### -param Handle [in]

Reserved and must be  <b>NULL</b>.

### -param ConfigId [in]

The type of configuration record to update. This parameter can be one of the following values from the <a href="/windows/desktop/api/http/ne-http-http_service_config_id">HTTP_SERVICE_CONFIG_ID</a> enumeration.

<table>
<tr>
<th><i>ConfigId</i> value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigSSLCertInfo"></a><a id="httpserviceconfigsslcertinfo"></a><a id="HTTPSERVICECONFIGSSLCERTINFO"></a><dl>
<dt><b>HttpServiceConfigSSLCertInfo</b></dt>
</dl>
</td>
<td width="60%">
Updates a specified SSL certificate record.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigSslSniCertInfo"></a><a id="httpserviceconfigsslsnicertinfo"></a><a id="HTTPSERVICECONFIGSSLSNICERTINFO"></a><dl>
<dt><b>HttpServiceConfigSslSniCertInfo</b></dt>
</dl>
</td>
<td width="60%">
Updates a specified SSL Server Name Indication (SNI) certificate record.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigSslCcsCertInfo"></a><a id="httpserviceconfigsslccscertinfo"></a><a id="HTTPSERVICECONFIGSSLCCSCERTINFO"></a><dl>
<dt><b>HttpServiceConfigSslCcsCertInfo</b></dt>
</dl>
</td>
<td width="60%">
Updates the   SSL certificate record that specifies that Http.sys should consult the Centralized Certificate Store (CCS) store to find certificates if the port receives a TLS handshake. The port is specified by the <b>KeyDesc</b> member of the <a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_ccs_set">HTTP_SERVICE_CONFIG_SSL_CCS_SET</a> structure that you  pass to the <i>pConfigInfo</i> parameter.

</td>
</tr>
</table>

### -param ConfigInfo [in]

A pointer to a buffer that contains the appropriate data to specify the type of record to update. The  following table shows the type of data the buffer contains for the different possible values of the <i>ConfigId</i> parameter.

<table>
<tr>
<th><i>ConfigId</i> value</th>
<th>Type of data in the <i>pConfigInfo</i> buffer</th>
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
<td width="40%"><a id="HttpServiceConfigSslSniCertInfo"></a><a id="httpserviceconfigsslsnicertinfo"></a><a id="HTTPSERVICECONFIGSSLSNICERTINFO"></a><dl>
<dt><b>HttpServiceConfigSslSniCertInfo</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_sni_set">HTTP_SERVICE_CONFIG_SSL_SNI_SET</a> structure. The hostname will be "*" when the SSL central certificate store is queried and wildcard bindings are used, and a host name for regular SNI.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigSslCcsCertInfo"></a><a id="httpserviceconfigsslccscertinfo"></a><a id="HTTPSERVICECONFIGSSLCCSCERTINFO"></a><dl>
<dt><b>HttpServiceConfigSslCcsCertInfo</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_ccs_set">HTTP_SERVICE_CONFIG_SSL_CCS_SET</a> structure. This structure is used to add the CCS store on the specified port, as well as to delete, retrieve, or update an existing SSL CCS record.

</td>
</tr>
</table>

### -param ConfigInfoLength [in]

The size, in bytes, of the <i>ConfigInfo</i> buffer.

### -param Overlapped [in]

Reserved and must be  <b>NULL</b>.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified record does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer size specified in the <i>ConfigInfoLength</i> parameter is insufficient.

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

The configuration parameters that you update with <b>HttpUpdateServiceConfiguration</b> are applied to all the HTTP Server API applications on the machine, and persist when the HTTP Server API shuts down, or when the computer is restarted.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-1-0-functions">HTTP Server API Version 1.0 Functions</a>



<a href="/windows/desktop/api/http/ne-http-http_service_config_id">HTTP_SERVICE_CONFIG_ID</a>



<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_ccs_set">HTTP_SERVICE_CONFIG_SSL_CCS_SET</a>



<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_set">HTTP_SERVICE_CONFIG_SSL_SET</a>



<a href="/windows/desktop/api/http/ns-http-http_service_config_ssl_sni_set">HTTP_SERVICE_CONFIG_SSL_SNI_SET</a>



<a href="/windows/desktop/api/http/nf-http-httpdeleteserviceconfiguration">HttpDeleteServiceConfiguration</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryserviceconfiguration">HttpQueryServiceConfiguration</a>



<a href="/windows/desktop/api/http/nf-http-httpsetserviceconfiguration">HttpSetServiceConfiguration</a>