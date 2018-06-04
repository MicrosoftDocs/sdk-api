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

# PixelOffsetMode enumeration


## -description


The <b>PixelOffsetMode</b> enumeration specifies the pixel offset mode of a 
			<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object. This enumeration is used by the <a href="https://msdn.microsoft.com/9d379aad-8e0d-4e3f-bbff-a8b26d0efa15">Graphics::GetPixelOffsetMode</a> and <a href="https://msdn.microsoft.com/2e93a8b1-e44d-4bd9-86bc-4291719afe9c">Graphics::SetPixelOffsetMode</a> methods of the 
			<b>Graphics</b> class.


## -enum-fields




### -field PixelOffsetModeInvalid

Used internally. 


### -field PixelOffsetModeDefault

Equivalent to PixelOffsetModeNone. 


### -field PixelOffsetModeHighSpeed

Equivalent to PixelOffsetModeNone. 


### -field PixelOffsetModeHighQuality

Equivalent to PixelOffsetModeHalf. 


### -field PixelOffsetModeNone

Indicates that pixel centers have integer coordinates. 


### -field PixelOffsetModeHalf

Indicates that pixel centers have coordinates that are half way between integer values. 


## -remarks



Consider the pixel in the upper-left corner of an image with address (0, 0). With <b><b>PixelOffsetModeNone</b></b>, the pixel covers the area between 
				–0.5 and 0.5 in both the x and y directions; that is, the pixel center is at (0, 0). With <b><b>PixelOffsetModeHalf</b></b>, the pixel covers the area between 0 and 1 in both the x and y directions; that is, the pixel center is at (0.5, 0.5).




## -see-also




<a href="https://msdn.microsoft.com/9d379aad-8e0d-4e3f-bbff-a8b26d0efa15">Graphics::GetPixelOffsetMode</a>



<a href="https://msdn.microsoft.com/2e93a8b1-e44d-4bd9-86bc-4291719afe9c">Graphics::SetPixelOffsetMode</a>
 

 

