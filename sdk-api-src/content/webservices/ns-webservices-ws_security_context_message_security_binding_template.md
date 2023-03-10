---
UID: NS:webservices._WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_TEMPLATE
title: WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_TEMPLATE (webservices.h)
description: The security binding template for specifying the use of an application supplied security context security binding. (WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_TEMPLATE)
helpviewer_keywords: ["WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_TEMPLATE","WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_TEMPLATE structure [Web Services for Windows]","webservices/WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_TEMPLATE","wsw.ws_security_context_message_security_binding_template"]
old-location: wsw\ws_security_context_message_security_binding_template.htm
tech.root: wsw
ms.assetid: 87944c01-7a8c-4029-a6ea-605b8bb84e3e
ms.date: 12/05/2018
ms.keywords: WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_TEMPLATE, WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_TEMPLATE structure [Web Services for Windows], webservices/WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_TEMPLATE, wsw.ws_security_context_message_security_binding_template
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
req.typenames: WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_TEMPLATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_TEMPLATE
 - webservices/_WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_TEMPLATE
 - WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_TEMPLATE
 - webservices/WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_TEMPLATE
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
 - WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_TEMPLATE
---

# WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_TEMPLATE structure


## -description

The security binding template for specifying the use of an application
        supplied security context security binding.  This security binding may 
        be used only with message security. So, it is used in conjunction with another transport
        security or message security binding that provides message protection.
      

See also <a href="/windows/desktop/api/webservices/ns-webservices-ws_security_context_message_security_binding">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING</a>

## -struct-fields

### -field securityBindingProperties

Application provided security binding properties that cannot be represented in policy.
