---
UID: NS:webservices._WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_TEMPLATE
title: WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_TEMPLATE (webservices.h)
description: The security binding template for specifying the use of the Kerberos AP_REQ ticket as a direct (i.e., without establishing a session) security token with WS-Security.
helpviewer_keywords: ["WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_TEMPLATE","WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_TEMPLATE structure [Web Services for Windows]","webservices/WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_TEMPLATE","wsw.ws_kerberos_apreq_message_security_binding_template"]
old-location: wsw\ws_kerberos_apreq_message_security_binding_template.htm
tech.root: wsw
ms.assetid: 7dabbc5e-2953-43dc-8ee9-e4ac3114c85a
ms.date: 12/05/2018
ms.keywords: WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_TEMPLATE, WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_TEMPLATE structure [Web Services for Windows], webservices/WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_TEMPLATE, wsw.ws_kerberos_apreq_message_security_binding_template
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
req.typenames: WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_TEMPLATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_TEMPLATE
 - webservices/_WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_TEMPLATE
 - WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_TEMPLATE
 - webservices/WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_TEMPLATE
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
 - WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_TEMPLATE
---

# WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_TEMPLATE structure


## -description

The security binding template for specifying the use of the Kerberos
        AP_REQ ticket as a direct (i.e., without establishing a session)
        security token with WS-Security.
      

See also <a href="/windows/desktop/api/webservices/ns-webservices-ws_kerberos_apreq_message_security_binding">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING</a>

## -struct-fields

### -field securityBindingProperties

Application provided security binding properties that cannot be represented in policy.

### -field clientCredential

The Windows credential to be used to obtain the Kerberos ticket.  This
          field is required on the client side, but must be <b>NULL</b> on the server
          side.