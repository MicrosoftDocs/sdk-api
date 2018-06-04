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

# _WS_SECURITY_CONTEXT_SECURITY_BINDING_TEMPLATE structure


## -description



        The security binding template for specifying the use of an application
        supplied security context security binding.  This security binding may 
        be used only with message security. So, it is used in conjunction with another transport
        security binding that provides message protection. The security properties are 
        used to establish the secure conversation.
      


        See also <a href="https://msdn.microsoft.com/c7f45f44-25e9-4124-a0a2-eb9969f0eb99">WS_SECURITY_CONTEXT_MESSAGE_SECURITY_BINDING</a>



## -struct-fields




### -field securityContextMessageSecurityBinding


          Application provided security binding properties that cannot be represented in policy.
        


### -field securityProperties


          Application provided additional security properties for the service channel
          that cannot be represented in policy. Only policy specified security properties is used if no additional properties are specified here.
        

