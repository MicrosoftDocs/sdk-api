---
UID: NS:webservices._WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TEMPLATE
title: WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TEMPLATE (webservices.h)
description: The security binding template for specifying the use of HTP header authentication protocol based security.
helpviewer_keywords: ["WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TEMPLATE","WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TEMPLATE structure [Web Services for Windows]","webservices/WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TEMPLATE","wsw.ws_http_header_auth_security_binding_template"]
old-location: wsw\ws_http_header_auth_security_binding_template.htm
tech.root: wsw
ms.assetid: 4eabe380-de6d-48e3-bdad-dbf593a9850a
ms.date: 12/05/2018
ms.keywords: WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TEMPLATE, WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TEMPLATE structure [Web Services for Windows], webservices/WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TEMPLATE, wsw.ws_http_header_auth_security_binding_template
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
req.typenames: WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TEMPLATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TEMPLATE
 - webservices/_WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TEMPLATE
 - WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TEMPLATE
 - webservices/WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TEMPLATE
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
 - WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TEMPLATE
---

# WS_HTTP_HEADER_AUTH_SECURITY_BINDING_TEMPLATE structure


## -description

The security binding template for specifying the use of HTP header authentication 
        protocol based security.
      

See also <a href="/windows/desktop/api/webservices/ns-webservices-ws_http_header_auth_security_binding">WS_HTTP_HEADER_AUTH_SECURITY_BINDING</a>

## -struct-fields

### -field securityBindingProperties

Application provided security binding properties that cannot be represented in policy.

### -field clientCredential

The Windows credential to be used to obtain this security token.  This
          is required on the client side and must be <b>NULL</b> on the server side.