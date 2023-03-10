---
UID: NF:http.HttpSetServerSessionProperty
title: HttpSetServerSessionProperty function (http.h)
description: Sets a new server session property or modifies an existing property on the specified server session.
helpviewer_keywords: ["HttpServerAuthenticationProperty","HttpServerChannelBindProperty","HttpServerExtendedAuthenticationProperty","HttpServerLoggingProperty","HttpServerQosProperty","HttpServerStateProperty","HttpServerTimeoutsProperty","HttpSetServerSessionProperty","HttpSetServerSessionProperty function [HTTP]","http.httpsetserversessionproperty","http/HttpSetServerSessionProperty"]
old-location: http\httpsetserversessionproperty.htm
tech.root: http
ms.assetid: d655832c-68a1-42d1-ac91-964884bf2dac
ms.date: 12/05/2018
ms.keywords: HttpServerAuthenticationProperty, HttpServerChannelBindProperty, HttpServerExtendedAuthenticationProperty, HttpServerLoggingProperty, HttpServerQosProperty, HttpServerStateProperty, HttpServerTimeoutsProperty, HttpSetServerSessionProperty, HttpSetServerSessionProperty function [HTTP], http.httpsetserversessionproperty, http/HttpSetServerSessionProperty
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
 - HttpSetServerSessionProperty
 - http/HttpSetServerSessionProperty
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
 - HttpSetServerSessionProperty
---

# HttpSetServerSessionProperty function


## -description

The <b>HttpSetServerSessionProperty</b> function sets a new server session property or modifies an existing property on the specified server session.

## -parameters

### -param ServerSessionId [in]

The server session for which the property is set.

### -param Property [in]

A member of the  <a href="/windows/desktop/api/http/ne-http-http_server_property">HTTP_SERVER_PROPERTY</a> enumeration that describes the property type that is set. This can be one of the following.

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
Modifies or sets the state of the server session. The state can be either enabled or disabled; the default state is enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServerTimeoutsProperty"></a><a id="httpservertimeoutsproperty"></a><a id="HTTPSERVERTIMEOUTSPROPERTY"></a><dl>
<dt><b>HttpServerTimeoutsProperty</b></dt>
</dl>
</td>
<td width="60%">
Modifies or sets the server session connection timeout limits.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServerQosProperty"></a><a id="httpserverqosproperty"></a><a id="HTTPSERVERQOSPROPERTY"></a><dl>
<dt><b>HttpServerQosProperty</b></dt>
</dl>
</td>
<td width="60%">
Modifies or sets the bandwidth throttling for the server session. By default, the HTTP Server API does not limit bandwidth. 

<div class="alert"><b>Note</b>  This value maps to the generic <a href="/windows/desktop/api/http/ns-http-http_qos_setting_info">HTTP_QOS_SETTING_INFO</a> structure with <b>QosType</b> set to <b>HttpQosSettingTypeBandwidth</b>. </div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="HttpServerLoggingProperty"></a><a id="httpserverloggingproperty"></a><a id="HTTPSERVERLOGGINGPROPERTY"></a><dl>
<dt><b>HttpServerLoggingProperty</b></dt>
</dl>
</td>
<td width="60%">
Enables or disables logging for the server session. This property sets only centralized W3C and centralized binary logging.  By default, logging is not enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServerAuthenticationProperty"></a><a id="httpserverauthenticationproperty"></a><a id="HTTPSERVERAUTHENTICATIONPROPERTY"></a><dl>
<dt><b>HttpServerAuthenticationProperty</b></dt>
</dl>
</td>
<td width="60%">
Enables kernel mode server side authentication for the Basic, NTLM, Negotiate, and Digest authentication schemes.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServerExtendedAuthenticationProperty"></a><a id="httpserverextendedauthenticationproperty"></a><a id="HTTPSERVEREXTENDEDAUTHENTICATIONPROPERTY"></a><dl>
<dt><b>HttpServerExtendedAuthenticationProperty</b></dt>
</dl>
</td>
<td width="60%">
Enables kernel mode server side authentication for the Kerberos authentication scheme.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServerChannelBindProperty_"></a><a id="httpserverchannelbindproperty_"></a><a id="HTTPSERVERCHANNELBINDPROPERTY_"></a><dl>
<dt><b>HttpServerChannelBindProperty </b></dt>
</dl>
</td>
<td width="60%">
Enables server side authentication that uses a channel binding token (CBT).

</td>
</tr>
</table>

### -param PropertyInformation [in]

A pointer to the buffer that contains the property data.

<i>pPropertyInformation</i> points to a property data structure, listed in the following table, based on the property that is set.<table>
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
<td>HttpServerLoggingProperty</td>
<td>
<a href="/windows/desktop/api/http/ns-http-http_logging_info">HTTP_LOGGING_INFO</a>
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
<td>HttpServerExtendedAuthenticationProperty</td>
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

The <i>pPropertyInformation</i> parameter is <b>NULL</b>.

The  <i>PropertyInformationLength</i> parameter is zero.

The <i>ServerSessionId</i> parameter does not contain a valid server session.

The application does not have permission to set the server session properties. Only the application that created the server session can set the properties.

</td>
</tr>
</table>

## -remarks

Server sessions are top level configuration containers for configuration data that applies to all of the URL groups created under them. The server session is created with <a href="/windows/desktop/api/http/nf-http-httpcreateserversession">HttpCreateServerSession</a>.

The <i>pPropertyInformation</i> parameter points to the configuration structure for the property type that is set. The <i>PropertyInformationLength</i> parameter specifies the size, in bytes, of the configuration structure. For example, when setting the <b>HttpServerTimeoutsProperty</b> the <i>pPropertyInformation</i> parameter must point to a buffer that is at least equal to the size of the <a href="/windows/desktop/api/http/ns-http-http_timeout_limit_info">HTTP_TIMEOUT_LIMIT_INFO</a> structure.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-functions">HTTP Server API Version 2.0 Functions</a>



<a href="/windows/desktop/api/http/nf-http-httpcloseserversession">HttpCloseServerSession</a>



<a href="/windows/desktop/api/http/nf-http-httpcreateserversession">HttpCreateServerSession</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryserversessionproperty">HttpQueryServerSessionProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpsetserversessionproperty">HttpSetServerSessionProperty</a>