---
UID: NF:http.HttpDeleteServiceConfiguration
title: HttpDeleteServiceConfiguration function
author: windows-sdk-content
description: Deletes specified data, such as IP addresses or SSL Certificates, from the HTTP Server API configuration store, one record at a time.
old-location: http\httpdeleteserviceconfiguration.htm
tech.root: Http
ms.assetid: 0ae94936-4c6a-4c9f-adb8-5e3af75cf486
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: HttpDeleteServiceConfiguration, HttpDeleteServiceConfiguration function [HTTP], HttpServiceConfigIPListenList, HttpServiceConfigSSLCertInfo, HttpServiceConfigSslCcsCertInfo, HttpServiceConfigSslSniCertInfo, HttpServiceConfigTimeout, HttpServiceConfigTimeouts, HttpServiceConfigUrlAclInfo, _http_httpdeleteserviceconfiguration, http.httpdeleteserviceconfiguration, http/HttpDeleteServiceConfiguration
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Httpapi.dll
api_name:
 - HttpDeleteServiceConfiguration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
the <a href="https://msdn.microsoft.com/1b250408-4e3b-4cec-a31e-2c7f7ebad23b">HTTP_SERVICE_CONFIG_ID</a> enumeration.

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
Deletes the   SSL certificate record that specifies that Http.sys should consult the Centralized Certificate Store (CCS) store to find certificates if the port receives a Transport Layer Security (TLS) handshake.  The port is specified by the <b>KeyDesc</b> member of the <a href="https://msdn.microsoft.com/BA815FB7-4A9F-4917-89E7-3CD108E1CEE3">HTTP_SERVICE_CONFIG_SSL_CCS_SET</a> structure that you  pass to the <i>pConfigInformation</i> parameter.

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

<a href="https://msdn.microsoft.com/a45fd5e4-0ae4-47fc-bb50-931e0947a6bc">HTTP_SERVICE_CONFIG_IP_LISTEN_PARAM</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigSSLCertInfo"></a><a id="httpserviceconfigsslcertinfo"></a><a id="HTTPSERVICECONFIGSSLCERTINFO"></a><dl>
<dt><b>HttpServiceConfigSSLCertInfo</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/23adda0b-907d-4804-9c12-e549af4f18c4">HTTP_SERVICE_CONFIG_SSL_SET</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigUrlAclInfo"></a><a id="httpserviceconfigurlaclinfo"></a><a id="HTTPSERVICECONFIGURLACLINFO"></a><dl>
<dt><b>HttpServiceConfigUrlAclInfo</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/92fc3f65-0153-4075-a61b-48a63c8e0ffe">HTTP_SERVICE_CONFIG_URLACL_SET</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigTimeouts"></a><a id="httpserviceconfigtimeouts"></a><a id="HTTPSERVICECONFIGTIMEOUTS"></a><dl>
<dt><b>HttpServiceConfigTimeouts</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/e591a6b8-e63f-40c3-bd48-e14cb9f89453">HTTP_SERVICE_CONFIG_TIMEOUT_KEY</a> structure.


<b>Windows Vista and later:  </b>This structure is supported.



</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigSslSniCertInfo"></a><a id="httpserviceconfigsslsnicertinfo"></a><a id="HTTPSERVICECONFIGSSLSNICERTINFO"></a><dl>
<dt><b>HttpServiceConfigSslSniCertInfo</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/382838B9-C15E-459F-AC40-ECA15EFC18B8">HTTP_SERVICE_CONFIG_SSL_SNI_SET</a> structure. The hostname will be "*" when the SSL central certificate store is queried and wildcard bindings are used, and a host name for regular SNI.


<b>Windows 8 and later:  </b>This structure is supported.



</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigSslCcsCertInfo"></a><a id="httpserviceconfigsslccscertinfo"></a><a id="HTTPSERVICECONFIGSSLCCSCERTINFO"></a><dl>
<dt><b><b>HttpServiceConfigSslCcsCertInfo</b></b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/BA815FB7-4A9F-4917-89E7-3CD108E1CEE3">HTTP_SERVICE_CONFIG_SSL_CCS_SET</a> structure.


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
A <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> defined in WinError.h.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1da9907d-a09d-41e1-aca1-9a8e2b91296f">HTTP Server API Version 1.0 Functions</a>



<a href="https://msdn.microsoft.com/bbd2c3c4-d2d0-4590-9b5c-6916b91600cd">HttpQueryServiceConfiguration</a>



<a href="https://msdn.microsoft.com/b0a6d442-2ff4-4e00-8301-696fb0864d8c">HttpSetServiceConfiguration</a>



<a href="https://msdn.microsoft.com/B2102444-1183-4133-A83F-A58587FB6B89">HttpUpdateServiceConfiguration</a>
 

 

