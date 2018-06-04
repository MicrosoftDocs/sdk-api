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

# _VMR9DeinterlaceCaps structure


## -description



The <code>VMR9DeinterlaceCaps</code> structure describes the capabilities of a deinterlacing mode.




## -struct-fields




### -field dwSize

Size of the structure, in bytes.


### -field dwNumPreviousOutputFrames

Number of previously de-interlaced frames that must be fed back to the hardware to deinterlace the next field. (Used by recursive deinterlacing algorithms.)


### -field dwNumForwardRefSamples

Number of future samples needed to deinterlace the current field.


### -field dwNumBackwardRefSamples

Number of past samples needed to deinterlace the current field.


### -field DeinterlaceTechnology

Bitwise combination of flags from the <a href="https://msdn.microsoft.com/2b0b56b7-bab3-4184-a453-2da880aa38c9">VMR9DeinterlaceTech</a> enumeration type. These flags are used to describe the deinterlacing algorithm.


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

