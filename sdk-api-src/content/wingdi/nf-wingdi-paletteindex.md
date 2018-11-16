---
UID: NF:wingdi.PALETTEINDEX
title: PALETTEINDEX macro
author: windows-sdk-content
description: The PALETTEINDEX macro accepts an index to a logical-color palette entry and returns a palette-entry specifier consisting of a COLORREF value that specifies the color associated with the given index.
old-location: gdi\paletteindex.htm
tech.root: gdi
ms.assetid: 76d859fa-11a5-451f-9d7a-9cf0740eca36
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: PALETTEINDEX, PALETTEINDEX macro [Windows GDI], _win32_PALETTEINDEX, gdi.paletteindex, wingdi/PALETTEINDEX
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - PALETTEINDEX
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- wingdi.h
: 
- PALETTEINDEX
: 
---

# PALETTEINDEX macro


## -description



The <b>PALETTEINDEX</b> macro accepts an index to a logical-color palette entry and returns a palette-entry specifier consisting of a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> value that specifies the color associated with the given index. An application using a logical palette can pass this specifier, instead of an explicit red, green, blue (RGB) value, to GDI functions that expect a color. This allows the function to use the color in the specified palette entry.




## -parameters




### -param i

An index to the palette entry containing the color to be used for a graphics operation.


## -see-also




<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



<a href="https://msdn.microsoft.com/f5bded0f-5f55-4512-9c00-9a9eb08c39f0">Color Macros</a>



<a href="https://msdn.microsoft.com/d1a25f13-6b47-4be7-927b-814dd6ae81f8">Colors Overview</a>



<a href="https://msdn.microsoft.com/affe6d0f-2827-4de1-a21e-8fdcdad85fc5">PALETTERGB</a>



<a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a>
 

 

