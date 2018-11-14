---
UID: NE:icm.COLORTYPE
title: COLORTYPE
author: windows-sdk-content
description: The values of the COLORTYPE enumeration are used by several WCS functions. Variables of type COLOR are defined in the color spaces enumerated by the COLORTYPE enumeration.
old-location: wcs\colortype.htm
tech.root: WCS
ms.assetid: 9735e4e5-362b-4542-9285-887279cc6499
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*PCOLORTYPE, COLORTYPE, COLORTYPE enumeration [Windows Color System], COLOR_3_CHANNEL, COLOR_5_CHANNEL, COLOR_6_CHANNEL, COLOR_7_CHANNEL, COLOR_8_CHANNEL, COLOR_CMYK, COLOR_GRAY, COLOR_Lab, COLOR_NAMED, COLOR_RGB, COLOR_XYZ, COLOR_Yxy, LPCOLORTYPE, LPCOLORTYPE enumeration pointer [Windows Color System], PCOLORTYPE, PCOLORTYPE enumeration pointer [Windows Color System], _color_COLORDATATYPE, icm/COLORTYPE, icm/COLOR_3_CHANNEL, icm/COLOR_5_CHANNEL, icm/COLOR_6_CHANNEL, icm/COLOR_7_CHANNEL, icm/COLOR_8_CHANNEL, icm/COLOR_CMYK, icm/COLOR_GRAY, icm/COLOR_Lab, icm/COLOR_NAMED, icm/COLOR_RGB, icm/COLOR_XYZ, icm/COLOR_Yxy, icm/LPCOLORTYPE, icm/PCOLORTYPE, wcs.colortype"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: icm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Icm.h
api_name:
 - COLORTYPE
product: Windows
targetos: Windows
req.typenames: COLORTYPE
req.redist: 
---

# COLORTYPE enumeration


## -description


The values of the <b>COLORTYPE</b> enumeration are used by several WCS functions. Variables of type <b>COLOR</b> are defined in the color spaces enumerated by the <b>COLORTYPE</b> enumeration.


## -enum-fields




### -field COLOR_GRAY

The <b>COLOR</b> is in the GRAYCOLOR color space.


### -field COLOR_RGB

The <b>COLOR</b> is in the RGBCOLOR color space.


### -field COLOR_XYZ

The <b>COLOR</b> is in the XYZCOLOR color space.


### -field COLOR_Yxy

The <b>COLOR</b> is in the YxyCOLOR color space.


### -field COLOR_Lab

The <b>COLOR</b> is in the LabCOLOR color space.


### -field COLOR_3_CHANNEL

The <b>COLOR</b> is in the GENERIC3CHANNEL color space.


### -field COLOR_CMYK

The <b>COLOR</b> is in the CMYKCOLOR color space.


### -field COLOR_5_CHANNEL

The <b>COLOR</b> is in a five channel color space.


### -field COLOR_6_CHANNEL

The <b>COLOR</b> is in a six channel color space.


### -field COLOR_7_CHANNEL

The <b>COLOR</b> is in a seven channel color space.


### -field COLOR_8_CHANNEL

The <b>COLOR</b> is in an eight channel color space.


### -field COLOR_NAMED

The <b>COLOR</b> is in a named color space.


## -remarks



In addition to managing the common two, three, and four channel color spaces, WCS 1.0 is able to perform color management with device profiles that contain five through eight <a href="c.htm">color channels</a>. It is also able to use named color spaces. When five, six, seven, or eight color channels are used, the provider of the device profile is free to determine what the color channels represent. The same is true of named color spaces. WCS 1.0 is able to manage these color spaces as long as there is a mapping in the device profile that maps the channels or the name space into the <a href="p.htm">PCS</a>. The device profile must also contain a mapping from the PCS into the five, size, seven, or eight channel space, or into the named color space.



