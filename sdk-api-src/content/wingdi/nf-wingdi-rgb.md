---
UID: NF:wingdi.RGB
title: RGB macro
author: windows-sdk-content
description: The RGB macro selects a red, green, blue (RGB) color based on the arguments supplied and the color capabilities of the output device.
old-location: gdi\rgb.htm
old-project: gdi
ms.assetid: e1dcb5f8-c026-4a4e-8541-928a057bf0ae
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: RGB, RGB macro [Windows GDI], _win32_RGB, gdi.rgb, wingdi/RGB
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: wingdi.h
req.include-header: Windows.h
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
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wingdi.h
api_name:
-	RGB
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# RGB macro


## -description



The <b>RGB</b> macro selects a red, green, blue (RGB) color based on the arguments supplied and the color capabilities of the output device.




## -parameters




### -param r

TBD


### -param g

TBD


### -param b

TBD






#### - byBlue

The intensity of the blue color.


#### - byGreen

The intensity of the green color.


#### - byRed

The intensity of the red color.


## -remarks



The intensity for each argument is in the range 0 through 255. If all three intensities are zero, the result is black. If all three intensities are 255, the result is white.

To extract the individual values for the red, green, and blue components of a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> color value, use the <a href="https://msdn.microsoft.com/c183b671-20f8-468c-af0d-9f03cbc4b170">GetRValue</a>, <a href="https://msdn.microsoft.com/be989b36-8acb-435b-8d71-1c388c7884f0">GetGValue</a>, and <a href="https://msdn.microsoft.com/97e2644c-5298-4dea-b35a-fc0e2c74f9c8">GetBValue</a> macros, respectively.

When creating or examining a logical palette, use the <a href="https://msdn.microsoft.com/22e0991d-078e-4b44-9f03-004137e31f6c">RGBQUAD</a> structure to define color values and examine individual component values. For more information about using color values in a color palette, see the descriptions of the <a href="https://msdn.microsoft.com/76d859fa-11a5-451f-9d7a-9cf0740eca36">PALETTEINDEX</a> and <a href="https://msdn.microsoft.com/affe6d0f-2827-4de1-a21e-8fdcdad85fc5">PALETTERGB</a> macros.




## -see-also




<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



<a href="https://msdn.microsoft.com/f5bded0f-5f55-4512-9c00-9a9eb08c39f0">Color Macros</a>



<a href="https://msdn.microsoft.com/d1a25f13-6b47-4be7-927b-814dd6ae81f8">Colors Overview</a>



<a href="https://msdn.microsoft.com/97e2644c-5298-4dea-b35a-fc0e2c74f9c8">GetBValue</a>



<a href="https://msdn.microsoft.com/be989b36-8acb-435b-8d71-1c388c7884f0">GetGValue</a>



<a href="https://msdn.microsoft.com/c183b671-20f8-468c-af0d-9f03cbc4b170">GetRValue</a>



<a href="https://msdn.microsoft.com/76d859fa-11a5-451f-9d7a-9cf0740eca36">PALETTEINDEX</a>



<a href="https://msdn.microsoft.com/affe6d0f-2827-4de1-a21e-8fdcdad85fc5">PALETTERGB</a>



<a href="https://msdn.microsoft.com/22e0991d-078e-4b44-9f03-004137e31f6c">RGBQUAD</a>
 

 

