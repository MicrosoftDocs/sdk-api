---
UID: NF:http.HttpSetUrlGroupProperty
title: HttpSetUrlGroupProperty function (http.h)
description: Sets a new property or modifies an existing property on the specified URL Group.
helpviewer_keywords: ["HttpServerAuthenticationProperty","HttpServerBindingProperty","HttpServerChannelBindProperty","HttpServerExtendedAuthenticationProperty","HttpServerLoggingProperty","HttpServerQosProperty","HttpServerStateProperty","HttpServerTimeoutsProperty","HttpSetUrlGroupProperty","HttpSetUrlGroupProperty function [HTTP]","http.httpseturlgroupproperty","http/HttpSetUrlGroupProperty"]
old-location: http\httpseturlgroupproperty.htm
tech.root: http
ms.assetid: e0826a25-1c50-4757-9355-69eb4946e8dd
ms.date: 12/05/2018
ms.keywords: HttpServerAuthenticationProperty, HttpServerBindingProperty, HttpServerChannelBindProperty, HttpServerExtendedAuthenticationProperty, HttpServerLoggingProperty, HttpServerQosProperty, HttpServerStateProperty, HttpServerTimeoutsProperty, HttpSetUrlGroupProperty, HttpSetUrlGroupProperty function [HTTP], http.httpseturlgroupproperty, http/HttpSetUrlGroupProperty
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
 - HttpSetUrlGroupProperty
 - http/HttpSetUrlGroupProperty
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
 - HttpSetUrlGroupProperty
---

# HttpSetUrlGroupProperty function


## -description

The <b>HttpSetUrlGroupProperty</b> function sets a new property or modifies an existing property on the specified URL Group.

## -parameters

### -param UrlGroupId [in]

The ID of the URL Group for which the property is set.

### -param Property [in]

A member of the  <a href="/windows/desktop/api/http/ne-http-http_server_property">HTTP_SERVER_PROPERTY</a> enumeration that describes the property type that is modified or set. This can be one of the following:

<table>
<tr>
<th>Property</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HttpServerAuthenticationProperty"></a><a id="httpserverauthenticationproperty"></a><a id="HTTPSERVERAUTHENTICATIONPROPERTY"></a><dl>
<dt><b>HttpServerAuthenticationProperty</b></dt>
</dl>
</td>
<td width="60%">
Enables server-side authentication for the URL Group using the Basic, NTLM, Negotiate, and Digest authentication schemes.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServerExtendedAuthenticationProperty"></a><a id="httpserverextendedauthenticationproperty"></a><a id="HTTPSERVEREXTENDEDAUTHENTICATIONPROPERTY"></a><dl>
<dt><b>HttpServerExtendedAuthenticationProperty</b></dt>
</dl>
</td>
<td width="60%">
Enables server-side authentication for the URL Group using the Kerberos authentication scheme.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServerQosProperty"></a><a id="httpserverqosproperty"></a><a id="HTTPSERVERQOSPROPERTY"></a><dl>
<dt><b>HttpServerQosProperty</b></dt>
</dl>
</td>
<td width="60%">
This value maps to the generic <a href="/windows/desktop/api/http/ns-http-http_qos_setting_info">HTTP_QOS_SETTING_INFO</a> structure with <b>QosType</b> set to either <b>HttpQosSettingTypeBandwidth</b> or  <b>HttpQosSettingTypeConnectionLimit</b>. If <b>HttpQosSettingTypeBandwidth</b>, modifies or sets the bandwidth throttling for the URL Group. If <b>HttpQosSettingTypeConnectionLimit</b>, modifies or sets the maximum number of outstanding connections served for a URL Group at any time.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServerBindingProperty"></a><a id="httpserverbindingproperty"></a><a id="HTTPSERVERBINDINGPROPERTY"></a><dl>
<dt><b>HttpServerBindingProperty</b></dt>
</dl>
</td>
<td width="60%">
Modifies or sets the URL Group association with a request queue.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServerLoggingProperty"></a><a id="httpserverloggingproperty"></a><a id="HTTPSERVERLOGGINGPROPERTY"></a><dl>
<dt><b>HttpServerLoggingProperty</b></dt>
</dl>
</td>
<td width="60%">
Modifies or sets logging for the URL Group.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServerStateProperty"></a><a id="httpserverstateproperty"></a><a id="HTTPSERVERSTATEPROPERTY"></a><dl>
<dt><b>HttpServerStateProperty</b></dt>
</dl>
</td>
<td width="60%">
Modifies or sets the state of the URL Group. The state can be either enabled or disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServerTimeoutsProperty"></a><a id="httpservertimeoutsproperty"></a><a id="HTTPSERVERTIMEOUTSPROPERTY"></a><dl>
<dt><b>HttpServerTimeoutsProperty</b></dt>
</dl>
</td>
<td width="60%">
Modifies or sets the  connection timeout limits for the URL Group.

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

A pointer to the buffer that contains the property information.

<i>pPropertyInformation</i> points to one of the following property information structures based on the property that is set.<table>
<tr>
<th>Property</th>
<th>Structure</th>
</tr>
<tr>
<td>HttpServerAuthenticatonProperty</td>
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
<td>HttpServerQosProperty</td>
<td>
<a href="/windows/desktop/api/http/ns-http-http_qos_setting_info">HTTP_QOS_SETTING_INFO</a>
</td>
</tr>
<tr>
<td>HttpServerBindingProperty</td>
<td>
<a href="/windows/desktop/api/http/ns-http-http_binding_info">HTTP_BINDING_INFO</a>
</td>
</tr>
<tr>
<td>HttpServerLoggingProperty</td>
<td>
<a href="/windows/desktop/api/http/ns-http-http_logging_info">HTTP_LOGGING_INFO</a>
</td>
</tr>
<tr>
<td>HttpServerStateProperty</td>
<td>
<a href="/windows/desktop/api/http/ns-http-http_state_info">HTTP_STATE_INFO</a>
</td>
</tr>
<tr>
<td>HttpServerTimeoutsProperty</td>
<td>
<a href="/windows/desktop/api/http/ns-http-http_timeout_limit_info">HTTP_TIMEOUT_LIMIT_INFO</a>
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

If the function succeeds, it returns <b>NO_ERROR</b>.

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
The property type specified in the <i>Property</i> parameter is not supported for URL Groups.

The <i>pPropertyInformation</i> parameter is <b>NULL</b>.

The  <i>PropertyInformationLength</i> parameter is zero.

The <i>UrlGroupId</i> parameter does not contain a valid server session.

The application does not have permission to set the URL Group properties. Only the application that created the URL Group can set the properties.

</td>
</tr>
</table>

## -remarks

After the URL Group is created it must be associated with a request queue to receive requests. To associate the URL Group with a request queue, the application calls <b>HttpSetUrlGroupProperty</b> with the <b>HttpServerBindingProperty</b> property. If this property is not set, matching requests for the URL Group are not delivered to a request queue and the  HTTP Server API generates a 503 response.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-functions">HTTP Server API Version 2.0 Functions</a>



<a href="/windows/desktop/api/http/nf-http-httpaddurltourlgroup">HttpAddUrlToUrlGroup</a>



<a href="/windows/desktop/api/http/nf-http-httpcloseurlgroup">HttpCloseUrlGroup</a>



<a href="/windows/desktop/api/http/nf-http-httpcreateurlgroup">HttpCreateUrlGroup</a>



<a href="/windows/desktop/api/http/nf-http-httpqueryurlgroupproperty">HttpQueryUrlGroupProperty</a>



<a href="/windows/desktop/api/http/nf-http-httpremoveurlfromurlgroup">HttpRemoveUrlFromUrlGroup</a>