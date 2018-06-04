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

# tagCOLORADJUSTMENT structure


## -description



The <b>COLORADJUSTMENT</b> structure defines the color adjustment values used by the <a href="https://msdn.microsoft.com/5130c88e-08e8-4faa-a1cb-a8106c86cea0">StretchBlt</a> and <a href="https://msdn.microsoft.com/3d57a79a-338d-48ab-8161-3ce17739bf20">StretchDIBits</a> functions when the stretch mode is HALFTONE. You can set the color adjustment values by calling the <a href="https://msdn.microsoft.com/292d6cdc-cafa-438a-9392-a9c22e7d44a5">SetColorAdjustment</a> function.




## -struct-fields




### -field caSize

The size, in bytes, of the structure.


### -field caFlags

Specifies how the output image should be prepared. This member may be set to <b>NULL</b> or any combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>CA_NEGATIVE</td>
<td>Specifies that the negative of the original image should be displayed.</td>
</tr>
<tr>
<td>CA_LOG_FILTER</td>
<td>Specifies that a logarithmic function should be applied to the final density of the output colors. This will increase the color contrast when the luminance is low.</td>
</tr>
</table>
 


### -field caIlluminantIndex

The type of standard light source under which the image is viewed. This member may be set to one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>ILLUMINANT_DEVICE_DEFAULT</td>
<td>Device's default. Standard used by output devices.</td>
</tr>
<tr>
<td>ILLUMINANT_A</td>
<td>Tungsten lamp.</td>
</tr>
<tr>
<td>ILLUMINANT_B</td>
<td>Noon sunlight.</td>
</tr>
<tr>
<td>ILLUMINANT_C</td>
<td>NTSC daylight.</td>
</tr>
<tr>
<td>ILLUMINANT_D50</td>
<td>Normal print.</td>
</tr>
<tr>
<td>ILLUMINANT_D55</td>
<td>Bond paper print.</td>
</tr>
<tr>
<td>ILLUMINANT_D65</td>
<td>Standard daylight. Standard for CRTs and pictures.</td>
</tr>
<tr>
<td>ILLUMINANT_D75</td>
<td>Northern daylight.</td>
</tr>
<tr>
<td>ILLUMINANT_F2</td>
<td>Cool white lamp.</td>
</tr>
<tr>
<td>ILLUMINANT_TUNGSTEN</td>
<td>Same as ILLUMINANT_A.</td>
</tr>
<tr>
<td>ILLUMINANT_DAYLIGHT</td>
<td>Same as ILLUMINANT_C.</td>
</tr>
<tr>
<td>ILLUMINANT_FLUORESCENT</td>
<td>Same as ILLUMINANT_F2.</td>
</tr>
<tr>
<td>ILLUMINANT_NTSC</td>
<td>Same as ILLUMINANT_C.</td>
</tr>
</table>
 


### -field caRedGamma

Specifies the <i>n</i><sup>th</sup> power gamma-correction value for the red primary of the source colors. The value must be in the range from 2500 to 65,000. A value of 10,000 means no gamma correction.


### -field caGreenGamma

Specifies the <i>n</i><sup>th</sup> power gamma-correction value for the green primary of the source colors. The value must be in the range from 2500 to 65,000. A value of 10,000 means no gamma correction.


### -field caBlueGamma

Specifies the <i>n</i><sup>th</sup> power gamma-correction value for the blue primary of the source colors. The value must be in the range from 2500 to 65,000. A value of 10,000 means no gamma correction.


### -field caReferenceBlack

The black reference for the source colors. Any colors that are darker than this are treated as black. The value must be in the range from 0 to 4000.


### -field caReferenceWhite

The white reference for the source colors. Any colors that are lighter than this are treated as white. The value must be in the range from 6000 to 10,000.


### -field caContrast

The amount of contrast to be applied to the source object. The value must be in the range from -100 to 100. A value of 0 means no contrast adjustment.


### -field caBrightness

The amount of brightness to be applied to the source object. The value must be in the range from -100 to 100. A value of 0 means no brightness adjustment.


### -field caColorfulness

The amount of colorfulness to be applied to the source object. The value must be in the range from -100 to 100. A value of 0 means no colorfulness adjustment.


### -field caRedGreenTint

The amount of red or green tint adjustment to be applied to the source object. The value must be in the range from -100 to 100. Positive numbers adjust toward red and negative numbers adjust toward green. Zero means no tint adjustment.


## -see-also




<a href="https://msdn.microsoft.com/29f8237f-9c7e-41a7-90b1-5f048fcc74a6">Bitmap Structures</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/405c0d0d-9433-4f4a-9957-5c42a0fb3a07">
        GetColorAdjustment
      </a>



<a href="https://msdn.microsoft.com/292d6cdc-cafa-438a-9392-a9c22e7d44a5">
        SetColorAdjustment
      </a>



<a href="https://msdn.microsoft.com/3e5a48dc-ccd5-41ea-a24b-5c40213abf38">
        SetStretchBltMode
      </a>



<a href="https://msdn.microsoft.com/5130c88e-08e8-4faa-a1cb-a8106c86cea0">
        StretchBlt
      </a>



<a href="https://msdn.microsoft.com/3d57a79a-338d-48ab-8161-3ce17739bf20">
        StretchDIBits
      </a>
 

 

