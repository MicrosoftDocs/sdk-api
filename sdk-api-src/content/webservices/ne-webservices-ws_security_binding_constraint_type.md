---
UID: NE:webservices.__unnamed_enum_107
title: WS_SECURITY_BINDING_CONSTRAINT_TYPE (webservices.h)
description: The values in this enumeration are used to identify the sub-types of WS_SECURITY_BINDING_CONSTRAINT.
helpviewer_keywords: ["WS_CERT_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE","WS_HTTP_HEADER_AUTH_SECURITY_BINDING_CONSTRAINT_TYPE","WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE","WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE","WS_SECURITY_BINDING_CONSTRAINT_TYPE","WS_SECURITY_BINDING_CONSTRAINT_TYPE enumeration [Web Services for Windows]","WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE","WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT_TYPE","WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_CONSTRAINT_TYPE","WS_USERNAME_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE","webservices/WS_CERT_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE","webservices/WS_HTTP_HEADER_AUTH_SECURITY_BINDING_CONSTRAINT_TYPE","webservices/WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE","webservices/WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE","webservices/WS_SECURITY_BINDING_CONSTRAINT_TYPE","webservices/WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE","webservices/WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT_TYPE","webservices/WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_CONSTRAINT_TYPE","webservices/WS_USERNAME_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE","wsw.ws_security_binding_constraint_type"]
old-location: wsw\ws_security_binding_constraint_type.htm
tech.root: wsw
ms.assetid: 198869b4-0f25-4f10-8740-e4d501f6791b
ms.date: 12/05/2018
ms.keywords: WS_CERT_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE, WS_HTTP_HEADER_AUTH_SECURITY_BINDING_CONSTRAINT_TYPE, WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE, WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE, WS_SECURITY_BINDING_CONSTRAINT_TYPE, WS_SECURITY_BINDING_CONSTRAINT_TYPE enumeration [Web Services for Windows], WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE, WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT_TYPE, WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_CONSTRAINT_TYPE, WS_USERNAME_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE, webservices/WS_CERT_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE, webservices/WS_HTTP_HEADER_AUTH_SECURITY_BINDING_CONSTRAINT_TYPE, webservices/WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE, webservices/WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE, webservices/WS_SECURITY_BINDING_CONSTRAINT_TYPE, webservices/WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE, webservices/WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT_TYPE, webservices/WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_CONSTRAINT_TYPE, webservices/WS_USERNAME_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE, wsw.ws_security_binding_constraint_type
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
req.typenames: WS_SECURITY_BINDING_CONSTRAINT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_SECURITY_BINDING_CONSTRAINT_TYPE
 - webservices/WS_SECURITY_BINDING_CONSTRAINT_TYPE
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
 - WS_SECURITY_BINDING_CONSTRAINT_TYPE
---

# WS_SECURITY_BINDING_CONSTRAINT_TYPE enumeration


## -description

The values in this enumeration are used to identify the sub-types of <a href="/windows/win32/api/webservices/ns-webservices-ws_security_binding_constraint">WS_SECURITY_BINDING_CONSTRAINT</a>.

## -enum-fields

### -field WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT_TYPE:1

This value is used in the type field of <a href="/windows/win32/api/webservices/ns-webservices-ws_security_binding_constraint">WS_SECURITY_BINDING_CONSTRAINT</a> to identify a <a href="/windows/desktop/api/webservices/ns-webservices-ws_ssl_transport_security_binding_constraint">WS_SSL_TRANSPORT_SECURITY_BINDING_CONSTRAINT</a> structure.

### -field WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_CONSTRAINT_TYPE:2

This value is used in the type field of <a href="/windows/win32/api/webservices/ns-webservices-ws_security_binding_constraint">WS_SECURITY_BINDING_CONSTRAINT</a> to identify a <a href="/windows/desktop/api/webservices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint">WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_CONSTRAINT</a> structure.

### -field WS_HTTP_HEADER_AUTH_SECURITY_BINDING_CONSTRAINT_TYPE:3

This value is used in the type field of <a href="/windows/win32/api/webservices/ns-webservices-ws_security_binding_constraint">WS_SECURITY_BINDING_CONSTRAINT</a> to identify a <a href="/windows/desktop/api/webservices/ns-webservices-ws_http_header_auth_security_binding_constraint">WS_HTTP_HEADER_AUTH_SECURITY_BINDING_CONSTRAINT</a> structure.

### -field WS_USERNAME_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE:4

This value is used in the type field of <a href="/windows/win32/api/webservices/ns-webservices-ws_security_binding_constraint">WS_SECURITY_BINDING_CONSTRAINT</a> to identify a <a href="/windows/desktop/api/webservices/ns-webservices-ws_username_message_security_binding_constraint">WS_USERNAME_MESSAGE_SECURITY_BINDING_CONSTRAINT</a> structure.

### -field WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE:5

This value is used in the type field of <a href="/windows/win32/api/webservices/ns-webservices-ws_security_binding_constraint">WS_SECURITY_BINDING_CONSTRAINT</a> to identify a <a href="/windows/desktop/api/webservices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_CONSTRAINT</a> structure.

### -field WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE:6

This value is used in the type field of <a href="/windows/win32/api/webservices/ns-webservices-ws_security_binding_constraint">WS_SECURITY_BINDING_CONSTRAINT</a> to identify a <a href="/windows/desktop/api/webservices/ns-webservices-ws_issued_token_message_security_binding_constraint">WS_ISSUED_TOKEN_MESSAGE_SECURITY_BINDING_CONSTRAINT</a> structure.

### -field WS_CERT_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE:7

This value is used in the type field of <a href="/windows/win32/api/webservices/ns-webservices-ws_security_binding_constraint">WS_SECURITY_BINDING_CONSTRAINT</a> to identify a <a href="/windows/desktop/api/webservices/ns-webservices-ws_cert_message_security_binding_constraint">WS_CERT_MESSAGE_SECURITY_BINDING_CONSTRAINT</a> structure.

### -field WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT_TYPE:8

This value is used in the type field of <a href="/windows/win32/api/webservices/ns-webservices-ws_security_binding_constraint">WS_SECURITY_BINDING_CONSTRAINT</a> to identify a <a href="/windows/desktop/api/webservices/ns-webservices-ws_security_context_message_security_binding_constraint">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT</a> structure.
