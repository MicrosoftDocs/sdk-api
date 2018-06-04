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

# _GAMMARAMP structure


## -description


The GAMMARAMP structure is used by <a href="https://msdn.microsoft.com/library/windows/hardware/ff556243">DrvIcmSetDeviceGammaRamp</a> to set the hardware <a href="https://msdn.microsoft.com/f67c673d-c6f0-49f0-850a-d8b00e99ddd4">gamma ramp</a> of a particular display device. 


## -struct-fields




### -field Red

Is the 256-entry ramp for the red color channel.


### -field Green

Is the 256-entry ramp for the green color channel.


### -field Blue

Is the 256-entry ramp for the blue color channel.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556243">DrvIcmSetDeviceGammaRamp</a>
 

 

