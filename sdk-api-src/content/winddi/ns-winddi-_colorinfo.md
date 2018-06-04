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

# _COLORINFO structure


## -description


The COLORINFO structure defines a device's colors in <a href="https://msdn.microsoft.com/ac439eb8-b491-4215-877d-5ee177fbdb39">CIE</a> coordinate space.


## -struct-fields




### -field Red


### -field Green


### -field Blue


### -field Cyan


### -field Magenta


### -field Yellow


### -field AlignmentWhite

Specify <a href="https://msdn.microsoft.com/library/windows/hardware/ff539399">CIECHROMA</a> structures that each define the x-coordinate, y-coordinate, and Y-coordinate (luminance) of the named color.

The <b>Cyan</b> member can have a special meaning for monochrome printers. <b>Cyan.Y</b> must be set to 65534 (0xFFFE) to enable all of the grayscale halftone pattern sizes. For more information, see the following Remarks section.


### -field RedGamma


### -field GreenGamma


### -field BlueGamma

Are the gamma corrections of display devices that permit the display device to display colors between the primary colors with accuracy. The values of these members should be in the range from 0 through 6.5535, which means that the numbers that are actually stored in these members must be in the range from 0 through 65535. For more information about these members and this data type, see the following Remarks section.


### -field MagentaInCyanDye


### -field YellowInCyanDye


### -field CyanInMagentaDye


### -field YellowInMagentaDye


### -field CyanInYellowDye


### -field MagentaInYellowDye

Used for printing devices to describe color purity and concentration. Values should be between zero and one, which means that the numbers actually stored in these members must be in the range 0 through 10000. For more information about this data type, see the following Remarks section.


## -remarks



The LDECI4 type is used to represent real numbers to four decimal places. For example, (LDECI4) 10000 represents the real number 1.0000, and (LDECI4) -12345 represents -1.2345.

For a monochrome printer, if you set the luminance for the <b>Cyan</b> member (that is, <b>Cyan.Y</b>) to 65534 (0xFFFE), you can select any of the available halftone pattern sizes. To select a halftone pattern size for a monochrome printer, set the <b>ulHTPatternSize</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff566484">GDIINFO</a> structure to the halftone pattern size that you want. If <b>Cyan.Y</b> is not set to 65534 (0xFFFE), halftone pattern sizes other than HT_PATSIZE_8x8_M or HT_PATSIZE_8x8 are converted to HT_PATSIZE_DEFAULT.

Setting the <b>RedGamma</b>, <b>BlueGamma</b>, and <b>GreenGamma</b> members of this structure to 0xFFFF can affect color management in printers when <a href="https://msdn.microsoft.com/c5b575c1-3ee7-4ad4-85e8-e1a6dbe34a5b">Image Color Management</a> (ICM) is disabled. In this situation, the GDI halftone module switches from performing its own color management to performing none, which potentially can cause a significant change in the resulting printer output. When ICM is enabled (and <b>RedGamma</b>, <b>BlueGamma</b>, and <b>GreenGamma</b> are set to 0XFFFF), there is no difference in color output. For more information, see <a href="https://msdn.microsoft.com/b83a46b3-57cb-463f-9a57-64a9b73035e2">Color Management for Printers</a>.

Any values in the COLORINFO structure that are out of the specified range default to the NTSC values.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff539399">CIECHROMA</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566484">GDIINFO</a>
 

 

