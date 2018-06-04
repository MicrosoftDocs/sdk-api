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

# IAudioEndpointOffloadStreamMeter::GetMeterChannelCount


## -description


Gets the number of available audio channels in the offloaded stream that can be metered.


## -parameters




### -param pu32ChannelCount [out]

A Pointer to a variable that indicates the number of available audio channels in the offloaded stream that can be metered.


## -returns



The <b>GetMeterChannelCount</b> method returns <b>S_OK</b> to indicate that it has completed successfully. Otherwise it returns an appropriate error code.




## -see-also




<a href="https://msdn.microsoft.com/B19413F9-1DE9-4940-B0A1-11E5278F084B">IAudioEndpointOffloadStreamMeter</a>
 

 

