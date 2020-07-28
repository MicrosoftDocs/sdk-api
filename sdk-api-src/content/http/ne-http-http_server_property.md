---
UID: NE:http._HTTP_SERVER_PROPERTY
title: HTTP_SERVER_PROPERTY (http.h)
description: Defines the properties that are configured by the HTTP Server API on a URL group, server session, or request queue.
helpviewer_keywords: ["*PHTTP_SERVER_PROPERTY","*PHTTP_SERVER_PROPERTY enumeration [HTTP]","HTTP_SERVER_PROPERTY","HTTP_SERVER_PROPERTY enumeration [HTTP]","HttpServer503VerbosityProperty","HttpServerAuthenticationProperty","HttpServerBindingProperty","HttpServerChannelBindProperty","HttpServerExtendedAuthenticationProperty","HttpServerListenEndpointProperty","HttpServerLoggingProperty","HttpServerQosProperty","HttpServerQueueLengthProperty","HttpServerStateProperty","HttpServerTimeoutsProperty","http.http_server_property","http/*PHTTP_SERVER_PROPERTY","http/HTTP_SERVER_PROPERTY","http/HttpServer503VerbosityProperty","http/HttpServerAuthenticationProperty","http/HttpServerBindingProperty","http/HttpServerChannelBindProperty","http/HttpServerExtendedAuthenticationProperty","http/HttpServerListenEndpointProperty","http/HttpServerLoggingProperty","http/HttpServerQosProperty","http/HttpServerQueueLengthProperty","http/HttpServerStateProperty","http/HttpServerTimeoutsProperty"]
old-location: http\http_server_property.htm
tech.root: http
ms.assetid: 14865796-135c-43c2-955a-fdeae05a8278
ms.date: 12/05/2018
ms.keywords: '*PHTTP_SERVER_PROPERTY, *PHTTP_SERVER_PROPERTY enumeration [HTTP], HTTP_SERVER_PROPERTY, HTTP_SERVER_PROPERTY enumeration [HTTP], HttpServer503VerbosityProperty, HttpServerAuthenticationProperty, HttpServerBindingProperty, HttpServerChannelBindProperty, HttpServerExtendedAuthenticationProperty, HttpServerListenEndpointProperty, HttpServerLoggingProperty, HttpServerQosProperty, HttpServerQueueLengthProperty, HttpServerStateProperty, HttpServerTimeoutsProperty, http.http_server_property, http/*PHTTP_SERVER_PROPERTY, http/HTTP_SERVER_PROPERTY, http/HttpServer503VerbosityProperty, http/HttpServerAuthenticationProperty, http/HttpServerBindingProperty, http/HttpServerChannelBindProperty, http/HttpServerExtendedAuthenticationProperty, http/HttpServerListenEndpointProperty, http/HttpServerLoggingProperty, http/HttpServerQosProperty, http/HttpServerQueueLengthProperty, http/HttpServerStateProperty, http/HttpServerTimeoutsProperty'
f1_keywords:
- http/HTTP_SERVER_PROPERTY
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Http.h
api_name:
- HTTP_SERVER_PROPERTY
targetos: Windows
req.typenames: HTTP_SERVER_PROPERTY, *PHTTP_SERVER_PROPERTY
req.redist: 
ms.custom: 19H1
---

# HTTP_SERVER_PROPERTY enumeration


## -description


The <b>HTTP_SERVER_PROPERTY</b> enumeration defines the properties that are configured by the HTTP Server API on a URL group, server session, or request queue.


## -enum-fields




### -field HttpServerAuthenticationProperty

The authentication property enables server-side authentication for a URL group, or  server session using the Basic, NTLM, Negotiate, and Digest authentication schemes.

 The <a href="https://docs.microsoft.com/windows/desktop/api/http/ns-http-http_server_authentication_info">HTTP_SERVER_AUTHENTICATION_INFO</a>  structure contains the configuration data for this property.


### -field HttpServerLoggingProperty

The logging property enables logging for a server session or URL group.

The <a href="https://docs.microsoft.com/windows/desktop/api/http/ns-http-http_logging_info">HTTP_LOGGING_INFO</a> structure contains the configuration data for this property.


### -field HttpServerQosProperty

The QOS property enables settings affecting quality of service, such as limiting the maximum number of outstanding connections served for a URL group at any given time or limiting the response send bandwidth for a server session or URL group.

The <a href="https://docs.microsoft.com/windows/desktop/api/http/ns-http-http_qos_setting_info">HTTP_QOS_SETTING_INFO</a> structure contains the configuration data for this property.


### -field HttpServerTimeoutsProperty

The timeouts property  configures timeouts for a server session or URL group.

The <a href="https://docs.microsoft.com/windows/desktop/api/http/ns-http-http_timeout_limit_info">HTTP_TIMEOUT_LIMIT_INFO</a> structure contains the configuration data for this property.


### -field HttpServerQueueLengthProperty

The connections property limits the number of requests in the request queue. This is a <b>ULONG</b>.


### -field HttpServerStateProperty

The connections property configures the state of a URL group, server session, or request queue.

The <a href="https://docs.microsoft.com/windows/desktop/api/http/ns-http-http_state_info">HTTP_STATE_INFO</a> structure contains the configuration data for this property for the URL group or server session. The request queue uses the <a href="https://docs.microsoft.com/windows/desktop/api/http/ne-http-http_enabled_state">HTTP_ENABLED_STATE</a> enumeration to configure this property.


### -field HttpServer503VerbosityProperty

The 503 verbosity  property configures the verbosity level of 503 responses generated by the HTTP Server API for a request queue.

The <a href="https://docs.microsoft.com/windows/desktop/api/http/ne-http-http_503_response_verbosity">HTTP_503_RESPONSE_VERBOSITY</a> enumeration contains the configuration data for this property.


### -field HttpServerBindingProperty

The binding property associates a URL group with a  request queue.

The <a href="https://docs.microsoft.com/windows/desktop/api/http/ns-http-http_binding_info">HTTP_BINDING_INFO</a> structure contains the configuration data for this property.


### -field HttpServerExtendedAuthenticationProperty

The extended authentication property enables server-side authentication for a URL group, or  server session using the Kerberos authentication scheme.

 The <a href="https://docs.microsoft.com/windows/desktop/api/http/ns-http-http_server_authentication_info">HTTP_SERVER_AUTHENTICATION_INFO</a>  structure contains the configuration data for this property.


### -field HttpServerListenEndpointProperty

Listening endpoint property.


### -field HttpServerChannelBindProperty

This property implements authorization channel binding.

The <a href="https://docs.microsoft.com/windows/desktop/api/http/ns-http-http_channel_bind_info">HTTP_CHANNEL_BIND_INFO</a> structure contains the authorization details.


### -field HttpServerProtectionLevelProperty




## -remarks



The <b>HTTP_SERVER_PROPERTY</b> enumeration types are used to set or query the configurations on a server session, URL group, or request queue. A member of this enumeration together with the  associated configuration structure is used by <a href="https://docs.microsoft.com/windows/desktop/api/http/nf-http-httpqueryrequestqueueproperty">HttpQueryRequestQueueProperty</a>, <a href="https://docs.microsoft.com/windows/desktop/api/http/nf-http-httpqueryserversessionproperty">HttpQueryServerSessionProperty</a>, <a href="https://docs.microsoft.com/windows/desktop/api/http/nf-http-httpqueryurlgroupproperty">HttpQueryUrlGroupProperty</a>, <a href="https://docs.microsoft.com/windows/desktop/api/http/nf-http-httpsetrequestqueueproperty">HttpSetRequestQueueProperty</a>, <a href="https://docs.microsoft.com/windows/desktop/api/http/nf-http-httpsetserversessionproperty">HttpSetServerSessionProperty</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/http/nf-http-httpseturlgroupproperty">HttpSetUrlGroupProperty</a> to define the configuration parameters.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Http/http-server-api-version-2-0-enumeration-types">HTTP Server API Version 2.0 Enumeration Types</a>



<a href="https://docs.microsoft.com/windows/desktop/api/http/nf-http-httpqueryrequestqueueproperty">HttpQueryRequestQueueProperty</a>



<a href="https://docs.microsoft.com/windows/desktop/api/http/nf-http-httpqueryserversessionproperty">HttpQueryServerSessionProperty</a>



<a href="https://docs.microsoft.com/windows/desktop/api/http/nf-http-httpqueryurlgroupproperty">HttpQueryUrlGroupProperty</a>



<a href="https://docs.microsoft.com/windows/desktop/api/http/nf-http-httpsetrequestqueueproperty">HttpSetRequestQueueProperty</a>



<a href="https://docs.microsoft.com/windows/desktop/api/http/nf-http-httpsetserversessionproperty">HttpSetServerSessionProperty</a>



<a href="https://docs.microsoft.com/windows/desktop/api/http/nf-http-httpseturlgroupproperty">HttpSetUrlGroupProperty</a>
 

 

