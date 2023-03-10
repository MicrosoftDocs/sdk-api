---
UID: NS:webservices._WS_SAML_MESSAGE_SECURITY_BINDING
title: WS_SAML_MESSAGE_SECURITY_BINDING (webservices.h)
description: The security binding subtype for specifying the use of a SAML assertion as a message security token.
helpviewer_keywords: ["WS_SAML_MESSAGE_SECURITY_BINDING","WS_SAML_MESSAGE_SECURITY_BINDING structure [Web Services for Windows]","webservices/WS_SAML_MESSAGE_SECURITY_BINDING","wsw.ws_saml_message_security_binding"]
old-location: wsw\ws_saml_message_security_binding.htm
tech.root: wsw
ms.assetid: 713afe9a-49b8-419a-b78b-d3b5a4a8d073
ms.date: 12/05/2018
ms.keywords: WS_SAML_MESSAGE_SECURITY_BINDING, WS_SAML_MESSAGE_SECURITY_BINDING structure [Web Services for Windows], webservices/WS_SAML_MESSAGE_SECURITY_BINDING, wsw.ws_saml_message_security_binding
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
req.typenames: WS_SAML_MESSAGE_SECURITY_BINDING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_SAML_MESSAGE_SECURITY_BINDING
 - webservices/_WS_SAML_MESSAGE_SECURITY_BINDING
 - WS_SAML_MESSAGE_SECURITY_BINDING
 - webservices/WS_SAML_MESSAGE_SECURITY_BINDING
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
 - WS_SAML_MESSAGE_SECURITY_BINDING
---

# WS_SAML_MESSAGE_SECURITY_BINDING structure


## -description

The security binding subtype for specifying the use of a SAML
assertion as a message security token.  The SAML token is expected to
be presented to a service in a WS-Security header according to the
bindingUsage specified.  This security binding may be included in a 
<a href="/windows/desktop/api/webservices/ns-webservices-ws_security_description">security description</a> only on the
server side.
           

Only one instance of this binding may be present in a <a href="/windows/desktop/api/webservices/ns-webservices-ws_security_description">security description</a>.

This security binding is not supported with the <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_NAMEDPIPE_CHANNEL_BINDING</a>.

For a <a href="/windows/desktop/wsw/federation">federated security</a> scenario that
involves getting a security token from an issuer and then presenting
it to a service, one may use <a href="/windows/win32/api/webservices/ns-webservices-ws_xml_token_message_security_binding">WsRequestSecurityToken</a> together with the <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_token_message_security_binding">WS_XML_TOKEN_MESSAGE_SECURITY_BINDING</a> on
the client side, and this binding on the server side.
           

The extent of validation performed on the received SAML depends on the
authenticator specified.  If additional validation is required, the
application may get the received SAML assertion using 
<a href="/windows/desktop/api/webservices/nf-webservices-wsgetmessageproperty">WsGetMessageProperty</a> with the key <a href="/windows/desktop/api/webservices/ne-webservices-ws_message_property_id">WS_MESSAGE_PROPERTY_SAML_ASSERTION</a> 
and do further processing.
            

With this security binding, no security binding properties may be specified:

## -struct-fields

### -field binding

The base type from which this security binding subtype and all other security binding subtypes derive.

### -field bindingUsage

How the security token corresponding to this security binding should be bound to a message.
                
Only <a href="/windows/desktop/api/webservices/ne-webservices-ws_message_security_usage">WS_SUPPORTING_MESSAGE_SECURITY_USAGE</a> is

supported.  With this usage, this security binding provides client
authentication, but not message protection (such as signing,
encryption, replay detection).  Thus, this binding must be used
together with another security binding such as the <a href="/windows/desktop/api/webservices/ns-webservices-ws_ssl_transport_security_binding">WS_SSL_TRANSPORT_SECURITY_BINDING</a> that provides a protected
channel.
                

To use this binding on HTTP without SSL, the security description property <b>WS_SECURITY_PROPERTY_TRANSPORT_PROTECTION_LEVEL</b> must be explicitly set to <b>WS_PROTECTION_LEVEL_NONE</b>. This is not supported on the client or on TCP.

### -field authenticator

The authenticator for validating incoming SAML tokens.  This field is
required.