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

# _XLATEOBJ structure


## -description


The XLATEOBJ structure is used to translate color indexes from one palette to another.


## -struct-fields




### -field iUniq

A cache identifier that enables the driver to recognize an XLATEOBJ structure that it has previously cached. If this member is zero, the driver should not cache the XLATEOBJ structure.


### -field flXlate

Flags specifying hints about the translation. This member can be any combination of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
XO_DEVICE_ICM

</td>
<td>
ICM is enabled on the device. The driver should translate color according to the color transform created by <a href="https://msdn.microsoft.com/library/windows/hardware/ff556239">DrvIcmCreateColorTransform</a>. The driver should call <a href="https://msdn.microsoft.com/library/windows/hardware/ff570639">XLATEOBJ_hGetColorTransform</a> to get the color transform handle. This bit is mutually exclusive from XO_HOST_ICM.

</td>
</tr>
<tr>
<td>
XO_FROM_CMYK

</td>
<td>
As a result of ICM translation, source indices are translated to the 32-bit <a href="https://msdn.microsoft.com/ac439eb8-b491-4215-877d-5ee177fbdb39">CMYK</a> color format. When this bit is set, <b>iSrcType</b>, <b>iDstType</b>, <b>cEntries</b>, and <b>pulXlate</b> should be ignored.

</td>
</tr>
<tr>
<td>
XO_HOST_ICM

</td>
<td>
ICM is performed by the graphics engine, so the colors in this color table are corrected to the target surface. This bit is set by the GDI as information for the driver: no action is required by the driver. This bit is mutually exclusive from XO_DEVICE_ICM.

</td>
</tr>
<tr>
<td>
XO_TABLE

</td>
<td>
A table is provided to translate source indices to target indices.

</td>
</tr>
<tr>
<td>
XO_TO_MONO

</td>
<td>
Source indices are translated to a monochrome format with the special property that all indices map to zero, except for one. A driver can use this to accelerate a block transfer.

</td>
</tr>
<tr>
<td>
XO_TRIVIAL

</td>
<td>
Source indices are usable as target indices.

</td>
</tr>
</table>
 


### -field iSrcType

Is obsolete. Use <a href="https://msdn.microsoft.com/library/windows/hardware/ff570637">XLATEOBJ_cGetPalette</a> to query the source format.


### -field iDstType

Is obsolete. Use <a href="https://msdn.microsoft.com/library/windows/hardware/ff570637">XLATEOBJ_cGetPalette</a> to query the destination format.


### -field cEntries

Specifies the number of entries in the array pointed to by the <b>pulXlate</b> member. Indexing into <b>pulXlate</b> with a value greater than <b>cEntries</b> results in a memory access violation.


### -field pulXlate

Pointer to an array of translation entries.


## -remarks



The destination palette always belongs to the destination surface of some drawing operation. The source palette is an application-selected palette or a palette from another surface.

The XLATEOBJ structure is used to translate color indices that refer to the source palette to indices for the destination palette. The resulting index identifies a color that matches the source color as closely as possible.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556239">DrvIcmCreateColorTransform</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570637">XLATEOBJ_cGetPalette</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570639">XLATEOBJ_hGetColorTransform</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570644">XLATEOBJ_piVector</a>
 

 

