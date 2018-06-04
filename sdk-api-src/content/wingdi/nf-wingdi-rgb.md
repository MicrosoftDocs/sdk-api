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
 

 

