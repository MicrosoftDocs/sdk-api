---
UID: NF:winddi.EngDitherColor
title: EngDitherColor function
author: windows-sdk-content
description: The EngDitherColor function returns a standard 8x8 dither that approximates the specified RGB color.
old-location: display\engdithercolor.htm
tech.root: display
ms.assetid: 6c45fd2a-3bba-4e41-a1ee-b3b10602b65a
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: EngDitherColor, EngDitherColor function [Display Devices], display.engdithercolor, gdifncs_99024e1a-c511-4b02-80dc-e39dd82a8d57.xml, winddi/EngDitherColor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngDitherColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EngDitherColor function


## -description


The <b>EngDitherColor</b> function returns a standard 8x8 dither that approximates the specified RGB color.


## -parameters




### -param hdev

Handle to the device. This is the handle that GDI passed to <a href="https://msdn.microsoft.com/6343c6cc-f2f3-4776-a747-7a5b5cebef5f">DrvCompletePDEV</a>.


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

Pointer to the memory location in which GDI returns the dithering information. The driver must have allocated memory for a standard-format bitmap with dithered brush dimensions of 8x8. The driver must also set the <b>cxDither</b> and <b>cyDither</b> members of the <a href="https://msdn.microsoft.com/5ba3e521-2e70-4a5b-979d-30a061275d42">DEVINFO</a> structure to 8.


## -returns



The return value is DCR_DRIVER if the dither values have been calculated by the driver, or DCR_SOLID if the engine should use the best solid color approximation of the color. 




## -remarks



<b>EngDitherColor</b> can be called for bitmaps that are 8bpp or higher.




## -see-also




<a href="https://msdn.microsoft.com/2948f274-cef2-4fcf-9607-79540b6e5a5f">DrvRealizeBrush</a>
 

 

