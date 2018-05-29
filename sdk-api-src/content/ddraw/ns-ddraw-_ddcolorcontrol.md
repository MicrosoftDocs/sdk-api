---
UID: NS:ddraw._DDCOLORCONTROL
title: "_DDCOLORCONTROL"
author: windows-sdk-content
description: The DDCOLORCONTROL structure defines the color controls that are associated with an overlay surface or a primary surface.
old-location: directdraw\ddcolorcontrol.htm
old-project: directdraw
ms.assetid: 69408101-9f19-4b89-bfcf-2af185c62807
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: "*LPDDCOLORCONTROL, DDCOLORCONTROL, DDCOLORCONTROL structure [DirectDraw], DDCOLOR_BRIGHTNESS, DDCOLOR_COLORENABLE, DDCOLOR_CONTRAST, DDCOLOR_GAMMA, DDCOLOR_HUE, DDCOLOR_SATURATION, DDCOLOR_SHARPNESS, LPDDCOLORCONTROL, LPDDCOLORCONTROL structure pointer [DirectDraw], _DDCOLORCONTROL, ddraw/DDCOLORCONTROL, ddraw/LPDDCOLORCONTROL, directdraw.ddcolorcontrol"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ddraw.h
req.include-header: 
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
req.typenames: "*LPDDCOLORCONTROL, DDCOLORCONTROL"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ddraw.h
api_name:
-	DDCOLORCONTROL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DDCOLORCONTROL structure


## -description


The <b>DDCOLORCONTROL</b> structure defines the color controls that are associated with an overlay surface or a primary surface.




## -struct-fields




### -field dwSize

Size of the structure, in bytes. This member must be initialized before the structure can be used.


### -field dwFlags

The following flags specifying which structure members contain valid data. When the structure is returned by the <a href="https://msdn.microsoft.com/16ac7bef-e88c-47da-8db9-9e6258a381a0">IDirectDrawColorControl::GetColorControls</a> method, it also indicates which options are supported by the device.



#### DDCOLOR_BRIGHTNESS

The <b>lBrightness</b> member contains valid data.



#### DDCOLOR_COLORENABLE

The <b>lColorEnable</b> member contains valid data.



#### DDCOLOR_CONTRAST

The <b>lContrast</b> member contains valid data.



#### DDCOLOR_GAMMA

The <b>lGamma</b> member contains valid data.



#### DDCOLOR_HUE

The <b>lHue</b> member contains valid data.



#### DDCOLOR_SATURATION

The <b>lSaturation</b> member contains valid data.



#### DDCOLOR_SHARPNESS

The <b>lSharpness</b> member contains valid data.


### -field lBrightness

Luminance intensity, in International Radio Engineers scale (IRE) units times 100. The valid range is from 0 through 10,000. The default is 750, which translates to 7.5 IRE.


### -field lContrast

Relative difference between higher and lower intensity luminance values in IRE units times 100. The valid range is from 0 through 20,000. The default value is 10,000 (100 IRE). Higher values of contrast cause darker luminance values to tend toward black and lighter luminance values to tend toward white. Lower values of contrast cause all luminance values to move toward the middle of the scale.


### -field lHue

Phase relationship of the chrominance components. Hue is specified in degrees, and the valid range is from –180 through 180, with a default of 0.


### -field lSaturation

Color intensity, in IRE units times 100. The valid range is from 0 through 20,000. The default value is 10,000, which translates to 100 IRE.


### -field lSharpness

Sharpness, in arbitrary units. The valid range is from 0 through 10, with a default of 5.


### -field lGamma

Controls the amount of gamma correction applied to the luminance values. The valid range is from 1 through 500 gamma units, with a default of 1.


### -field lColorEnable

Flag indicating whether color is used. If this member is 0, color is not used; if it is 1, color is used. The default value is 1.


### -field dwReserved1

Reserved

