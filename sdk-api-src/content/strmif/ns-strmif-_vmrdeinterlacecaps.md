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

# _VMRDeinterlaceCaps structure


## -description



The <code>VMRDeinterlaceCaps</code> structure describes the capabilities of a deinterlacing mode.




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

Bitwise combination of flags from the <a href="https://msdn.microsoft.com/10149023-c5e8-4dce-8a8c-cde96ae6c073">VMRDeinterlaceTech</a> enumeration type. These flags are used to describe the deinterlacing algorithm.


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/77abbcd4-6538-491d-b3c2-6a29a391c68a">IVMRDeinterlaceControl Interface</a>
 

 

