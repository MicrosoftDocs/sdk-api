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

# _WSD_EVENTING_EXPIRES structure


## -description


Represents the expiration time of a WS-Eventing message. 


## -struct-fields




### -field Duration

Reference to a <a href="https://msdn.microsoft.com/43d4d0c5-509a-46c4-bdf6-24c3307fb811">WSD_DURATION</a> structure that specifies the length of time a request or response is valid.


### -field DateTime

Reference to a <a href="https://msdn.microsoft.com/ec42d69c-133a-4e76-bbbe-0e6978f4723a">WSD_DATETIME</a> structure that specifies the time that the request or response expires. 

