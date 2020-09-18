---
UID: NS:webservices._WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING
title: WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING (webservices.h)
description: The security binding subtype for specifying the use of the Windows Integrated Authentication protocol (such as Kerberos, NTLM or SPNEGO) with the named pipe transport.
helpviewer_keywords: ["WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING","WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING structure [Web Services for Windows]","webservices/WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING","wsw.ws_namedpipe_sspi_transport_security_binding"]
old-location: wsw\ws_namedpipe_sspi_transport_security_binding.htm
tech.root: wsw
ms.assetid: 02FCD206-23BC-4ED0-9E4A-76AB0926FD7C
ms.date: 12/05/2018
ms.keywords: WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING, WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING structure [Web Services for Windows], webservices/WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING, wsw.ws_namedpipe_sspi_transport_security_binding
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING
 - webservices/_WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING
 - WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING
 - webservices/WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING
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
 - WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING
---

# WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING structure


## -description

The security binding subtype for specifying the use of the Windows Integrated Authentication protocol (such as Kerberos, NTLM or SPNEGO) with the named pipe transport. A specific SSP package may be chosen using the security binding property <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_property_id">WS_SECURITY_BINDING_PROPERTY_WINDOWS_INTEGRATED_AUTH_PACKAGE</a>; if that property is not specified, SPNEGO is used by default.

This security binding operates at the transport security level and is supported only with the <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_NAMEDPIPE_CHANNEL_BINDING</a>. The NamedPipe/Windows SSPI combination uses the wire form defined by the <a href="/openspecs/windows_protocols/mc-nmf/0aab922d-8023-48bb-8ba2-c4d3404cc69d">NegotiateStream</a> protocol and the <a href="/openspecs/windows_protocols/ms-nns/93df08eb-a6c4-4dff-81c3-519cf7236df4">.Net Message Framing</a> specification. 

On the client side, the security identity of the target server is specified using the identity field of the <a href="/windows/desktop/api/webservices/ns-webservices-ws_endpoint_address">WS_ENDPOINT_ADDRESS</a> parameter supplied during <a href="/windows/desktop/api/webservices/nf-webservices-wsopenchannel">WsOpenChannel</a>. 



The named pipe binding supports only this one transport security binding and does not support any message security bindings. 

With this security binding, the following security binding properties may be specified: 
<ul>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_property_id">WS_SECURITY_BINDING_PROPERTY_WINDOWS_INTEGRATED_AUTH_PACKAGE</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_property_id">WS_SECURITY_BINDING_PROPERTY_REQUIRE_SERVER_AUTH</a> (client side only)</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_property_id">WS_SECURITY_BINDING_PROPERTY_ALLOW_ANONYMOUS_CLIENTS</a> (server side only)</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_security_property_id">WS_SECURITY_BINDING_PROPERTY_ALLOWED_IMPERSONATION_LEVEL</a> (client side only)</li>
</ul>This type derives from the base type <a href="/windows/desktop/api/webservices/ns-webservices-ws_security_binding">WS_SECURITY_BINDING</a>. For an instance of this type, the type selector field <b>bindingType</b> must have the value <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_binding_type">WS_NAMEDPIPE_SSPI_TRANSPORT_SECURITY_BINDING_TYPE</a>.

## -struct-fields

### -field binding

The <a href="/windows/desktop/api/webservices/ns-webservices-ws_security_binding">base type</a> from which this security binding subtype and all other security binding subtypes derive.

### -field clientCredential

The <a href="/windows/win32/api/webservices/ns-webservices-ws_windows_integrated_auth_credential">WS_WINDOWS_INTEGRATED_AUTH_CREDENTIAL</a> structure to be used to authenticate the client. This is required on the client and must not be specified on the server.