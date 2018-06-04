---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
        

