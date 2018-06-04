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

# EngCreatePalette function


## -description


The <b>EngCreatePalette</b> function sends a request to GDI to create an RGB palette.


## -parameters




### -param iMode [in]

Specifies how the palette will be defined. This parameter can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
PAL_BITFIELDS

</td>
<td>
The palette is defined by the <i>flRed</i>, <i>flGreen</i>, and <i>flBlue</i> parameters.

</td>
</tr>
<tr>
<td>
PAL_BGR

</td>
<td>
The device accepts RGB colors directly, with B (blue) as the least significant byte.

</td>
</tr>
<tr>
<td>
PAL_CMYK

</td>
<td>
The device accepts CMYK colors directly, with C (cyan) as the least significant byte.

</td>
</tr>
<tr>
<td>
PAL_INDEXED

</td>
<td>
An array of RGB colors is provided with <i>cColors</i> and <i>pulColors</i>.

</td>
</tr>
<tr>
<td>
PAL_RGB

</td>
<td>
The device accepts RGB colors directly, with R (red) as the least significant byte.

</td>
</tr>
</table>
 


### -param cColors [in]

If the <i>iMode</i> parameter is PAL_INDEXED, <i>cColors</i> specifies the number of colors provided in the array pointed to by <i>pulColors</i>. Otherwise, this parameter should be zero.


### -param pulColors [in]

Pointer to the beginning of an array of ULONG values if <i>iMode</i> is PAL_INDEXED. The low-order 3 bytes of each ULONG define the RGB colors in the palette.


### -param flRed [in]

If the <i>iMode</i> parameter is PAL_BITFIELDS, the <i>flRed</i>, <i>flGreen</i> and <i>flBlue</i> parameters are masks that show which bits correspond to red, green, and blue. Each mask must consist of contiguous bits and should not overlap other masks. All combinations of bitfields are supported by GDI.


### -param flGreen [in]

If the <i>iMode</i> parameter is PAL_BITFIELDS, the <i>flRed</i>, <i>flGreen</i> and <i>flBlue</i> parameters are masks that show which bits correspond to red, green, and blue. Each mask must consist of contiguous bits and should not overlap other masks. All combinations of bitfields are supported by GDI.


### -param flBlue [in]

If the <i>iMode</i> parameter is PAL_BITFIELDS, the <i>flRed</i>, <i>flGreen</i> and <i>flBlue</i> parameters are masks that show which bits correspond to red, green, and blue. Each mask must consist of contiguous bits and should not overlap other masks. All combinations of bitfields are supported by GDI.


## -returns



The return value is a handle to the new palette if the function is successful. Otherwise, it is zero, and an error code is logged.




## -remarks



The driver can associate the new palette with a device by returning a pointer to the palette in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff552835">DEVINFO</a> structure.

A PAL_INDEXED palette associated with the device must have its first index entry set to black (red = 0, green = 0, blue = 0) and its last entry set to white (255, 255, 255). All other entries should be set so that entries whose indexes are one's complements of each other have colors that contrast greatly. For example, if entry 0x9 of a 16 entry palette is set to pure green (0,255,0), entry 0x6 (=~0x9) should be set to a color that contrasts well with green, such as dark purple (128,0,128). Setting entries in this way allows XOR raster operations to behave reasonably.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552835">DEVINFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556282">DrvSetPalette</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564808">EngDeletePalette</a>
 

 

