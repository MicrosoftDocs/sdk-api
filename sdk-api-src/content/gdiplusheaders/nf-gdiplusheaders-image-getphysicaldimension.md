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

# Image::GetPhysicalDimension


## -description


The <b>Image::GetPhysicalDimension</b> method gets the width and height of this image.


## -parameters




### -param size [out]

Type: <b><a href="https://msdn.microsoft.com/b40ade07-f89e-44ba-9185-9aec01f1051f">SizeF</a>*</b>

Pointer to a 
					<a href="https://msdn.microsoft.com/b40ade07-f89e-44ba-9185-9aec01f1051f">SizeF</a> object that receives the width and height of this image. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/81d20adc-0481-4b1b-80aa-ae218fdecd84">Cropping and Scaling Images</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/b94cee76-2e3d-4f78-96b3-ec898054bd6e">Image::GetBounds</a>



<a href="https://msdn.microsoft.com/a39deeae-e610-4468-ba93-1da5abaa00b8">Image::GetHeight</a>



<a href="https://msdn.microsoft.com/09e0d6d9-10b5-4319-8547-f13ca06cf0cd">Image::GetHorizontalResolution</a>



<a href="https://msdn.microsoft.com/8aa90120-479e-4fa7-b9d8-609fdf1912e7">Image::GetVerticalResolution</a>



<a href="https://msdn.microsoft.com/e55bc22d-e5c6-43c8-87f8-345d348e5707">Image::GetWidth</a>



<a href="https://msdn.microsoft.com/da571970-a4fc-4d4a-9264-0085d9807d66">Improving Performance by Avoiding Automatic Scaling</a>
 

 

