---
UID: NF:winddi.DrvIcmCheckBitmapBits
title: DrvIcmCheckBitmapBits function
author: windows-sdk-content
description: The DrvIcmCheckBitmapBits function checks whether the pixels in the specified bitmap lie within the device gamut of the specified transform.
old-location: display\drvicmcheckbitmapbits.htm
tech.root: display
ms.assetid: afde9270-3bbf-4f78-97ca-20ddfae83a2d
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: DrvIcmCheckBitmapBits, DrvIcmCheckBitmapBits function [Display Devices], ddifncs_f7d444c6-446a-4c46-9f5e-73407323c2d7.xml, display.drvicmcheckbitmapbits, winddi/DrvIcmCheckBitmapBits
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Desktop
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvIcmCheckBitmapBits
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrvIcmCheckBitmapBits function


## -description


The <b>DrvIcmCheckBitmapBits</b> function checks whether the pixels in the specified bitmap lie within the device gamut of the specified transform.


## -parameters




### -param dhpdev

Handle to the physical device's <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a>.


### -param hColorTransform

Handle to the color transform against which the bitmap is to be checked. This transform was created by the driver through a prior call to its <a href="https://msdn.microsoft.com/a4fda665-ba26-4799-820d-c4d82a58d6fd">DrvIcmCreateColorTransform</a> routine.


### -param pso

Pointer to the <a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a> that contains the bitmap surface to be checked.


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
 

<b>DrvIcmCheckBitmapBits</b> can be optionally implemented in drivers that support ICM. A driver indicates support for ICM by setting the GCAPS_ICM flag in the <b>flGraphicsCaps</b> member of the <a href="https://msdn.microsoft.com/5ba3e521-2e70-4a5b-979d-30a061275d42">DEVINFO</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/a4fda665-ba26-4799-820d-c4d82a58d6fd">DrvIcmCreateColorTransform</a>
 

 

