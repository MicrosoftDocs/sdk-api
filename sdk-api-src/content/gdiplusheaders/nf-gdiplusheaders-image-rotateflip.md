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

# Image::RotateFlip


## -description


The <b>Image::RotateFlip</b> method rotates and flips this image.


## -parameters




### -param rotateFlipType [in]

Type: <b><a href="https://msdn.microsoft.com/60fb3966-7313-4421-abd8-f437b521ac08">RotateFlipType</a></b>

Element of the <a href="https://msdn.microsoft.com/60fb3966-7313-4421-abd8-f437b521ac08">RotateFlipType</a> enumeration that specifies the type of rotation and the type of flip. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/60fb3966-7313-4421-abd8-f437b521ac08">RotateFlipType</a>



<a href="https://msdn.microsoft.com/1e982d84-8749-451b-89a8-81440fcee439">Rotating, Reflecting, and Skewing Images</a>
 

 

