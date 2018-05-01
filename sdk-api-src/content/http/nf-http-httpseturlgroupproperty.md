---
UID: NF:http.HttpSetUrlGroupProperty
title: HttpSetUrlGroupProperty function
author: windows-driver-content
description: Sets a new property or modifies an existing property on the specified URL Group.
old-location: http\httpseturlgroupproperty.htm
old-project: Http
ms.assetid: e0826a25-1c50-4757-9355-69eb4946e8dd
ms.author: windowsdriverdev
ms.date: 4/12/2018
ms.keywords: HttpServerAuthenticationProperty, HttpServerBindingProperty, HttpServerChannelBindProperty, HttpServerExtendedAuthenticationProperty, HttpServerLoggingProperty, HttpServerQosProperty, HttpServerStateProperty, HttpServerTimeoutsProperty, HttpSetUrlGroupProperty, HttpSetUrlGroupProperty function [HTTP], http.httpseturlgroupproperty, http/HttpSetUrlGroupProperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: HTTP_VERB, *PHTTP_VERB
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Httpapi.dll
api_name:
-	HttpSetUrlGroupProperty
product: Windows
targetos: Windows
req.lib: Httpapi.lib
req.dll: Httpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# HttpSetUrlGroupProperty function


## -description


The <b>HttpSetUrlGroupProperty</b> function sets a new property or modifies an existing property on the specified URL Group.


## -parameters




### -param UrlGroupId [in]

The ID of the URL Group for which the property is set.


### -param Property [in]

A member of the  <a href="https://msdn.microsoft.com/14865796-135c-43c2-955a-fdeae05a8278">HTTP_SERVER_PROPERTY</a> enumeration that describes the property type that is modified or set. This can be one of the following:

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
This value maps to the generic <a href="https://msdn.microsoft.com/6c220063-02d0-44c0-b3a3-e7bfd5c57e1f">HTTP_QOS_SETTING_INFO</a> structure with <b>QosType</b> set to either <b>HttpQosSettingTypeBandwidth</b> or  <b>HttpQosSettingTypeConnectionLimit</b>. If <b>HttpQosSettingTypeBandwidth</b>, modifies or sets the bandwidth throttling for the URL Group. If <b>HttpQosSettingTypeConnectionLimit</b>, modifies or sets the maximum number of outstanding connections served for a URL Group at any time.

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
 


### -param PropertyInformation

TBD


### -param PropertyInformationLength [in]

The length, in bytes, of the buffer pointed to by the <i>pPropertyInformation</i> parameter.


#### - pPropertyInformation [in]

A pointer to the buffer that contains the property information.

<i>pPropertyInformation</i> points to one of the following property information structures based on the property that is set.<table>
<tr>
<th>Property</th>
<th>Structure</th>
</tr>
<tr>
<td>HttpServerAuthenticatonProperty</td>
<td>
<a href="https://msdn.microsoft.com/4f408115-c073-4e9f-b316-8ad3f03acf53">HTTP_SERVER_AUTHENTICATION_INFO</a>
</td>
</tr>
<tr>
<td>HttpServerExtendedAuthenticationProperty</td>
<td>
<a href="https://msdn.microsoft.com/4f408115-c073-4e9f-b316-8ad3f03acf53">HTTP_SERVER_AUTHENTICATION_INFO</a>
</td>
</tr>
<tr>
<td>HttpServerQosProperty</td>
<td>
<a href="https://msdn.microsoft.com/6c220063-02d0-44c0-b3a3-e7bfd5c57e1f">HTTP_QOS_SETTING_INFO</a>
</td>
</tr>
<tr>
<td>HttpServerBindingProperty</td>
<td>
<a href="https://msdn.microsoft.com/551a928a-84c6-479b-a500-de69dc8857cd">HTTP_BINDING_INFO</a>
</td>
</tr>
<tr>
<td>HttpServerLoggingProperty</td>
<td>
<a href="https://msdn.microsoft.com/12e12f83-c36a-4b4e-8890-50566cf00c2b">HTTP_LOGGING_INFO</a>
</td>
</tr>
<tr>
<td>HttpServerStateProperty</td>
<td>
<a href="https://msdn.microsoft.com/736ae89b-a4fb-4962-ae68-9aaccd869c88">HTTP_STATE_INFO</a>
</td>
</tr>
<tr>
<td>HttpServerTimeoutsProperty</td>
<td>
<a href="https://msdn.microsoft.com/900f4b4d-c34d-4994-b8eb-b3f15e54f29a">HTTP_TIMEOUT_LIMIT_INFO</a>
</td>
</tr>
<tr>
<td>HttpServerChannelBindProperty</td>
<td>
<a href="https://msdn.microsoft.com/60428e66-9c08-418b-99e1-6824c638f2be">HTTP_CHANNEL_BIND_INFO</a>
</td>
</tr>
</table>
 




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




<a href="https://msdn.microsoft.com/12daffca-b403-4f06-8037-206f90e33252">HTTP Server API Version 2.0 Functions</a>



<a href="https://msdn.microsoft.com/e6bf68aa-d6a5-4079-b689-49cfc2303ba5">HttpAddUrlToUrlGroup</a>



<a href="https://msdn.microsoft.com/8b8e4ec9-3d85-4d64-98dc-86e5fd093e93">HttpCloseUrlGroup</a>



<a href="https://msdn.microsoft.com/6f2b14bb-ecb9-4a63-9bef-e2ceaf09f97a">HttpCreateUrlGroup</a>



<a href="https://msdn.microsoft.com/f3e8fde0-5a78-46aa-8c6c-cea957d12356">HttpQueryUrlGroupProperty</a>



<a href="https://msdn.microsoft.com/9c5c1fec-f3b4-414f-a841-e360f5f4e4db">HttpRemoveUrlFromUrlGroup</a>
 

 

