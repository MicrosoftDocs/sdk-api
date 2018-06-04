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

# DrvIcmCheckBitmapBits function


## -description


The <b>DrvIcmCheckBitmapBits</b> function checks whether the pixels in the specified bitmap lie within the device gamut of the specified transform.


## -parameters




### -param dhpdev

Handle to the physical device's <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a>.


### -param hColorTransform

Handle to the color transform against which the bitmap is to be checked. This transform was created by the driver through a prior call to its <a href="https://msdn.microsoft.com/library/windows/hardware/ff556239">DrvIcmCreateColorTransform</a> routine.


### -param pso

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a> that contains the bitmap surface to be checked.


### -param paResults

Pointer to an array of bytes in which the driver returns the test results. GDI allocates this buffer to contain at least as many bytes as there are pixels in the bitmap. The driver need not perform any allocation or bound checking before writing to the array.


## -returns



<b>DrvIcmCheckBitmapBits</b> returns <b>TRUE</b> upon success. Otherwise, it reports an error and returns <b>FALSE</b>.




## -remarks



Each byte in the array to which <i>paResults</i> points corresponds with a pixel in the bitmap. For each pixel, the driver determines whether its color value is in the device gamut and then writes a value between zero and 255 in the corresponding array byte. The values have the following meanings:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
Zero

</td>
<td>
The color is in the device gamut.

</td>
</tr>
<tr>
<td>
Nonzero

</td>
<td>
The color is outside of the gamut. A value of <i>n+1</i> indicates that the color is at least as far out of the gamut as a value of <i>n</i>.

</td>
</tr>
</table>
 

<b>DrvIcmCheckBitmapBits</b> can be optionally implemented in drivers that support ICM. A driver indicates support for ICM by setting the GCAPS_ICM flag in the <b>flGraphicsCaps</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff552835">DEVINFO</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556239">DrvIcmCreateColorTransform</a>
 

 

