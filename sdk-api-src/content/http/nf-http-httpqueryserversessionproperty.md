---
UID: NF:http.HttpQueryServerSessionProperty
title: HttpQueryServerSessionProperty function (http.h)
description: Queries a server property on the specified server session.
helpviewer_keywords: ["HttpQueryServerSessionProperty","HttpQueryServerSessionProperty function [HTTP]","HttpServerAuthenticationProperty","HttpServerChannelBindProperty","HttpServerQosProperty","HttpServerStateProperty","HttpServerTimeoutsProperty","http.httpqueryserversessionproperty","http/HttpQueryServerSessionProperty"]
old-location: http\httpqueryserversessionproperty.htm
tech.root: http
ms.assetid: 653b286b-dc86-4896-8f03-1628b7178680
ms.date: 12/05/2018
ms.keywords: HttpQueryServerSessionProperty, HttpQueryServerSessionProperty function [HTTP], HttpServerAuthenticationProperty, HttpServerChannelBindProperty, HttpServerQosProperty, HttpServerStateProperty, HttpServerTimeoutsProperty, http.httpqueryserversessionproperty, http/HttpQueryServerSessionProperty
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
req.lib: Httpapi.lib
req.dll: Httpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HttpQueryServerSessionProperty
 - http/HttpQueryServerSessionProperty
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
 - HttpQueryServerSessionProperty
---

# HttpQueryServerSessionProperty function


## -description

The <b>HttpQueryServerSessionProperty</b> function queries a  server property on the specified server session.

## -parameters

### -param ServerSessionId [in]

The server session for which the property setting is returned.

### -param Property [in]

A member of the  <a href="/windows/desktop/api/http/ne-http-http_server_property">HTTP_SERVER_PROPERTY</a> enumeration that describes the property type that is queried. This can be one of the following.

<table>
<tr>
<th>Property</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HttpServerStateProperty"></a><a id="httpserverstateproperty"></a><a id="HTTPSERVERSTATEPROPERTY"></a><dl>
<dt><b>HttpServerStateProperty</b></dt>
</dl>
</td>
<td width="60%">
Queries the current state of the server session.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServerTimeoutsProperty"></a><a id="httpservertimeoutsproperty"></a><a id="HTTPSERVERTIMEOUTSPROPERTY"></a><dl>
<dt><b>HttpServerTimeoutsProperty</b></dt>
</dl>
</td>
<td width="60%">
Queries the server session connection timeout limits.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServerQosProperty"></a><a id="httpserverqosproperty"></a><a id="HTTPSERVERQOSPROPERTY"></a><dl>
<dt><b>HttpServerQosProperty</b></dt>
</dl>
</td>
<td width="60%">
Queries the bandwidth throttling for the server session. By default, the HTTP Server API does not limit bandwidth. 

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServerAuthenticationProperty"></a><a id="httpserverauthenticationproperty"></a><a id="HTTPSERVERAUTHENTICATIONPROPERTY"></a><dl>
<dt><b>HttpServerAuthenticationProperty</b></dt>
</dl>
</td>
<td width="60%">
Queries kernel mode server-side authentication for the Basic, NTLM, Negotiate, and Digest authentication schemes.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServerChannelBindProperty"></a><a id="httpserverchannelbindproperty"></a><a id="HTTPSERVERCHANNELBINDPROPERTY"></a><dl>
<dt><b>HttpServerChannelBindProperty</b></dt>
</dl>
</td>
<td width="60%">
Queries the channel binding token (CBT) properties.

</td>
</tr>
</table>

### -param PropertyInformation [out]

A pointer to the buffer that receives the property data.

<i>pPropertyInformation</i> points to one of the following property data structures based on the property that is set.<table>
<tr>
<th>Property</th>
<th>Structure</th>
</tr>
<tr>
<td>HttpServerStateProperty</td>
<td>
<a href="/windows/desktop/api/http/ns-http-http_state_info">HTTP_STATE_INFO</a>
</td>
</tr>
<tr>
<td>HttpServerQosProperty</td>
<td>
<a href="/windows/desktop/api/http/ns-http-http_qos_setting_info">HTTP_QOS_SETTING_INFO</a>
</td>
</tr>
<tr>
<td>HttpServerTimeoutsProperty</td>
<td>
<a href="/windows/desktop/api/http/ns-http-http_timeout_limit_info">HTTP_TIMEOUT_LIMIT_INFO</a>
</td>
</tr>
<tr>
<td>HttpServerAuthenticationProperty</td>
<td>
<a href="/windows/desktop/api/http/ns-http-http_server_authentication_info">HTTP_SERVER_AUTHENTICATION_INFO</a>
</td>
</tr>
<tr>
<td>HttpServerChannelBindProperty</td>
<td>
<a href="/windows/desktop/api/http/ns-http-http_channel_bind_info">HTTP_CHANNEL_BIND_INFO</a>
</td>
</tr>
</table>

### -param PropertyInformationLength [in]

The length, in bytes, of the buffer pointed to by the <i>pPropertyInformation</i> parameter.

### -param ReturnLength [out, optional]

The number, in  bytes, returned in the  <i>pPropertyInformation</i> buffer.

If the output buffer is too small, the call fails with a return value of <b>ERROR_MORE_DATA</b>. The value pointed to by <i>pReturnLength</i> can be used to determine the minimum length of the buffer required for the call to succeed.

## -returns

If the function succeeds, it returns <b>NO_ERROR</b>

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
The property type specified in the <i>Property</i> parameter is not supported for server sessions.

The <i>ServerSessionId</i> parameter does not contain a valid server session.

The <i>pPropertyInformation</i> parameter is <b>NULL</b>.

The  <i>PropertyInformationLength</i> parameter is zero.

The application does not have permission to query the server session properties. Only the application that created the server session can query the properties.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The size, in bytes, of the buffer pointed to by the  <i>pPropertyInformation</i> parameter is too small to receive the property data. On exit call the function again with a buffer at least as large as the size pointed to by <i>pReturnLength</i> on exit.

</td>
</tr>
</table>

## -remarks

Querying the <b>HttpServerLoggingProperty</b> is not supported.

The <i>pPropertyInformation</i> parameter points to the configuration structure for the property type that is queried. The <i>PropertyInformationLength</i> parameter specifies the size, in bytes,  of the configuration structure. For example, when querying the <b>HttpServerTimeoutsProperty</b> the <i>pPropertyInformation</i> parameter must point to a buffer that is at least the size of the <a href="/windows/desktop/api/http/ns-http-http_timeout_limit_info">HTTP_TIMEOUT_LIMIT_INFO</a> structure.

 To specify the HttpServerQosProperty property in the <i>pPropertyInformation</i> parameter, set    <b>QosType</b> to <b>HttpQosSettingTypeBandwidth</b> inside the <a href="/windows/desktop/api/http/ns-http-http_qos_setting_info">HTTP_QOS_SETTING_INFO</a> structure, and pass a pointer to this structure in the parameter.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-functions">HTTP Server API Version 2.0 Functions</a>



<a href="/windows/desktop/api/http/nf-http-httpcloseserversession">HttpCloseServerSession</a>



<a href="/windows/desktop/api/http/nf-http-httpcreateserversession">HttpCreateServerSession</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryserversessionproperty">HttpQueryServerSessionProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpsetserversessionproperty">HttpSetServerSessionProperty</a>