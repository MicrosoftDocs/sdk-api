---
UID: NS:webservices._WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TEMPLATE
title: WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TEMPLATE (webservices.h)
description: The security binding template for specifying the use of Windows SSPI protocol based transport security.
helpviewer_keywords: ["WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TEMPLATE","WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TEMPLATE structure [Web Services for Windows]","webservices/WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TEMPLATE","wsw.ws_tcp_sspi_transport_security_binding_template"]
old-location: wsw\ws_tcp_sspi_transport_security_binding_template.htm
tech.root: wsw
ms.assetid: bdfd8bfe-a46d-4bbf-81e3-c0183fcd25bf
ms.date: 12/05/2018
ms.keywords: WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TEMPLATE, WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TEMPLATE structure [Web Services for Windows], webservices/WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TEMPLATE, wsw.ws_tcp_sspi_transport_security_binding_template
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
req.typenames: WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TEMPLATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TEMPLATE
 - webservices/_WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TEMPLATE
 - WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TEMPLATE
 - webservices/WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TEMPLATE
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
 - WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TEMPLATE
---

# WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TEMPLATE structure


## -description

The security binding template for specifying the use of Windows SSPI
        protocol based transport security. 
      

See also <a href="/windows/desktop/api/webservices/ns-webservices-ws_tcp_sspi_transport_security_binding">WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING</a>.

## -struct-fields

### -field securityBindingProperties

Application provided security binding properties that cannot be represented in policy.

### -field clientCredential

The Windows credential to be used to obtain this security token.  This
          is required on the client and must not be specified on the server.