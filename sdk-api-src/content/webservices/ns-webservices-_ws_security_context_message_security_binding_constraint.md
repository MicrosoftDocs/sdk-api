---
UID: NS:webservices._WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT
title: "_WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT"
author: windows-sdk-content
description: A security binding constraint that corresponds to the WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING.
old-location: wsw\ws_security_context_message_security_binding_constraint.htm
old-project: wsw
ms.assetid: 7abc37d8-cb00-459d-aa08-609a06b65a5c
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT, WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT structure [Web Services for Windows], _WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT, webservices/WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT, wsw.ws_security_context_message_security_binding_constraint
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING_CONSTRAINT structure


## -description



        A security binding constraint that corresponds to 
        the <a href="https://msdn.microsoft.com/c7f45f44-25e9-4124-a0a2-eb9969f0eb99">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING</a>.
      


## -struct-fields




### -field bindingConstraint


          The base binding constraint that this binding constraint derives from.
        


          The following binding constraints are supported at this point: <a href="https://msdn.microsoft.com/6c8b3277-3f49-469b-9783-c552a4c44558">WS_SECURITY_BINDING_PROPERTY_SECURE_CONVERSATION_VERSION</a> 
          and <b>WS_SECURITY_BINDING_PROPERTY_SECURITY_CONTEXT_KEY_ENTROPY_MODE</b>. 
           Currently only <a href="https://msdn.microsoft.com/17c21a3a-1cb5-4174-8300-a5c3d87e3e0f">WS_SECURE_CONVERSATION_VERSION_FEBRUARY_2005</a>
          is supported in policy, so a binding constraint containing the
          value <b>WS_SECURE_CONVERSATION_VERSION_FEBRUARY_2005</b> must be specified in
          order for the policy to match.
        


### -field bindingUsage


          This specifies how the security context token should be attached to a message.
        


### -field bootstrapSecurityConstraint


          This specifies the bootstrap security used to establish the secure conversation context.
        

