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

# _WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING_TEMPLATE structure


## -description



        The security binding template for specifying the use of the Kerberos
        AP_REQ ticket as a direct (i.e., without establishing a session)
        security token with WS-Security.
      

See also <a href="https://msdn.microsoft.com/03127248-f5cc-44da-9c3d-abf016dd6bb2">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING</a>



## -struct-fields




### -field securityBindingProperties


          Application provided security binding properties that cannot be represented in policy.
        


### -field clientCredential


          The Windows credential to be used to obtain the Kerberos ticket.  This
          field is required on the client side, but must be <b>NULL</b> on the server
          side.
        

