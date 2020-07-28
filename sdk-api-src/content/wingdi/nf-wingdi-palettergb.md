---
UID: NF:wingdi.PALETTERGB
title: PALETTERGB macro (wingdi.h)
description: The PALETTERGB macro accepts three values that represent the relative intensities of red, green, and blue and returns a palette-relative red, green, blue (RGB) specifier consisting of 2 in the high-order byte and an RGB value in the three low-order bytes. An application using a color palette can pass this specifier, instead of an explicit RGB value, to functions that expect a color.
helpviewer_keywords: ["PALETTERGB","PALETTERGB macro [Windows GDI]","_win32_PALETTERGB","gdi.palettergb","wingdi/PALETTERGB"]
old-location: gdi\palettergb.htm
tech.root: gdi
ms.assetid: affe6d0f-2827-4de1-a21e-8fdcdad85fc5
ms.date: 12/05/2018
ms.keywords: PALETTERGB, PALETTERGB macro [Windows GDI], _win32_PALETTERGB, gdi.palettergb, wingdi/PALETTERGB
f1_keywords:
- wingdi/PALETTERGB
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Wingdi.h
api_name:
- PALETTERGB
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PALETTERGB macro


## -description



The <b>PALETTERGB</b> macro accepts three values that represent the relative intensities of red, green, and blue and returns a palette-relative red, green, blue (RGB) specifier consisting of 2 in the high-order byte and an RGB value in the three low-order bytes. An application using a color palette can pass this specifier, instead of an explicit RGB value, to functions that expect a color.




## -parameters




### -param r

The intensity of the red color field.


### -param g

The intensity of the green color field.


### -param b

The intensity of the blue color field.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdi/colorref">COLORREF</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/color-macros">Color Macros</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/colors">Colors Overview</a>



<a href="https://docs.microsoft.com/previous-versions/dd162770(v=vs.85)">PALETTEINDEX</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a>
 

 

