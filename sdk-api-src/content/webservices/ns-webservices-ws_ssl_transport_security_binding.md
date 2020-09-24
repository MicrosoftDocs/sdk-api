---
UID: NS:webservices._WS_SSL_TRANSPORT_SECURITY_BINDING
title: WS_SSL_TRANSPORT_SECURITY_BINDING (webservices.h)
description: The security binding subtype for specifying the use of SSL/TLS protocol based transport security.
helpviewer_keywords: ["WS_SSL_TRANSPORT_SECURITY_BINDING","WS_SSL_TRANSPORT_SECURITY_BINDING structure [Web Services for Windows]","webservices/WS_SSL_TRANSPORT_SECURITY_BINDING","wsw.ws_ssl_transport_security_binding"]
old-location: wsw\ws_ssl_transport_security_binding.htm
tech.root: wsw
ms.assetid: 078efc1d-a1bc-4035-919c-f927a8ceb8e6
ms.date: 12/05/2018
ms.keywords: WS_SSL_TRANSPORT_SECURITY_BINDING, WS_SSL_TRANSPORT_SECURITY_BINDING structure [Web Services for Windows], webservices/WS_SSL_TRANSPORT_SECURITY_BINDING, wsw.ws_ssl_transport_security_binding
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
req.typenames: WS_SSL_TRANSPORT_SECURITY_BINDING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_SSL_TRANSPORT_SECURITY_BINDING
 - webservices/_WS_SSL_TRANSPORT_SECURITY_BINDING
 - WS_SSL_TRANSPORT_SECURITY_BINDING
 - webservices/WS_SSL_TRANSPORT_SECURITY_BINDING
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
 - WS_SSL_TRANSPORT_SECURITY_BINDING
---

# WS_SSL_TRANSPORT_SECURITY_BINDING structure


## -description

The security binding subtype for specifying the use of SSL/TLS
protocol based transport security.
            

This security binding is supported only with the
                <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_HTTP_CHANNEL_BINDING</a>.
            

With this security binding, the following security binding properties may be specified:
<ul>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_binding_property_id">WS_SECURITY_BINDING_PROPERTY_CERT_FAILURES_TO_IGNORE</a> (client side only)
                    </li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_binding_property_id">WS_SECURITY_BINDING_PROPERTY_DISABLE_CERT_REVOCATION_CHECK</a> (client side only)                    
                    </li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_binding_property_id">WS_SECURITY_BINDING_PROPERTY_REQUIRE_SSL_CLIENT_CERT</a> (server side only)

</li>
</ul>

## -struct-fields

### -field binding

The base type from which this security binding subtype and all other security binding subtypes derive.

### -field localCertCredential

The local certificate credential to be used with this security binding.
                

Server side: When SSL is used for transport security with <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_HTTP_CHANNEL_BINDING</a>, the server certificate must be
registered by the application using the httpcfg
tool and this field must be set to <b>NULL</b>.  In all other cases, the
server SSL certificate must be specified using this field.
                

Client side: If a client certificate is to be used with SSL, it must
be specified using this field.  If no client certificate is to be
used, this field must be set to <b>NULL</b>.