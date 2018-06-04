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

# _XHR_CRED_PROMPT enumeration


## -description


Specifies whether to allow credential prompts to the user for authentication. 


## -enum-fields




### -field XHR_CRED_PROMPT_ALL

Allow all credential prompts for authentication. 

This setting allows credential prompts in response to requests from the proxy or the server.


### -field XHR_CRED_PROMPT_NONE

Disable all credential prompts for authentication. This setting disables any credential prompts in response to requests from the proxy or the server.


### -field XHR_CRED_PROMPT_PROXY

Allow credential prompts for authentication only in response to requests from the proxy.

This setting disables any credential prompts in response to requests from the server.


## -see-also




<a href="https://msdn.microsoft.com/4BBA4E21-29ED-413D-90D6-161D31CC13C9">SetProperty</a>
 

 

