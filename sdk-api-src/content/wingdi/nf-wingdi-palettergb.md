---
UID: NF:wingdi.PALETTERGB
title: PALETTERGB macro
author: windows-sdk-content
description: The PALETTERGB macro accepts three values that represent the relative intensities of red, green, and blue and returns a palette-relative red, green, blue (RGB) specifier consisting of 2 in the high-order byte and an RGB value in the three low-order bytes. An application using a color palette can pass this specifier, instead of an explicit RGB value, to functions that expect a color.
old-location: gdi\palettergb.htm
old-project: gdi
ms.assetid: affe6d0f-2827-4de1-a21e-8fdcdad85fc5
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: PALETTERGB, PALETTERGB macro [Windows GDI], _win32_PALETTERGB, gdi.palettergb, wingdi/PALETTERGB
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
tech.root: 
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - PALETTERGB
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PALETTERGB macro


## -description



The <b>PALETTERGB</b> macro accepts three values that represent the relative intensities of red, green, and blue and returns a palette-relative red, green, blue (RGB) specifier consisting of 2 in the high-order byte and an RGB value in the three low-order bytes. An application using a color palette can pass this specifier, instead of an explicit RGB value, to functions that expect a color.




## -parameters




### -param r

TBD


### -param g

TBD


### -param b

TBD






#### - bBlue

The intensity of the blue color field.


#### - bGreen

The intensity of the green color field.


#### - bRed

The intensity of the red color field.


## -see-also




<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



<a href="https://msdn.microsoft.com/f5bded0f-5f55-4512-9c00-9a9eb08c39f0">Color Macros</a>



<a href="https://msdn.microsoft.com/d1a25f13-6b47-4be7-927b-814dd6ae81f8">Colors Overview</a>



<a href="https://msdn.microsoft.com/76d859fa-11a5-451f-9d7a-9cf0740eca36">PALETTEINDEX</a>



<a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a>
 

 

