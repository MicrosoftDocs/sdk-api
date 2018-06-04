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

# DrvCreateDeviceBitmap function


## -description


The <b>DrvCreateDeviceBitmap</b> function creates and manages bitmaps. 


## -parameters




### -param dhpdev

Handle to the PDEV that describes the physical device that an application has designated as the primary target for a bitmap. The format of the bitmap must be compatible with this physical device.


### -param sizl

Specifies a SIZEL structure that contains the width and height of the bitmap to be created. The <b>cx</b> and <b>cy</b> members of this structure contain respectively, the bitmap's width and height, in pixels. A SIZEL structure is identical to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">SIZE</a> structure.


### -param iFormat

Specifies the bitmap format, which indicates the required number of bits of color information per pixel, and always matches the format of the primary. This value can be one of the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
BMF_8BPP

</td>
<td>
8 bits per pixel.

</td>
</tr>
<tr>
<td>
BMF_16BPP

</td>
<td>
16 bits per pixel.

</td>
</tr>
<tr>
<td>
BMF_24BPP

</td>
<td>
24 bits per pixel.

</td>
</tr>
<tr>
<td>
BMF_32BPP

</td>
<td>
32 bits per pixel.

</td>
</tr>
</table>
 


## -returns



The return value is a handle that identifies the created bitmap if the function is successful. If the driver chooses to let GDI create and manage the bitmap, the return value is zero. If an error occurs, the return value is 0xFFFFFFFF, and GDI logs an error code.




## -remarks



If the driver creates the bitmap, it can store it anywhere and in any format. It is assumed that the driver will take into account the specifications of the parameters and provide a bitmap with at least as many bits per pixel as requested.

The contents of the created bitmap are undefined.

This function is optional. If this function is implemented, however, <a href="https://msdn.microsoft.com/library/windows/hardware/ff556187">DrvDeleteDeviceBitmap</a> must also be implemented.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556187">DrvDeleteDeviceBitmap</a>
 

 

