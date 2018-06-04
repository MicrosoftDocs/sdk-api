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

# WICBitmapDitherType enumeration


## -description


Specifies the type of <a href="https://docs.microsoft.com/">dither</a> algorithm to apply when converting between image formats.


## -enum-fields




### -field WICBitmapDitherTypeNone

A solid color algorithm without dither.


### -field WICBitmapDitherTypeSolid

A solid color algorithm without dither.


### -field WICBitmapDitherTypeOrdered4x4

A 4x4 ordered dither algorithm. 


### -field WICBitmapDitherTypeOrdered8x8

An 8x8 ordered dither algorithm.


### -field WICBitmapDitherTypeOrdered16x16

A 16x16 ordered dither algorithm.


### -field WICBitmapDitherTypeSpiral4x4

A 4x4 spiral dither algorithm.


### -field WICBitmapDitherTypeSpiral8x8

An 8x8 spiral dither algorithm.


### -field WICBitmapDitherTypeDualSpiral4x4

A 4x4 dual spiral dither algorithm.


### -field WICBitmapDitherTypeDualSpiral8x8

An 8x8 dual spiral dither algorithm.


### -field WICBitmapDitherTypeErrorDiffusion

An error diffusion algorithm.


### -field WICBITMAPDITHERTYPE_FORCE_DWORD




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
 

 

