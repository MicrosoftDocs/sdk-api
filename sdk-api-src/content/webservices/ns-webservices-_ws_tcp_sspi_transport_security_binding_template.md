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

# _WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING_TEMPLATE structure


## -description



        The security binding template for specifying the use of Windows SSPI
        protocol based transport security. 
      


        See also <a href="https://msdn.microsoft.com/c617f6cf-cedb-4d52-954c-fd4577260ca3">WS_TCP_SSPI_TRANSPORT_SECURITY_BINDING</a>.
      


## -struct-fields




### -field securityBindingProperties


          Application provided security binding properties that cannot be represented in policy.
        


### -field clientCredential


          The Windows credential to be used to obtain this security token.  This
          is required on the client and must not be specified on the server.
        

