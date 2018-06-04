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

# _WS_USERNAME_MESSAGE_SECURITY_BINDING_TEMPLATE structure


## -description



        The security binding template for specifying the use of an application
        supplied username / password pair as a direct (i.e., one-shot)
        security token.  This security binding may be used only with message
        security.  It provides client authentication, but not traffic signing
        or encryption.  So, it is used in conjunction with another transport
        security or message security binding that provides message protection.
      

See also <a href="https://msdn.microsoft.com/be6d4787-fa50-4260-8236-39dd992adcae">WS_USERNAME_MESSAGE_SECURITY_BINDING</a>



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
        

