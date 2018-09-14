---
UID: NF:http.HttpQueryServiceConfiguration
title: HttpQueryServiceConfiguration function
author: windows-sdk-content
description: Retrieves one or more HTTP Server API configuration records.
old-location: http\httpqueryserviceconfiguration.htm
tech.root: Http
ms.assetid: bbd2c3c4-d2d0-4590-9b5c-6916b91600cd
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: HttpQueryServiceConfiguration, HttpQueryServiceConfiguration function [HTTP], HttpServiceConfigIPListenList, HttpServiceConfigSSLCertInfo, HttpServiceConfigSslCcsCertInfo, HttpServiceConfigSslSniCertInfo, HttpServiceConfigTimeout, HttpServiceConfigUrlAclInfo, _http_httpqueryserviceconfiguration, http.httpqueryserviceconfiguration, http/HttpQueryServiceConfiguration
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
 - HttpQueryServiceConfiguration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# HttpQueryServiceConfiguration function


## -description


The 
<b>HttpQueryServiceConfiguration</b> function retrieves one or more HTTP Server API configuration records.


## -parameters




### -param ServiceHandle [in]

Reserved. Must be zero.


### -param ConfigId [in]

The configuration record query type. This  parameter is one of the following values from the  
<a href="https://msdn.microsoft.com/1b250408-4e3b-4cec-a31e-2c7f7ebad23b">HTTP_SERVICE_CONFIG_ID</a> enumeration.

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
Queries the IP Listen List.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigSSLCertInfo"></a><a id="httpserviceconfigsslcertinfo"></a><a id="HTTPSERVICECONFIGSSLCERTINFO"></a><dl>
<dt><b>HttpServiceConfigSSLCertInfo</b></dt>
</dl>
</td>
<td width="60%">
Queries the SSL store for a specific certificate record.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigUrlAclInfo"></a><a id="httpserviceconfigurlaclinfo"></a><a id="HTTPSERVICECONFIGURLACLINFO"></a><dl>
<dt><b>HttpServiceConfigUrlAclInfo</b></dt>
</dl>
</td>
<td width="60%">
Queries URL reservation information.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigTimeout"></a><a id="httpserviceconfigtimeout"></a><a id="HTTPSERVICECONFIGTIMEOUT"></a><dl>
<dt><b>HttpServiceConfigTimeout</b></dt>
</dl>
</td>
<td width="60%">
Queries HTTP Server API wide connection timeouts.


<b>Windows Vista and later:  </b>This enumeration is supported.



</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigSslSniCertInfo"></a><a id="httpserviceconfigsslsnicertinfo"></a><a id="HTTPSERVICECONFIGSSLSNICERTINFO"></a><dl>
<dt><b>HttpServiceConfigSslSniCertInfo</b></dt>
</dl>
</td>
<td width="60%">
Queries  the SSL Server Name Indication (SNI) store for a specific certificate record.

<b>Windows 8 and later:  </b>This enumeration value is supported.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigSslCcsCertInfo"></a><a id="httpserviceconfigsslccscertinfo"></a><a id="HTTPSERVICECONFIGSSLCCSCERTINFO"></a><dl>
<dt><b>HttpServiceConfigSslCcsCertInfo</b></dt>
</dl>
</td>
<td width="60%">
Queries  the SSL configuration for an SSL Centralized Certificate Store (CCS) record on the port. The port is specified by the <b>KeyDesc</b> member of the <a href="https://msdn.microsoft.com/E7578D74-E8BE-472D-A01B-51BBA511F561">HTTP_SERVICE_CONFIG_SSL_CCS_QUERY</a> structure that you  pass to the <i>pInputConfigInfo</i> parameter.

<b>Windows 8 and later:  </b>This enumeration value is supported.

</td>
</tr>
</table>
 


### -param pInput [in, optional]

A pointer to a structure whose contents further define the query and of the type that correlates with <i>ConfigId</i> in the following table.

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
No input data; set to <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigSSLCertInfo"></a><a id="httpserviceconfigsslcertinfo"></a><a id="HTTPSERVICECONFIGSSLCERTINFO"></a><dl>
<dt><b>HttpServiceConfigSSLCertInfo</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/733b451a-d35b-4b83-ba49-0529309cd99b">HTTP_SERVICE_CONFIG_SSL_QUERY</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigUrlAclInfo"></a><a id="httpserviceconfigurlaclinfo"></a><a id="HTTPSERVICECONFIGURLACLINFO"></a><dl>
<dt><b>HttpServiceConfigUrlAclInfo</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/298edd6c-c036-4e45-88f3-84917c8a76ea">HTTP_SERVICE_CONFIG_URLACL_QUERY</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigTimeout"></a><a id="httpserviceconfigtimeout"></a><a id="HTTPSERVICECONFIGTIMEOUT"></a><dl>
<dt><b>HttpServiceConfigTimeout</b></dt>
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

<a href="https://msdn.microsoft.com/9C45B1B1-5572-4153-BBA4-0E8A52F650CA">HTTP_SERVICE_CONFIG_SSL_SNI_QUERY</a> structure.


<b>Windows 8 and later:  </b>This structure is supported.



</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigSslCcsCertInfo"></a><a id="httpserviceconfigsslccscertinfo"></a><a id="HTTPSERVICECONFIGSSLCCSCERTINFO"></a><dl>
<dt><b>HttpServiceConfigSslCcsCertInfo</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/E7578D74-E8BE-472D-A01B-51BBA511F561">HTTP_SERVICE_CONFIG_SSL_CCS_QUERY</a> structure.


<b>Windows 8 and later:  </b>This structure is supported.



</td>
</tr>
</table>
 

For more information, see the appropriate query structures.


### -param InputLength [in, optional]

Size, in bytes, of the <i>pInputConfigInfo</i> buffer.


### -param pOutput [in, out, optional]

A pointer to a buffer in which the query results are returned. The type of this buffer correlates with <i>ConfigId</i>.

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

<a href="https://msdn.microsoft.com/8cecb295-a35b-466d-9420-3b72f77f731f">HTTP_SERVICE_CONFIG_IP_LISTEN_QUERY</a> structure.

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
<td width="40%"><a id="HttpServiceConfigTimeout"></a><a id="httpserviceconfigtimeout"></a><a id="HTTPSERVICECONFIGTIMEOUT"></a><dl>
<dt><b>HttpServiceConfigTimeout</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/13a0cac9-9e75-4350-a523-5ad9a57caad7">HTTP_SERVICE_CONFIG_TIMEOUT_PARAM</a> data type.


<b>Windows Vista and later:  </b>This structure is supported.



</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigSslSniCertInfo"></a><a id="httpserviceconfigsslsnicertinfo"></a><a id="HTTPSERVICECONFIGSSLSNICERTINFO"></a><dl>
<dt><b>HttpServiceConfigSslSniCertInfo</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/382838B9-C15E-459F-AC40-ECA15EFC18B8">HTTP_SERVICE_CONFIG_SSL_SNI_SET</a> structure.


<b>Windows 8 and later:  </b>This structure is supported.



</td>
</tr>
<tr>
<td width="40%"><a id="HttpServiceConfigSslCcsCertInfo"></a><a id="httpserviceconfigsslccscertinfo"></a><a id="HTTPSERVICECONFIGSSLCCSCERTINFO"></a><dl>
<dt><b>HttpServiceConfigSslCcsCertInfo</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/BA815FB7-4A9F-4917-89E7-3CD108E1CEE3">HTTP_SERVICE_CONFIG_SSL_CCS_SET</a> structure.


<b>Windows 8 and later:  </b>This structure is supported.



</td>
</tr>
</table>
 


### -param OutputLength [in, optional]

Size, in bytes, of the <i>pOutputConfigInfo</i> buffer.


### -param pReturnLength [out, optional]

A pointer to a variable that receives the number of bytes to be written in the output buffer. If the output buffer is too small, the call fails with a return value of <b>ERROR_INSUFFICIENT_BUFFER</b>. The value pointed to by <i>pReturnLength</i> can be used to determine the minimum length the buffer requires for the call to succeed.


### -param pOverlapped [in]

Reserved for asynchronous operation and must be set to <b>NULL</b>.


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
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by <i>pOutputConfigInfo</i> is too small to receive the output data. Call the function again with a buffer at least as large as the size pointed to by <i>pReturnLength</i> on exit.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
This error code is only returned when <i>ConfigId</i> is set to <b>HttpServiceConfigTimeout</b>. The buffer pointed to by <i>pOutputConfigInfo</i> is too small to receive the output data. Call the function again with a buffer at least as large as the size pointed to by <i>pReturnLength</i> on exit.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no more items to return that meet the specified criteria.

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



<a href="https://msdn.microsoft.com/0ae94936-4c6a-4c9f-adb8-5e3af75cf486">HttpDeleteServiceConfiguration</a>



<a href="https://msdn.microsoft.com/b0a6d442-2ff4-4e00-8301-696fb0864d8c">HttpSetServiceConfiguration</a>



<a href="https://msdn.microsoft.com/B2102444-1183-4133-A83F-A58587FB6B89">HttpUpdateServiceConfiguration</a>
 

 

