---
UID: NE:webservices.__unnamed_enum_109
title: WS_BINDING_TEMPLATE_TYPE (webservices.h)
description: An enumeration of the different security binding combinations that are supported.
helpviewer_keywords: ["WS_BINDING_TEMPLATE_TYPE","WS_BINDING_TEMPLATE_TYPE enumeration [Web Services for Windows]","WS_HTTP_BINDING_TEMPLATE_TYPE","WS_HTTP_HEADER_AUTH_BINDING_TEMPLATE_TYPE","WS_HTTP_SSL_BINDING_TEMPLATE_TYPE","WS_HTTP_SSL_HEADER_AUTH_BINDING_TEMPLATE_TYPE","WS_HTTP_SSL_KERBEROS_APREQ_BINDING_TEMPLATE_TYPE","WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE","WS_HTTP_SSL_USERNAME_BINDING_TEMPLATE_TYPE","WS_HTTP_SSL_USERNAME_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE","WS_TCP_BINDING_TEMPLATE_TYPE","WS_TCP_SSPI_BINDING_TEMPLATE_TYPE","WS_TCP_SSPI_KERBEROS_APREQ_BINDING_TEMPLATE_TYPE","WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE","WS_TCP_SSPI_USERNAME_BINDING_TEMPLATE_TYPE","WS_TCP_SSPI_USERNAME_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE","webservices/WS_BINDING_TEMPLATE_TYPE","webservices/WS_HTTP_BINDING_TEMPLATE_TYPE","webservices/WS_HTTP_HEADER_AUTH_BINDING_TEMPLATE_TYPE","webservices/WS_HTTP_SSL_BINDING_TEMPLATE_TYPE","webservices/WS_HTTP_SSL_HEADER_AUTH_BINDING_TEMPLATE_TYPE","webservices/WS_HTTP_SSL_KERBEROS_APREQ_BINDING_TEMPLATE_TYPE","webservices/WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE","webservices/WS_HTTP_SSL_USERNAME_BINDING_TEMPLATE_TYPE","webservices/WS_HTTP_SSL_USERNAME_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE","webservices/WS_TCP_BINDING_TEMPLATE_TYPE","webservices/WS_TCP_SSPI_BINDING_TEMPLATE_TYPE","webservices/WS_TCP_SSPI_KERBEROS_APREQ_BINDING_TEMPLATE_TYPE","webservices/WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE","webservices/WS_TCP_SSPI_USERNAME_BINDING_TEMPLATE_TYPE","webservices/WS_TCP_SSPI_USERNAME_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE","wsw.ws_binding_template_type"]
old-location: wsw\ws_binding_template_type.htm
tech.root: wsw
ms.assetid: 831001f4-619d-4128-a645-85077701c28c
ms.date: 12/05/2018
ms.keywords: WS_BINDING_TEMPLATE_TYPE, WS_BINDING_TEMPLATE_TYPE enumeration [Web Services for Windows], WS_HTTP_BINDING_TEMPLATE_TYPE, WS_HTTP_HEADER_AUTH_BINDING_TEMPLATE_TYPE, WS_HTTP_SSL_BINDING_TEMPLATE_TYPE, WS_HTTP_SSL_HEADER_AUTH_BINDING_TEMPLATE_TYPE, WS_HTTP_SSL_KERBEROS_APREQ_BINDING_TEMPLATE_TYPE, WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE, WS_HTTP_SSL_USERNAME_BINDING_TEMPLATE_TYPE, WS_HTTP_SSL_USERNAME_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE, WS_TCP_BINDING_TEMPLATE_TYPE, WS_TCP_SSPI_BINDING_TEMPLATE_TYPE, WS_TCP_SSPI_KERBEROS_APREQ_BINDING_TEMPLATE_TYPE, WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE, WS_TCP_SSPI_USERNAME_BINDING_TEMPLATE_TYPE, WS_TCP_SSPI_USERNAME_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE, webservices/WS_BINDING_TEMPLATE_TYPE, webservices/WS_HTTP_BINDING_TEMPLATE_TYPE, webservices/WS_HTTP_HEADER_AUTH_BINDING_TEMPLATE_TYPE, webservices/WS_HTTP_SSL_BINDING_TEMPLATE_TYPE, webservices/WS_HTTP_SSL_HEADER_AUTH_BINDING_TEMPLATE_TYPE, webservices/WS_HTTP_SSL_KERBEROS_APREQ_BINDING_TEMPLATE_TYPE, webservices/WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE, webservices/WS_HTTP_SSL_USERNAME_BINDING_TEMPLATE_TYPE, webservices/WS_HTTP_SSL_USERNAME_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE, webservices/WS_TCP_BINDING_TEMPLATE_TYPE, webservices/WS_TCP_SSPI_BINDING_TEMPLATE_TYPE, webservices/WS_TCP_SSPI_KERBEROS_APREQ_BINDING_TEMPLATE_TYPE, webservices/WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE, webservices/WS_TCP_SSPI_USERNAME_BINDING_TEMPLATE_TYPE, webservices/WS_TCP_SSPI_USERNAME_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE, wsw.ws_binding_template_type
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
req.typenames: WS_BINDING_TEMPLATE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_BINDING_TEMPLATE_TYPE
 - webservices/WS_BINDING_TEMPLATE_TYPE
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
 - WS_BINDING_TEMPLATE_TYPE
---

# WS_BINDING_TEMPLATE_TYPE enumeration


## -description

An enumeration of the different security binding combinations that 
        are supported.

## -enum-fields

### -field WS_HTTP_BINDING_TEMPLATE_TYPE:0

The policy specifies HTTP channel binding.

### -field WS_HTTP_SSL_BINDING_TEMPLATE_TYPE:1

The policy specifies HTTP channel binding with <a href="/windows/desktop/api/webservices/ns-webservices-ws_ssl_transport_security_binding">WS_SSL_TRANSPORT_SECURITY_BINDING</a>.

### -field WS_HTTP_HEADER_AUTH_BINDING_TEMPLATE_TYPE:2

The policy specifies HTTP channel binding with <a href="/windows/desktop/api/webservices/ns-webservices-ws_http_header_auth_security_binding">WS_HTTP_HEADER_AUTH_SECURITY_BINDING</a>

### -field WS_HTTP_SSL_HEADER_AUTH_BINDING_TEMPLATE_TYPE:3

The policy specifies HTTP channel binding with <a href="/windows/desktop/api/webservices/ns-webservices-ws_ssl_transport_security_binding">WS_SSL_TRANSPORT_SECURITY_BINDING</a> and
          <a href="/windows/desktop/api/webservices/ns-webservices-ws_http_header_auth_security_binding">WS_HTTP_HEADER_AUTH_SECURITY_BINDING</a>.

### -field WS_HTTP_SSL_USERNAME_BINDING_TEMPLATE_TYPE:4

The policy specifies HTTP channel binding with <a href="/windows/desktop/api/webservices/ns-webservices-ws_ssl_transport_security_binding">WS_SSL_TRANSPORT_SECURITY_BINDING</a> 
          and <a href="/windows/desktop/api/webservices/ns-webservices-ws_username_message_security_binding">WS_USERNAME_MESSAGE_SECURITY_BINDING</a>.

### -field WS_HTTP_SSL_KERBEROS_APREQ_BINDING_TEMPLATE_TYPE:5

The policy specifies HTTP channel binding with <a href="/windows/desktop/api/webservices/ns-webservices-ws_ssl_transport_security_binding">WS_SSL_TRANSPORT_SECURITY_BINDING</a> and <a href="/windows/desktop/api/webservices/ns-webservices-ws_kerberos_apreq_message_security_binding">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING</a>.

### -field WS_TCP_BINDING_TEMPLATE_TYPE:6

The policy specifies TCP channel binding.

### -field WS_TCP_SSPI_BINDING_TEMPLATE_TYPE:7

The policy specifies TCP channel binding with <a href="/windows/desktop/api/webservices/ns-webservices-ws_tcp_sspi_transport_security_binding">WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING</a>.

### -field WS_TCP_SSPI_USERNAME_BINDING_TEMPLATE_TYPE:8

The policy specifies TCP channel binding with <a href="/windows/desktop/api/webservices/ns-webservices-ws_tcp_sspi_transport_security_binding">WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING</a> and
          <a href="/windows/desktop/api/webservices/ns-webservices-ws_username_message_security_binding">WS_USERNAME_MESSAGE_SECURITY_BINDING</a>.

### -field WS_TCP_SSPI_KERBEROS_APREQ_BINDING_TEMPLATE_TYPE:9

The policy specifies TCP channel binding with <a href="/windows/desktop/api/webservices/ns-webservices-ws_tcp_sspi_transport_security_binding">WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING</a> and
          <a href="/windows/desktop/api/webservices/ns-webservices-ws_kerberos_apreq_message_security_binding">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING</a>.

### -field WS_HTTP_SSL_USERNAME_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE:10

The policy specifies HTTP channel binding with <a href="/windows/desktop/api/webservices/ns-webservices-ws_ssl_transport_security_binding">WS_SSL_TRANSPORT_SECURITY_BINDING</a> and
          <a href="/windows/desktop/api/webservices/ns-webservices-ws_security_context_message_security_binding">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING</a>,  using bootstrap channel
          with HTTP channel binding, <b>WS_SSL_TRANSPORT_SECURITY_BINDING</b> and
          <a href="/windows/desktop/api/webservices/ns-webservices-ws_username_message_security_binding">WS_USERNAME_MESSAGE_SECURITY_BINDING</a>.

### -field WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE:11

The policy specifies HTTP channel binding with <a href="/windows/desktop/api/webservices/ns-webservices-ws_ssl_transport_security_binding">WS_SSL_TRANSPORT_SECURITY_BINDING</a> and
          <a href="/windows/desktop/api/webservices/ns-webservices-ws_security_context_message_security_binding">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING</a>,  using bootstrap channel
          with HTTP channel binding, <b>WS_SSL_TRANSPORT_SECURITY_BINDING</b> and
          <a href="/windows/desktop/api/webservices/ns-webservices-ws_kerberos_apreq_message_security_binding">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING</a>.

### -field WS_TCP_SSPI_USERNAME_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE:12

The policy specifies TCP channel binding with <a href="/windows/desktop/api/webservices/ns-webservices-ws_ssl_transport_security_binding">WS_SSL_TRANSPORT_SECURITY_BINDING</a> and
          <a href="/windows/desktop/api/webservices/ns-webservices-ws_security_context_message_security_binding">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING</a>,  using bootstrap channel
          with TCP channel binding, <b>WS_SSL_TRANSPORT_SECURITY_BINDING</b> and
          <a href="/windows/desktop/api/webservices/ns-webservices-ws_username_message_security_binding">WS_USERNAME_MESSAGE_SECURITY_BINDING</a>.

### -field WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE:13

The policy specifies TCP channel binding with <a href="/windows/desktop/api/webservices/ns-webservices-ws_ssl_transport_security_binding">WS_SSL_TRANSPORT_SECURITY_BINDING</a> and
          <a href="/windows/desktop/api/webservices/ns-webservices-ws_security_context_message_security_binding">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING</a>,  using bootstrap channel
          with TCP channel binding, <b>WS_SSL_TRANSPORT_SECURITY_BINDING</b> and
          <a href="/windows/desktop/api/webservices/ns-webservices-ws_kerberos_apreq_message_security_binding">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING</a>.
