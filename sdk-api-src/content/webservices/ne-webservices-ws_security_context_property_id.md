---
UID: NE:webservices.__unnamed_enum_76
title: WS_SECURITY_CONTEXT_PROPERTY_ID (webservices.h)
description: Identifies a property of a security context object. This enumeration is used with WsGetSecurityContextProperty.
helpviewer_keywords: ["WS_SECURITY_CONTEXT_PROPERTY_ID","WS_SECURITY_CONTEXT_PROPERTY_ID enumeration [Web Services for Windows]","WS_SECURITY_CONTEXT_PROPERTY_IDENTIFIER","WS_SECURITY_CONTEXT_PROPERTY_MESSAGE_SECURITY_WINDOWS_TOKEN","WS_SECURITY_CONTEXT_PROPERTY_SAML_ASSERTION","WS_SECURITY_CONTEXT_PROPERTY_USERNAME","webservices/WS_SECURITY_CONTEXT_PROPERTY_ID","webservices/WS_SECURITY_CONTEXT_PROPERTY_IDENTIFIER","webservices/WS_SECURITY_CONTEXT_PROPERTY_MESSAGE_SECURITY_WINDOWS_TOKEN","webservices/WS_SECURITY_CONTEXT_PROPERTY_SAML_ASSERTION","webservices/WS_SECURITY_CONTEXT_PROPERTY_USERNAME","wsw.ws_security_context_property_id"]
old-location: wsw\ws_security_context_property_id.htm
tech.root: wsw
ms.assetid: fd2b92d4-9834-4d4b-85c3-8ea8d2c8bd8c
ms.date: 12/05/2018
ms.keywords: WS_SECURITY_CONTEXT_PROPERTY_ID, WS_SECURITY_CONTEXT_PROPERTY_ID enumeration [Web Services for Windows], WS_SECURITY_CONTEXT_PROPERTY_IDENTIFIER, WS_SECURITY_CONTEXT_PROPERTY_MESSAGE_SECURITY_WINDOWS_TOKEN, WS_SECURITY_CONTEXT_PROPERTY_SAML_ASSERTION, WS_SECURITY_CONTEXT_PROPERTY_USERNAME, webservices/WS_SECURITY_CONTEXT_PROPERTY_ID, webservices/WS_SECURITY_CONTEXT_PROPERTY_IDENTIFIER, webservices/WS_SECURITY_CONTEXT_PROPERTY_MESSAGE_SECURITY_WINDOWS_TOKEN, webservices/WS_SECURITY_CONTEXT_PROPERTY_SAML_ASSERTION, webservices/WS_SECURITY_CONTEXT_PROPERTY_USERNAME, wsw.ws_security_context_property_id
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
req.typenames: WS_SECURITY_CONTEXT_PROPERTY_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_SECURITY_CONTEXT_PROPERTY_ID
 - webservices/WS_SECURITY_CONTEXT_PROPERTY_ID
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
 - WS_SECURITY_CONTEXT_PROPERTY_ID
---

# WS_SECURITY_CONTEXT_PROPERTY_ID enumeration


## -description

Identifies a property of a security context object.  This enumeration is used with <a href="/windows/desktop/api/webservices/nf-webservices-wsgetsecuritycontextproperty">WsGetSecurityContextProperty</a>.

## -enum-fields

### -field WS_SECURITY_CONTEXT_PROPERTY_IDENTIFIER:1

On the wire, a security context is identified by an absolute URI, which is unique to both sender and 
          recipient. See <a href="https://docs.oasis-open.org/ws-sx/ws-secureconversation/200512/ws-secureconversation-1.3-os.html">WS-SecureConversation</a>.
          This property is a <a href="/windows/desktop/api/webservices/ns-webservices-ws_unique_id">WS_UNIQUE_ID</a> structure that represents that URI.

### -field WS_SECURITY_CONTEXT_PROPERTY_USERNAME:2

If a <a href="/windows/desktop/api/webservices/ns-webservices-ws_username_message_security_binding">WS_USERNAME_MESSAGE_SECURITY_BINDING</a> is used as bootstrap security, this property
          is a <a href="/windows/desktop/api/webservices/ns-webservices-ws_string">WS_STRING</a> that represents the username that was used during the establishment of the security context.

### -field WS_SECURITY_CONTEXT_PROPERTY_MESSAGE_SECURITY_WINDOWS_TOKEN:3

If a <a href="/windows/desktop/api/webservices/ns-webservices-ws_kerberos_apreq_message_security_binding">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING</a> is used as bootstrap security, this property
          is a <b>HANDLE</b> that represents the token that was used during the establishment of the security context.

### -field WS_SECURITY_CONTEXT_PROPERTY_SAML_ASSERTION:4

If a <a href="/windows/win32/api/webservices/ns-webservices-ws_saml_message_security_binding">WS_SAML_MESSAGE_SECURITY_BINDING</a> is used as bootstrap security, this property
          is a pointer to a <a href="/windows/desktop/wsw/ws-xml-buffer">WS_XML_BUFFER</a> that represents the SAML assertion that was used during the establishment of the security context.
