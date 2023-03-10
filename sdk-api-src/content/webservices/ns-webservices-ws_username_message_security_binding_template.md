---
UID: NS:webservices._WS_USERNAME_MESSAGE_SECURITY_BINDING_TEMPLATE
title: WS_USERNAME_MESSAGE_SECURITY_BINDING_TEMPLATE (webservices.h)
description: The security binding template for specifying the use of an application supplied username / password pair as a direct (i.e., one-shot) security token.
helpviewer_keywords: ["WS_USERNAME_MESSAGE_SECURITY_BINDING_TEMPLATE","WS_USERNAME_MESSAGE_SECURITY_BINDING_TEMPLATE structure [Web Services for Windows]","webservices/WS_USERNAME_MESSAGE_SECURITY_BINDING_TEMPLATE","wsw.ws_username_message_security_binding_template"]
old-location: wsw\ws_username_message_security_binding_template.htm
tech.root: wsw
ms.assetid: c538c670-9a61-4891-9f63-e0eea12ee224
ms.date: 12/05/2018
ms.keywords: WS_USERNAME_MESSAGE_SECURITY_BINDING_TEMPLATE, WS_USERNAME_MESSAGE_SECURITY_BINDING_TEMPLATE structure [Web Services for Windows], webservices/WS_USERNAME_MESSAGE_SECURITY_BINDING_TEMPLATE, wsw.ws_username_message_security_binding_template
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
req.typenames: WS_USERNAME_MESSAGE_SECURITY_BINDING_TEMPLATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_USERNAME_MESSAGE_SECURITY_BINDING_TEMPLATE
 - webservices/_WS_USERNAME_MESSAGE_SECURITY_BINDING_TEMPLATE
 - WS_USERNAME_MESSAGE_SECURITY_BINDING_TEMPLATE
 - webservices/WS_USERNAME_MESSAGE_SECURITY_BINDING_TEMPLATE
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
 - WS_USERNAME_MESSAGE_SECURITY_BINDING_TEMPLATE
---

# WS_USERNAME_MESSAGE_SECURITY_BINDING_TEMPLATE structure


## -description

The security binding template for specifying the use of an application
        supplied username / password pair as a direct (i.e., one-shot)
        security token.  This security binding may be used only with message
        security.  It provides client authentication, but not traffic signing
        or encryption.  So, it is used in conjunction with another transport
        security or message security binding that provides message protection.
      

See also <a href="/windows/desktop/api/webservices/ns-webservices-ws_username_message_security_binding">WS_USERNAME_MESSAGE_SECURITY_BINDING</a>

## -struct-fields

### -field securityBindingProperties

Application provided security binding properties that cannot be represented in policy.

### -field clientCredential

The username credential to be used with this security binding.  This
          needs to be specified when this security binding is used on the
          client.

### -field passwordValidator

The validator to be used to check received username/password pairs.
          This needs to be specified when this security binding is used on the
          service.

### -field passwordValidatorCallbackState

The optional state to be passed in as an argument when the username validator is invoked.