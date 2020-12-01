---
UID: NF:http.HttpQueryUrlGroupProperty
title: HttpQueryUrlGroupProperty function (http.h)
description: Queries a property on the specified URL Group.
helpviewer_keywords: ["HttpQueryUrlGroupProperty","HttpQueryUrlGroupProperty function [HTTP]","HttpServerAuthenticationProperty","HttpServerChannelBindProperty","HttpServerQosProperty","HttpServerStateProperty","HttpServerTimeoutsProperty","http.httpqueryurlgroupproperty","http/HttpQueryUrlGroupProperty"]
old-location: http\httpqueryurlgroupproperty.htm
tech.root: http
ms.assetid: f3e8fde0-5a78-46aa-8c6c-cea957d12356
ms.date: 12/05/2018
ms.keywords: HttpQueryUrlGroupProperty, HttpQueryUrlGroupProperty function [HTTP], HttpServerAuthenticationProperty, HttpServerChannelBindProperty, HttpServerQosProperty, HttpServerStateProperty, HttpServerTimeoutsProperty, http.httpqueryurlgroupproperty, http/HttpQueryUrlGroupProperty
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
 - HttpQueryUrlGroupProperty
 - http/HttpQueryUrlGroupProperty
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
 - HttpQueryUrlGroupProperty
---

# HttpQueryUrlGroupProperty function


## -description

The <b>HttpQueryUrlGroupProperty</b> function queries a property on the specified URL Group.

## -parameters

### -param UrlGroupId [in]

The ID of the URL Group for which the property setting is returned.

### -param Property [in]

A member of the  <a href="/windows/desktop/api/http/ne-http-http_server_property">HTTP_SERVER_PROPERTY</a> enumeration that describes the property type that is queried. This can be one of the following:

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
Queries the enabled server-side authentication schemes.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServerTimeoutsProperty"></a><a id="httpservertimeoutsproperty"></a><a id="HTTPSERVERTIMEOUTSPROPERTY"></a><dl>
<dt><b>HttpServerTimeoutsProperty</b></dt>
</dl>
</td>
<td width="60%">
Queries the URL Group connection timeout limits.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServerStateProperty"></a><a id="httpserverstateproperty"></a><a id="HTTPSERVERSTATEPROPERTY"></a><dl>
<dt><b>HttpServerStateProperty</b></dt>
</dl>
</td>
<td width="60%">
Queries the current state of the URL Group. The state can be either enabled or disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="HttpServerQosProperty"></a><a id="httpserverqosproperty"></a><a id="HTTPSERVERQOSPROPERTY"></a><dl>
<dt><b>HttpServerQosProperty</b></dt>
</dl>
</td>
<td width="60%">
This value maps to the generic <a href="/windows/desktop/api/http/ns-http-http_qos_setting_info">HTTP_QOS_SETTING_INFO</a> structure with <b>QosType</b> set to either <b>HttpQosSettingTypeBandwidth</b> or  <b>HttpQosSettingTypeConnectionLimit</b>. If <b>HttpQosSettingTypeBandwidth</b>, queries the bandwidth throttling for the URL Group. If <b>HttpQosSettingTypeConnectionLimit</b>, queries the maximum number of outstanding connections served for a URL group at any time.

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

A pointer to the buffer that receives the property information.

<i>pPropertyInformation</i> points to one of the following property information structures based on the property that is queried.<table>
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
<td>HttpServerAuthenticationProperty</td>
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

### -param ReturnLength [out, optional]

The size, in bytes, returned in the  <i>pPropertyInformation</i> buffer.

If the output buffer is too small, the call fails with a return value of <b>ERROR_MORE_DATA</b>. The value pointed to by <i>pReturnLength</i> can be used to determine the minimum length of the buffer required for the call to succeed.

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

The <i>UrlGroupId</i> parameter does not identify a valid server URL Group.

The <i>pPropertyInformation</i> parameter is <b>NULL</b>.

The  <i>PropertyInformationLength</i> parameter is zero.

The application does not have permission to query the URL Group properties. Only the application that created the URL Group can query the properties.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The size, in bytes, of the buffer pointed to by the  <i>pPropertyInformation</i> parameter is too small to receive the property information. Call the function again with a buffer at least as large as the size pointed to by <i>pReturnLength</i> on exit.

</td>
</tr>
</table>

## -remarks

Querying the <b>HttpServerLoggingProperty</b> is not supported.

## -see-also

<a href="/windows/desktop/Http/http-server-api-version-2-0-functions">HTTP Server API Version 2.0 Functions</a>



<a href="/windows/desktop/api/http/nf-http-httpaddurltourlgroup">HttpAddUrlToUrlGroup</a>



<a href="/windows/desktop/api/http/nf-http-httpcloseurlgroup">HttpCloseUrlGroup</a>



<a href="/windows/desktop/api/http/nf-http-httpcreateurlgroup">HttpCreateUrlGroup</a>



<a href="/windows/desktop/api/http/nf-http-httpremoveurlfromurlgroup">HttpRemoveUrlFromUrlGroup</a>



<a href="/windows/desktop/api/http/nf-http-httpseturlgroupproperty">HttpSetUrlGroupProperty</a>