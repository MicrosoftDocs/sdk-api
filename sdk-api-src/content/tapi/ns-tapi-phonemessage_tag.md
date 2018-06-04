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

# phonemessage_tag structure


## -description


The 
<b>PHONEMESSAGE</b> structure contains the next message queued for delivery to the application. The 
<a href="https://msdn.microsoft.com/8afa17ef-a47f-41af-b120-1e2d5acb4106">phoneGetMessage</a> function returns this structure.


## -struct-fields




### -field hDevice

Handle to a phone device.


### -field dwMessageID

Phone message.


### -field dwCallbackInstance

Instance data passed back to the application, which was specified by the application in 
<a href="https://msdn.microsoft.com/362e37df-4b14-4651-8d23-b70613e354c8">phoneInitializeEx</a>. This value is not interpreted by TAPI.


### -field dwParam1

Parameter for the message.


### -field dwParam2

Parameter for the message.


### -field dwParam3

Parameter for the message.


## -remarks



For information about parameter values passed in this structure, see 
<a href="https://msdn.microsoft.com/b84c77ae-5d0f-416c-83c5-f7874168d996">Phone Device Messages</a>.




## -see-also




<a href="https://msdn.microsoft.com/8afa17ef-a47f-41af-b120-1e2d5acb4106">phoneGetMessage</a>



<a href="https://msdn.microsoft.com/362e37df-4b14-4651-8d23-b70613e354c8">phoneInitializeEx</a>
 

 

