---
UID: NS:wingdi.tagRGBTRIPLE
title: tagRGBTRIPLE
author: windows-sdk-content
description: The RGBTRIPLE structure describes a color consisting of relative intensities of red, green, and blue. The bmciColors member of the BITMAPCOREINFO structure consists of an array of RGBTRIPLE structures.
old-location: gdi\rgbtriple.htm
old-project: gdi
ms.assetid: bc1467a5-0027-4f22-bfc9-1deab562c573
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPRGBTRIPLE, *NPRGBTRIPLE, *PRGBTRIPLE, RGBTRIPLE, RGBTRIPLE structure [Windows GDI], _win32_RGBTRIPLE_str, gdi.rgbtriple, tagRGBTRIPLE, wingdi/RGBTRIPLE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: RGBTRIPLE, *PRGBTRIPLE, *NPRGBTRIPLE, *LPRGBTRIPLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - RGBTRIPLE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagRGBTRIPLE structure


## -description



The <b>RGBTRIPLE</b> structure describes a color consisting of relative intensities of red, green, and blue. The <b>bmciColors</b> member of the <a href="https://msdn.microsoft.com/cb6cb9da-8f7f-47e9-980a-aa77fe04c80c">BITMAPCOREINFO</a> structure consists of an array of <b>RGBTRIPLE</b> structures.




## -struct-fields




### -field rgbtBlue

The intensity of blue in the color.


### -field rgbtGreen

The intensity of green in the color.


### -field rgbtRed

The intensity of red in the color.


## -see-also




<a href="https://msdn.microsoft.com/cb6cb9da-8f7f-47e9-980a-aa77fe04c80c">BITMAPCOREINFO</a>



<a href="https://msdn.microsoft.com/29f8237f-9c7e-41a7-90b1-5f048fcc74a6">Bitmap Structures</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>
 

 

