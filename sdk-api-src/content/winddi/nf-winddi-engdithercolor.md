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

# EngDitherColor function


## -description


The <b>EngDitherColor</b> function returns a standard 8x8 dither that approximates the specified RGB color.


## -parameters




### -param hdev

Handle to the device. This is the handle that GDI passed to <a href="https://msdn.microsoft.com/library/windows/hardware/ff556181">DrvCompletePDEV</a>.


### -param iMode

Determines the palette that GDI should dither against. This parameter can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DM_DEFAULT

</td>
<td>
Requests that GDI create a dither for the native, default color space of the device. For example, if the device is running at 16bpp, the resulting dither is in a 16bpp format. 

</td>
</tr>
<tr>
<td>
DM_MONOCHROME

</td>
<td>
Requests that GDI create the dither for monochrome color space; that is, the dither is returned as a 1bpp bitmap.

</td>
</tr>
</table>
 


### -param rgb

Specifies the RGB color that is to be dithered. GDI ignores the high byte of this ULONG value.


### -param pul

Pointer to the memory location in which GDI returns the dithering information. The driver must have allocated memory for a standard-format bitmap with dithered brush dimensions of 8x8. The driver must also set the <b>cxDither</b> and <b>cyDither</b> members of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff552835">DEVINFO</a> structure to 8.


## -returns



The return value is DCR_DRIVER if the dither values have been calculated by the driver, or DCR_SOLID if the engine should use the best solid color approximation of the color. 




## -remarks



<b>EngDitherColor</b> can be called for bitmaps that are 8bpp or higher.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556273">DrvRealizeBrush</a>
 

 

