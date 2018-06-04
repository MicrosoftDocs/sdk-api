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

# SetBitmapBits function


## -description


The <b>SetBitmapBits</b> function sets the bits of color data for a bitmap to the specified values.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. Applications should use the <a href="https://msdn.microsoft.com/706f4532-4073-4d5c-ae2d-e33aea9163e9">SetDIBits</a> function.</div><div> </div>

## -parameters




### -param hbm

TBD


### -param cb

TBD


### -param pvBits

TBD




#### - cBytes [in]

The number of bytes pointed to by the <i>lpBits</i> parameter.


#### - hbmp [in]

A handle to the bitmap to be set. This must be a compatible bitmap (DDB).


#### - lpBits [in]

A pointer to an array of bytes that contain color data for the specified bitmap.


## -returns



If the function succeeds, the return value is the number of bytes used in setting the bitmap bits.

If the function fails, the return value is zero.




## -remarks



The array identified by <i>lpBits</i> must be WORD aligned.




## -see-also




<a href="https://msdn.microsoft.com/ef3abc8a-5d95-41d0-8eb6-47719d472414">Bitmap Functions</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/72e8cc6b-d282-451e-b6ec-0473d2daea7c">GetBitmapBits</a>



<a href="https://msdn.microsoft.com/706f4532-4073-4d5c-ae2d-e33aea9163e9">SetDIBits</a>
 

 

