---
UID: NS:webservices._WS_SSL_TRANSPORT_SECURITY_BINDING_TEMPLATE
title: WS_SSL_TRANSPORT_SECURITY_BINDING_TEMPLATE (webservices.h)
description: The security binding template for specifying the use of SSL/TLS protocol based transport security.
helpviewer_keywords: ["WS_SSL_TRANSPORT_SECURITY_BINDING_TEMPLATE","WS_SSL_TRANSPORT_SECURITY_BINDING_TEMPLATE structure [Web Services for Windows]","webservices/WS_SSL_TRANSPORT_SECURITY_BINDING_TEMPLATE","wsw.ws_ssl_transport_security_binding_template"]
old-location: wsw\ws_ssl_transport_security_binding_template.htm
tech.root: wsw
ms.assetid: 6b7e9ed6-0337-479d-9a83-dec5770c050d
ms.date: 12/05/2018
ms.keywords: WS_SSL_TRANSPORT_SECURITY_BINDING_TEMPLATE, WS_SSL_TRANSPORT_SECURITY_BINDING_TEMPLATE structure [Web Services for Windows], webservices/WS_SSL_TRANSPORT_SECURITY_BINDING_TEMPLATE, wsw.ws_ssl_transport_security_binding_template
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
req.typenames: WS_SSL_TRANSPORT_SECURITY_BINDING_TEMPLATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_SSL_TRANSPORT_SECURITY_BINDING_TEMPLATE
 - webservices/_WS_SSL_TRANSPORT_SECURITY_BINDING_TEMPLATE
 - WS_SSL_TRANSPORT_SECURITY_BINDING_TEMPLATE
 - webservices/WS_SSL_TRANSPORT_SECURITY_BINDING_TEMPLATE
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
 - WS_SSL_TRANSPORT_SECURITY_BINDING_TEMPLATE
---

# WS_SSL_TRANSPORT_SECURITY_BINDING_TEMPLATE structure


## -description

The security binding template for specifying the use of SSL/TLS
        protocol based transport security. 
      

See also <a href="/windows/desktop/api/webservices/ns-webservices-ws_ssl_transport_security_binding">WS_SSL_TRANSPORT_SECURITY_BINDING</a>.

This security binding is supported only with the
        <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_HTTP_CHANNEL_BINDING</a>.

## -struct-fields

### -field securityBindingProperties

Application provided security binding properties that cannot be represented in policy.

### -field localCertCredential

The local certificate credential to be used with this security binding.
        

Server side: When SSL is used for transport security with <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_HTTP_CHANNEL_BINDING</a>, the server certificate must be
          registered by the application using the <a href="/windows/win32/http/httpcfg-exe">HttpCfg.exe</a> and this field must be set to <b>NULL</b>.  In all other cases, the
          server SSL certificate must be specified using this field.
        

Client side: If a client certificate is to be used with SSL, it must
          be specified using this field.  If no client certificate is to be
          used, this field must be set to <b>NULL</b>.