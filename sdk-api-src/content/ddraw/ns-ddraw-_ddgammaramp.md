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

# _DDGAMMARAMP structure


## -description


The <b>DDGAMMARAMP</b> structure contains red, green, and blue ramp data for the <a href="https://msdn.microsoft.com/ba83605c-c388-42c0-9297-1666c80a278e">IDirectDrawGammaControl::GetGammaRamp</a> and <a href="https://msdn.microsoft.com/3bde7ba7-8498-42e5-bd5a-625e162fc1db">IDirectDrawGammaControl::SetGammaRamp</a> methods.




## -struct-fields




### -field red

Array of 256 WORD elements that describe the red gamma ramp.


### -field green

Array of 256 WORD elements that describe the green gamma ramp.


### -field blue

Array of 256 WORD elements that describe the blue gamma ramp.

