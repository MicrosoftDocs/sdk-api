---
UID: NS:webservices._WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT
title: WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT (webservices.h)
description: A security binding constraint that corresponds to the WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING.
helpviewer_keywords: ["WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT","WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT structure [Web Services for Windows]","webservices/WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT","wsw.ws_security_context_message_security_binding_constraint"]
old-location: wsw\ws_security_context_message_security_binding_constraint.htm
tech.root: wsw
ms.assetid: 7abc37d8-cb00-459d-aa08-609a06b65a5c
ms.date: 12/05/2018
ms.keywords: WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT, WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT structure [Web Services for Windows], webservices/WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT, wsw.ws_security_context_message_security_binding_constraint
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
req.typenames: WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT
 - webservices/_WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT
 - WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT
 - webservices/WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT
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
 - WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT
---

# WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT structure


## -description

A security binding constraint that corresponds to 
        the <a href="/windows/desktop/api/webservices/ns-webservices-ws_security_context_message_security_binding">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING</a>.

## -struct-fields

### -field bindingConstraint

The base binding constraint that this binding constraint derives from.
        

The following binding constraints are supported at this point: <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_binding_property_id">WS_SECURITY_BINDING_PROPERTY_SECURE_CONVERSATION_VERSION</a> 
          and <b>WS_SECURITY_BINDING_PROPERTY_SECURITY_CONTEXT_KEY_ENTROPY_MODE</b>. 
           Currently only <a href="/windows/desktop/api/webservices/ne-webservices-ws_secure_conversation_version">WS_SECURE_CONVERSATION_VERSION_FEBRUARY_2005</a> is supported in policy, so a binding constraint containing the
          value <b>WS_SECURE_CONVERSATION_VERSION_FEBRUARY_2005</b> must be specified in
          order for the policy to match.

### -field bindingUsage

This specifies how the security context token should be attached to a message.

### -field bootstrapSecurityConstraint

This specifies the bootstrap security used to establish the secure conversation context.