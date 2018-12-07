---
UID: NS:winddi._COLORINFO
title: "_COLORINFO"
author: windows-sdk-content
description: The COLORINFO structure defines a device's colors in CIE coordinate space.
old-location: display\colorinfo.htm
tech.root: display
ms.assetid: bbada28c-d855-4197-acf8-2a070423ddfe
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PCOLORINFO, COLORINFO, COLORINFO structure [Display Devices], PCOLORINFO, PCOLORINFO structure pointer [Display Devices], _COLORINFO, display.colorinfo, grstrcts_1e247041-c753-4925-a86c-fbd246410a72.xml, winddi/COLORINFO, winddi/PCOLORINFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Windows
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
 - COLORINFO
product: Windows
targetos: Windows
req.typenames: COLORINFO, *PCOLORINFO
req.redist: 
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

Specify <a href="https://msdn.microsoft.com/b8d1fd9b-c735-49f6-8d3b-12b5b1d92543">CIECHROMA</a> structures that each define the x-coordinate, y-coordinate, and Y-coordinate (luminance) of the named color.

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

For a monochrome printer, if you set the luminance for the <b>Cyan</b> member (that is, <b>Cyan.Y</b>) to 65534 (0xFFFE), you can select any of the available halftone pattern sizes. To select a halftone pattern size for a monochrome printer, set the <b>ulHTPatternSize</b> member of the <a href="https://msdn.microsoft.com/f75f599f-43ea-4da6-a6e3-6591cf6d69f1">GDIINFO</a> structure to the halftone pattern size that you want. If <b>Cyan.Y</b> is not set to 65534 (0xFFFE), halftone pattern sizes other than HT_PATSIZE_8x8_M or HT_PATSIZE_8x8 are converted to HT_PATSIZE_DEFAULT.

Setting the <b>RedGamma</b>, <b>BlueGamma</b>, and <b>GreenGamma</b> members of this structure to 0xFFFF can affect color management in printers when <a href="https://msdn.microsoft.com/c5b575c1-3ee7-4ad4-85e8-e1a6dbe34a5b">Image Color Management</a> (ICM) is disabled. In this situation, the GDI halftone module switches from performing its own color management to performing none, which potentially can cause a significant change in the resulting printer output. When ICM is enabled (and <b>RedGamma</b>, <b>BlueGamma</b>, and <b>GreenGamma</b> are set to 0XFFFF), there is no difference in color output. For more information, see <a href="https://msdn.microsoft.com/b83a46b3-57cb-463f-9a57-64a9b73035e2">Color Management for Printers</a>.

Any values in the COLORINFO structure that are out of the specified range default to the NTSC values.




## -see-also




<a href="https://msdn.microsoft.com/b8d1fd9b-c735-49f6-8d3b-12b5b1d92543">CIECHROMA</a>



<a href="https://msdn.microsoft.com/9a7ed18a-f21c-486b-9261-59a3fe5aef9e">DrvEnablePDEV</a>



<a href="https://msdn.microsoft.com/f75f599f-43ea-4da6-a6e3-6591cf6d69f1">GDIINFO</a>
 

 

