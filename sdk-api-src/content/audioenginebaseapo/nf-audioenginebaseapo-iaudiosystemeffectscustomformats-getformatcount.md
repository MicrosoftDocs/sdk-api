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

# IAudioSystemEffectsCustomFormats::GetFormatCount


## -description


The <code>GetFormatCount</code> method retrieves the number of custom formats supported by the system effects audio processing object (sAPO).


## -parameters




### -param pcFormats [out]

Specifies a pointer to an unsigned integer. The unsigned integer represents the number of formats supported by the sAPO.


## -returns



The <code>GetFormatCount</code> method returns S_OK when the call is successful. Otherwise, it returns E_POINTER to indicate that an invalid pointer was passed to the function.




## -remarks



For more information about sAPOs, see <a href="https://msdn.microsoft.com/5275e404-19b9-4a44-88de-1a40f3798ede">System Effects Audio Processing Objects</a>.




## -see-also




<a href="https://msdn.microsoft.com/54ac63b4-9846-44ce-8afb-ded52ae2cd71">System Effects Audio Processing Objects</a>
 

 

