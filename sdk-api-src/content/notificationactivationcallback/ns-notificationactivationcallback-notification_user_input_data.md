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

# NOTIFICATION_USER_INPUT_DATA structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Contains information about how a user interacted with a notification toast in the action center. This structure is used by <a href="https://msdn.microsoft.com/C366FE9F-D962-485F-B029-A96AA3358942">Activate</a>.


## -struct-fields




### -field Key

The ID of the user input field in the XML payload.


### -field Value

The input value selected by the user for a given input field.


## -remarks



Each key-value pair contains a piece of information based on an item in the notification toast when the <a href="https://msdn.microsoft.com/C366FE9F-D962-485F-B029-A96AA3358942">Activate</a> callback is triggered.




## -see-also




<a href="https://msdn.microsoft.com/050E6944-6727-4632-85E8-8E68887D4786">Respond to toast activations</a>
 

 

