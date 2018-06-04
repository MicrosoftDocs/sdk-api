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

# EngCreateDeviceSurface function


## -description


The <b>EngCreateDeviceSurface</b> function creates and returns a handle for a device surface that the driver will manage.


## -parameters




### -param dhsurf [in]

Device handle to the surface to be managed by the device. This handle is passed to the driver when a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a> structure is passed for input or output.


### -param sizl [in]

Specifies a SIZEL structure that contains the width and height of the surface to be created. The <b>cx</b> and <b>cy</b> members of this structure contain respectively, the surface's width and height, in pixels. A SIZEL structure is identical to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">SIZE</a> structure.


### -param iFormatCompat

Specifies the compatible engine format of the device surface being created. This is used by GDI if a temporary buffer is needed to simulate a complicated drawing call.


## -returns



The return value is a handle that identifies the surface if the function is successful. Otherwise, it is zero, and an error code is logged.




## -remarks



The storage space for the surface can optionally be provided by the driver. The surface should be associated by using <a href="https://msdn.microsoft.com/library/windows/hardware/ff564183">EngAssociateSurface</a>. The surface should be deleted when it is no longer needed by using <a href="https://msdn.microsoft.com/library/windows/hardware/ff564827">EngDeleteSurface</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564183">EngAssociateSurface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564827">EngDeleteSurface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a>
 

 

