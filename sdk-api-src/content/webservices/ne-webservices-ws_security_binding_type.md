---
UID: NE:webservices.__unnamed_enum_47
title: WS_SECURITY_BINDING_TYPE (webservices.h)
description: The type of the security binding, used as a selector for subtypes of WS_SECURITY_BINDING.
helpviewer_keywords: ["WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TYPE","WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_TYPE","WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING_TYPE","WS_SAML_MESSAGE_SECURITY_BINDING_TYPE","WS_SECURITY_BINDING_TYPE","WS_SECURITY_BINDING_TYPE enumeration [Web Services for Windows]","WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_TYPE","WS_SSL_TRANSPORT_SECURITY_BINDING_TYPE","WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TYPE","WS_USERNAME_MESSAGE_SECURITY_BINDING_TYPE","WS_XML_TOKEN_MESSAGE_SECURITY_BINDING_TYPE","webservices/WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TYPE","webservices/WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_TYPE","webservices/WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING_TYPE","webservices/WS_SAML_MESSAGE_SECURITY_BINDING_TYPE","webservices/WS_SECURITY_BINDING_TYPE","webservices/WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_TYPE","webservices/WS_SSL_TRANSPORT_SECURITY_BINDING_TYPE","webservices/WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TYPE","webservices/WS_USERNAME_MESSAGE_SECURITY_BINDING_TYPE","webservices/WS_XML_TOKEN_MESSAGE_SECURITY_BINDING_TYPE","wsw.ws_security_binding_type"]
old-location: wsw\ws_security_binding_type.htm
tech.root: wsw
ms.assetid: caa3d71c-420c-4be0-a371-0f2d48ebd757
ms.date: 12/05/2018
ms.keywords: WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TYPE, WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_TYPE, WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING_TYPE, WS_SAML_MESSAGE_SECURITY_BINDING_TYPE, WS_SECURITY_BINDING_TYPE, WS_SECURITY_BINDING_TYPE enumeration [Web Services for Windows], WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_TYPE, WS_SSL_TRANSPORT_SECURITY_BINDING_TYPE, WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TYPE, WS_USERNAME_MESSAGE_SECURITY_BINDING_TYPE, WS_XML_TOKEN_MESSAGE_SECURITY_BINDING_TYPE, webservices/WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TYPE, webservices/WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_TYPE, webservices/WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING_TYPE, webservices/WS_SAML_MESSAGE_SECURITY_BINDING_TYPE, webservices/WS_SECURITY_BINDING_TYPE, webservices/WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_TYPE, webservices/WS_SSL_TRANSPORT_SECURITY_BINDING_TYPE, webservices/WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TYPE, webservices/WS_USERNAME_MESSAGE_SECURITY_BINDING_TYPE, webservices/WS_XML_TOKEN_MESSAGE_SECURITY_BINDING_TYPE, wsw.ws_security_binding_type
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: WS_SECURITY_BINDING_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_SECURITY_BINDING_TYPE
 - webservices/WS_SECURITY_BINDING_TYPE
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
 - WS_SECURITY_BINDING_TYPE
---

# WS_SECURITY_BINDING_TYPE enumeration


## -description

The type of the security binding, used as a selector for subtypes of
<a href="/windows/desktop/api/webservices/ns-webservices-ws_security_binding">WS_SECURITY_BINDING</a>.  In general, the type name of the
security binding (one of the values defined here) specifies how the
security token used with that security binding is obtained and used.

## -enum-fields

### -field WS_SSL_TRANSPORT_SECURITY_BINDING_TYPE:1

Type id for the security binding <a href="/windows/desktop/api/webservices/ns-webservices-ws_ssl_transport_security_binding">WS_SSL_TRANSPORT_SECURITY_BINDING</a>.

### -field WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TYPE:2

Type id for the security binding <a href="/windows/desktop/api/webservices/ns-webservices-ws_tcp_sspi_transport_security_binding">WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING</a>.

### -field WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TYPE:3

Type id for the security binding <a href="/windows/desktop/api/webservices/ns-webservices-ws_http_header_auth_security_binding">WS_HTTP_HEADER_AUTH_SECURITY_BINDING</a>.

### -field WS_USERNAME_MESSAGE_SECURITY_BINDING_TYPE:4

Type id for the security binding <a href="/windows/desktop/api/webservices/ns-webservices-ws_username_message_security_binding">WS_USERNAME_MESSAGE_SECURITY_BINDING</a>.

### -field WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_TYPE:5

Type id for the security binding <a href="/windows/desktop/api/webservices/ns-webservices-ws_kerberos_apreq_message_security_binding">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING</a>.

### -field WS_XML_TOKEN_MESSAGE_SECURITY_BINDING_TYPE:6

Type id for the security binding <a href="/windows/win32/api/webservices/ns-webservices-ws_xml_token_message_security_binding">WS_XML_TOKEN_MESSAGE_SECURITY_BINDING</a>.

### -field WS_SAML_MESSAGE_SECURITY_BINDING_TYPE:7

Type id for the security binding <a href="/windows/win32/api/webservices/ns-webservices-ws_saml_message_security_binding">WS_SAML_MESSAGE_SECURITY_BINDING</a>.

### -field WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_TYPE:8

Type id for the security binding <a href="/windows/desktop/api/webservices/ns-webservices-ws_security_context_message_security_binding">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING</a>.

### -field WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING_TYPE:9

Windows 8 or later:
Type id for the security binding <a href="/windows/win32/api/webservices/ns-webservices-ws_namedpipe_sspi_transport_security_binding">WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING</a>.
