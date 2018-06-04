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

# GetBitmapBits function


## -description


The <b>GetBitmapBits</b> function copies the bitmap bits of a specified device-dependent bitmap into a buffer.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. Applications should use the <a href="https://msdn.microsoft.com/be3ffa3f-b343-4e38-8b1e-aeccf35d92b8">GetDIBits</a> function.</div><div> </div>

## -parameters




### -param hbit

TBD


### -param cb

TBD


### -param lpvBits [out]

A pointer to a buffer to receive the bitmap bits. The bits are stored as an array of byte values.


#### - cbBuffer [in]

The number of bytes to copy from the bitmap into the buffer.


#### - hbmp [in]

A handle to the device-dependent bitmap.


## -returns



If the function succeeds, the return value is the number of bytes copied to the buffer.

If the function fails, the return value is zero.




## -see-also




<a href="https://msdn.microsoft.com/ef3abc8a-5d95-41d0-8eb6-47719d472414">Bitmap Functions</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>
 

 

