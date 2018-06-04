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

# WS_REQUEST_SECURITY_TOKEN_ACTION enumeration


## -description



        Defines which set of actions to use when negotiating security tokens using WS-Trust.
      


## -enum-fields




### -field WS_REQUEST_SECURITY_TOKEN_ACTION_ISSUE


          Use the "request" action defined in WS-Trust.
        


### -field WS_REQUEST_SECURITY_TOKEN_ACTION_NEW_CONTEXT


          Use the "request" action defined in WS-SecureConversation.
        


### -field WS_REQUEST_SECURITY_TOKEN_ACTION_RENEW_CONTEXT


          Use the "renew" action defined in WS-SecureConversation. Requires <a href="https://msdn.microsoft.com/7a2063eb-ab60-43d5-bd8c-41ef132abf50">WS_REQUEST_SECURITY_TOKEN_PROPERTY_EXISTING_TOKEN</a>.
        

