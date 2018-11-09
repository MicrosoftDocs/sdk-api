---
UID: NS:wingdi.tagRGBQUAD
title: tagRGBQUAD
author: windows-sdk-content
description: The RGBQUAD structure describes a color consisting of relative intensities of red, green, and blue.
old-location: gdi\rgbquad.htm
tech.root: gdi
ms.assetid: 22e0991d-078e-4b44-9f03-004137e31f6c
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*LPRGBQUAD, RGBQUAD, RGBQUAD structure [Windows GDI], _win32_RGBQUAD_str, gdi.rgbquad, tagRGBQUAD, wingdi/RGBQUAD"
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
 - RGBQUAD
product: Windows
targetos: Windows
req.typenames: RGBQUAD
req.redist: 
---

# tagRGBQUAD structure


## -description



The <b>RGBQUAD</b> structure describes a color consisting of relative intensities of red, green, and blue.




## -struct-fields




### -field rgbBlue

The intensity of blue in the color.


### -field rgbGreen

The intensity of green in the color.


### -field rgbRed

The intensity of red in the color.


### -field rgbReserved

This member is reserved and must be zero.


## -remarks



The <b>bmiColors</b> member of the <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure consists of an array of <b>RGBQUAD</b> structures.




## -see-also




<a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a>



<a href="https://msdn.microsoft.com/29f8237f-9c7e-41a7-90b1-5f048fcc74a6">Bitmap Structures</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/9276ec84-2860-42be-a9f8-d4efb8d25eec">CreateDIBSection</a>



<a href="https://msdn.microsoft.com/e9a5b525-a6b6-4309-9e53-69d274b85783">CreateDIBitmap</a>



<a href="https://msdn.microsoft.com/be3ffa3f-b343-4e38-8b1e-aeccf35d92b8">GetDIBits</a>



<a href="https://msdn.microsoft.com/706f4532-4073-4d5c-ae2d-e33aea9163e9">SetDIBits</a>



<a href="https://msdn.microsoft.com/41225400-12e3-47ba-8b88-ac1d5b0fa90f">SetDIBitsToDevice</a>



<a href="https://msdn.microsoft.com/3d57a79a-338d-48ab-8161-3ce17739bf20">StretchDIBits</a>
 

 

