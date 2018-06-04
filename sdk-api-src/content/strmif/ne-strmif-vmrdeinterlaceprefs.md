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

# VMRDeinterlacePrefs enumeration


## -description


The <b>VMRDeinterlacePrefs</b> enumeration type describes the deinterlacing method that the <a href="https://msdn.microsoft.com/c83e6c50-76f2-4aeb-944b-5b244c6bf776">Video Mixing Renderer Filter 7</a> (VMR-7) uses if the method set by the application cannot be used.


## -enum-fields




### -field DeinterlacePref_NextBest


            Use the next best mode offered by the driver.
          


### -field DeinterlacePref_BOB


            Use the bob method.
          


### -field DeinterlacePref_Weave


            Use the weave method (that is, no deinterlacing).
          


### -field DeinterlacePref_Mask


            Bitwise <b>OR</b> of the previous flags. This value is not a valid flag.
          


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/77abbcd4-6538-491d-b3c2-6a29a391c68a">IVMRDeinterlaceControl Interface</a>
 

 

