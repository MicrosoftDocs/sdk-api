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

# _EAP_AUTHENTICATOR_SEND_TIMEOUT enumeration


## -description


Indicates to the authenticator method the amount of time to wait for user input after the packet is sent. The timeout value can be set to none.


## -enum-fields




### -field EAP_AUTHENTICATOR_SEND_TIMEOUT_NONE

 Sends the packet and never times out; the user can enter a response at any time. 


### -field EAP_AUTHENTICATOR_SEND_TIMEOUT_BASIC

Sends the packet and waits for a standard period of time for a response.


### -field EAP_AUTHENTICATOR_SEND_TIMEOUT_INTERACTIVE

Sends the packet and waits for a response for a longer period of time to allow for an interactive session.


## -see-also




<a href="https://msdn.microsoft.com/8c21625f-a9b7-4ea5-98ff-cdcce637dad8">EAPHost Authenticator Method Enumerations</a>
 

 

