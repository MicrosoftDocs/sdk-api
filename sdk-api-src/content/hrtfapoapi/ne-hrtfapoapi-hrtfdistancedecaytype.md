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

# HrtfDistanceDecayType enumeration


## -description


Indicates a distance-based decay type applied to a sound.


## -enum-fields




### -field NaturalDecay

Simulates natural decay with distance, as constrained by minimum and maximum gain distance limits. Drops to silence at rolloff distance. 


### -field CustomDecay

Used to set up a custom gain curve, within the maximum and minimum gain limit.  


## -see-also




<a href="https://msdn.microsoft.com/7b20bda9-dab2-cfbc-125a-cf46e4ede0c8">Enumerations</a>



<a href="https://msdn.microsoft.com/B488A674-91A7-41CB-9FF5-8270C6E941D2">HrtfDistanceDecay</a>
 

 

