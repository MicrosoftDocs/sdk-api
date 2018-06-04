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

# EngMovePointer function


## -description


The <b>EngMovePointer</b> function moves the engine-managed pointer on the device.


## -parameters




### -param pso [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a> structure that describes the display device surface on which the pointer is to be moved.


### -param x [in]

Specify the x-coordinate on the display where the hot spot of the pointer should be positioned.

A negative <i>x</i> value indicates that the pointer should be removed from the display because drawing is about to occur at its present location. If the pointer has been removed from the display and the <i>x</i> value is nonnegative, the pointer should be restored.


### -param y [in]

Specify the y-coordinate on the display where the hot spot of the pointer should be positioned.


### -param prcl [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569236">RECTL</a> structure defining an area that bounds all pixels affected by the pointer on the display. The driver should pass the <i>prcl</i> parameter received by its <a href="https://msdn.microsoft.com/library/windows/hardware/ff556248">DrvMovePointer</a> function. GDI will not draw in this rectangle without first removing the pointer from the screen. This parameter can be <b>NULL</b>.


## -returns



None




## -remarks



<b>EngMovePointer</b> must not be called while any thread is drawing in the display driver.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552835">DEVINFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556248">DrvMovePointer</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565017">EngSetPointerShape</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a>
 

 

