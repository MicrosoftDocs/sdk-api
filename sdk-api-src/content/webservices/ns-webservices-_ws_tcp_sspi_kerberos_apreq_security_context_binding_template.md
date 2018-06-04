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

# _WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE structure


## -description



        Security template information to be filled in by application.
        Associated with <a href="https://msdn.microsoft.com/831001f4-619d-4128-a645-85077701c28c">WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE</a>.
      


## -struct-fields




### -field channelProperties


          Application provided additional channel properties for both bootstrap channel and service channel
          that cannot be represented in policy.
        


### -field securityProperties


          Application provided additional security properties for the bootstrap channel 
          that cannot be represented in policy.
        


### -field sspiTransportSecurityBinding


          Application provided SSPI transport security information for the bootstrap channel and service 
          channel that cannot be represented in policy.
        


### -field kerberosApreqMessageSecurityBinding


          Application provided kerberos binding information for the bootstrap channel that cannot be represented in policy.
        


### -field securityContextSecurityBinding


          Application provided security context message binding information for the service channel that cannot be represented in policy.
        

