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

# SetBitmapDimensionEx function


## -description


The <b>SetBitmapDimensionEx</b> function assigns preferred dimensions to a bitmap. These dimensions can be used by applications; however, they are not used by the system.


## -parameters




### -param hbm

TBD


### -param w

TBD


### -param h

TBD


### -param lpsz

TBD




#### - hBitmap [in]

A handle to the bitmap. The bitmap cannot be a DIB-section bitmap.


#### - lpSize [out]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">SIZE</a> structure to receive the previous dimensions of the bitmap. This pointer can be <b>NULL</b>.


#### - nHeight [in]

The height, in 0.1-millimeter units, of the bitmap.


#### - nWidth [in]

The width, in 0.1-millimeter units, of the bitmap.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



An application can retrieve the dimensions assigned to a bitmap with the <b>SetBitmapDimensionEx</b> function by calling the <a href="https://msdn.microsoft.com/3e4f5afc-26d3-4fb2-8d00-183165fdf471">GetBitmapDimensionEx</a> function.

The bitmap identified by <i>hBitmap</i> cannot be a DIB section, which is a bitmap created by the <a href="https://msdn.microsoft.com/9276ec84-2860-42be-a9f8-d4efb8d25eec">CreateDIBSection</a> function. If the bitmap is a DIB section, the <b>SetBitmapDimensionEx</b> function fails.




## -see-also




<a href="https://msdn.microsoft.com/ef3abc8a-5d95-41d0-8eb6-47719d472414">Bitmap Functions</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/9276ec84-2860-42be-a9f8-d4efb8d25eec">CreateDIBSection</a>



<a href="https://msdn.microsoft.com/3e4f5afc-26d3-4fb2-8d00-183165fdf471">GetBitmapDimensionEx</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">SIZE</a>
 

 

