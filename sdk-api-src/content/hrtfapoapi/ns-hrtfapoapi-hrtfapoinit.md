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

# HrtfApoInit structure


## -description


Specifies parameters used to initialize HRTF spatial audio.


## -struct-fields




### -field distanceDecay

The decay type. If you pass in nullptr, the default value is used. The default is natural decay.


### -field directivity

The directivity type. If you pass in nullptr, the default value is used. The default directivity is omni-directional.


## -see-also




<a href="https://msdn.microsoft.com/24E3CD0D-FC0D-4B1B-961F-BE48935F7B71">CreateHrtfApo</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

