---
UID: NS:webservices._WS_HTTP_HEADER_AUTH_SECURITY_BINDING
title: WS_HTTP_HEADER_AUTH_SECURITY_BINDING (webservices.h)
description: The security binding subtype for specifying the use of HTTP header authentication against a target service or a HTTP proxy server based on the basic, digest (RFC 2617) and the SPNEGO (RFC4559) protocols.
helpviewer_keywords: ["WS_HTTP_HEADER_AUTH_SECURITY_BINDING","WS_HTTP_HEADER_AUTH_SECURITY_BINDING structure [Web Services for Windows]","webservices/WS_HTTP_HEADER_AUTH_SECURITY_BINDING","wsw.ws_http_header_auth_security_binding"]
old-location: wsw\ws_http_header_auth_security_binding.htm
tech.root: wsw
ms.assetid: c6ca6760-a927-470f-9785-7500d1711902
ms.date: 12/05/2018
ms.keywords: WS_HTTP_HEADER_AUTH_SECURITY_BINDING, WS_HTTP_HEADER_AUTH_SECURITY_BINDING structure [Web Services for Windows], webservices/WS_HTTP_HEADER_AUTH_SECURITY_BINDING, wsw.ws_http_header_auth_security_binding
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
targetos: Windows
req.typenames: WS_HTTP_HEADER_AUTH_SECURITY_BINDING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_HTTP_HEADER_AUTH_SECURITY_BINDING
 - webservices/_WS_HTTP_HEADER_AUTH_SECURITY_BINDING
 - WS_HTTP_HEADER_AUTH_SECURITY_BINDING
 - webservices/WS_HTTP_HEADER_AUTH_SECURITY_BINDING
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_HTTP_HEADER_AUTH_SECURITY_BINDING
---

# WS_HTTP_HEADER_AUTH_SECURITY_BINDING structure


## -description

The security binding subtype for specifying the use of HTTP header authentication against a target service or a HTTP proxy server 
                based on the basic, digest (RFC 2617) and the SPNEGO (RFC4559) protocols.
                Since this security binding operates at the HTTP header level, it is supported only with the <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_HTTP_CHANNEL_BINDING</a>. 
                By default, this security binding is used for the target service. However  <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_binding_property_id">WS_SECURITY_BINDING_PROPERTY_HTTP_HEADER_AUTH_TARGET</a> 
                security binding property can be specified to use it for a HTTP proxy server. This binding provides client authentication, but not message protection
                since the HTTP body is unaffected by this binding. While this security binding can be used alone, such usage is not recommended;
                more typically, HTTP header authentication is done in conjunction with transport level security provided by a security binding such as the 
                <a href="/windows/desktop/api/webservices/ns-webservices-ws_ssl_transport_security_binding">WS_SSL_TRANSPORT_SECURITY_BINDING</a>. To use this binding without SSL, the security description property <b>WS_SECURITY_PROPERTY_TRANSPORT_PROTECTION_LEVEL</b> must be explicitly set to <b>WS_PROTECTION_LEVEL_NONE</b>.

With this security binding, the following security binding properties may be specified:
<ul>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_binding_property_id">WS_SECURITY_BINDING_PROPERTY_HTTP_HEADER_AUTH_SCHEME</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_binding_property_id">WS_SECURITY_BINDING_PROPERTY_HTTP_HEADER_AUTH_TARGET</a> (client side only)</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_binding_property_id">WS_SECURITY_BINDING_PROPERTY_HTTP_HEADER_AUTH_BASIC_REALM</a> (server side only)</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_binding_property_id">WS_SECURITY_BINDING_PROPERTY_HTTP_HEADER_AUTH_DIGEST_REALM</a> (server side only)</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_binding_property_id">WS_SECURITY_BINDING_PROPERTY_HTTP_HEADER_AUTH_DIGEST_DOMAIN</a> (server side only)</li>
</ul>

## -struct-fields

### -field binding

The base type from which this security binding subtype and all other security binding subtypes derive.

### -field clientCredential

The Windows Integrated Authentication credential to be used to
authenticate the client.  This is required on the client side and must
be <b>NULL</b> on the server side.
                

If the credential used is a <a href="/windows/win32/api/webservices/ns-webservices-ws_default_windows_integrated_auth_credential">WS_DEFAULT_WINDOWS_INTEGRATED_AUTH_CREDENTIAL</a> then 
                    <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_binding_property_id">WS_SECURITY_BINDING_PROPERTY_HTTP_HEADER_AUTH_SCHEME</a> must be set to 
                    <a href="/windows/win32/api/webservices/ne-webservices-ws_xml_node_type">WS_HTTP_HEADER_AUTH_SCHEME_NONE</a>, <b>WS_HTTP_HEADER_AUTH_SCHEME_NTLM</b>, 
                    <b>WS_HTTP_HEADER_AUTH_SCHEME_NEGOTIATE</b> or <b>WS_HTTP_HEADER_AUTH_SCHEME_PASSPORT</b>.
                    <b>WS_HTTP_HEADER_AUTH_SCHEME_PASSPORT</b> defaults to using the Passport keyring.