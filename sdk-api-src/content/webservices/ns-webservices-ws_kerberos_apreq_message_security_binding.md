---
UID: NS:webservices._WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING
title: WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING (webservices.h)
description: The security binding subtype for specifying the use of the Kerberos AP_REQ ticket as a direct (i.e., without establishing a session) security token with WS-Security.
helpviewer_keywords: ["WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING","WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING structure [Web Services for Windows]","webservices/WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING","wsw.ws_kerberos_apreq_message_security_binding"]
old-location: wsw\ws_kerberos_apreq_message_security_binding.htm
tech.root: wsw
ms.assetid: 03127248-f5cc-44da-9c3d-abf016dd6bb2
ms.date: 12/05/2018
ms.keywords: WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING, WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING structure [Web Services for Windows], webservices/WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING, wsw.ws_kerberos_apreq_message_security_binding
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
req.typenames: WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING
 - webservices/_WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING
 - WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING
 - webservices/WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING
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
 - WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING
---

# WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING structure


## -description

The security binding subtype for specifying the use of the Kerberos
AP_REQ ticket as a direct (i.e., without establishing a session)
security token with WS-Security.
            

Only one instance of this binding may be present in a <a href="/windows/desktop/api/webservices/ns-webservices-ws_security_description">security description</a>.

This security binding is not supported with the <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_NAMEDPIPE_CHANNEL_BINDING</a>.

With this security binding, the following security binding properties may be specified:
<ul>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_binding_property_id">WS_SECURITY_BINDING_PROPERTY_ALLOWED_IMPERSONATION_LEVEL</a> (client side only)
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_binding_property_id">WS_SECURITY_BINDING_PROPERTY_ALLOW_ANONYMOUS_CLIENTS</a> (server side only)
</li>
</ul>


In Windows Vista and above on the client side, using this binding with HTTP will result in the message being sent using chunked transfer.

## -struct-fields

### -field binding

The base type from which this security binding subtype and all other security binding subtypes derive.

### -field bindingUsage

How the security token corresponding to this security binding should
be attached to a message.
                

Only <a href="/windows/desktop/api/webservices/ne-webservices-ws_message_security_usage">WS_SUPPORTING_MESSAGE_SECURITY_USAGE</a> is supported. With this usage, this security binding provides client authentication, but not message protection (such as signing, encryption, replay detection). Consequently, this binding is generally used together with another security binding such as the <a href="/windows/desktop/api/webservices/ns-webservices-ws_ssl_transport_security_binding">WS_SSL_TRANSPORT_SECURITY_BINDING</a> that provides a protected channel.


To use this binding on HTTP without SSL, the security description property <b>WS_SECURITY_PROPERTY_TRANSPORT_PROTECTION_LEVEL</b> must be explicitly set to <b>WS_PROTECTION_LEVEL_NONE</b>. This is not supported on the client or on TCP.

### -field clientCredential

The Windows Integrated Authentication credential to be used to obtain
the Kerberos ticket.  This field is required on the client side, but
must be <b>NULL</b> on the server side.