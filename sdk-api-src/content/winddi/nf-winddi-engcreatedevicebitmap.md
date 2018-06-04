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

# EngCreateDeviceBitmap function


## -description


The <b>EngCreateDeviceBitmap</b> function requests GDI to create a handle for a device bitmap.


## -parameters




### -param dhsurf [in]

Device handle to the device bitmap to be created.


### -param sizl [in]

Specifies a SIZEL structure that contains the width and height of the bitmap to be created. The <b>cx</b> and <b>cy</b> members of this structure contain respectively, the bitmap's width and height, in pixels. A SIZEL structure is identical to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">SIZE</a> structure.


### -param iFormatCompat

Specifies the compatible engine format of the device surface being created. This is used by GDI if a temporary buffer is needed to simulate a complicated drawing call. The allowable values for <i>iFormatCompat</i> are BMF_1BPP, BMF_4BPP, BMF_8BPP, BMF_16BPP, BMF_24BPP, and BMF_32BPP.


## -returns



The return value is a handle that identifies the bitmap if the function is successful. Otherwise, it is zero, and an error code is logged.




## -remarks



The surface should be associated by using <a href="https://msdn.microsoft.com/library/windows/hardware/ff564183">EngAssociateSurface</a>. The bitmap should be deleted by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff564827">EngDeleteSurface</a> when it is no longer needed.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564199">EngCreateBitmap</a>
 

 

