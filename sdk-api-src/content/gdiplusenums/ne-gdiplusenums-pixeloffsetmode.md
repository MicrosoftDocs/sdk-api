---
UID: NE:gdiplusenums.PixelOffsetMode
title: PixelOffsetMode
author: windows-sdk-content
description: The PixelOffsetMode enumeration specifies the pixel offset mode of a Graphics object. This enumeration is used by the Graphics::GetPixelOffsetMode and Graphics::SetPixelOffsetMode methods of the Graphics class.
old-location: gdiplus\_gdiplus_ENUM_PixelOffsetMode.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\pixeloffsetmode.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: PixelOffsetMode, PixelOffsetMode enumeration [GDI+], PixelOffsetModeDefault, PixelOffsetModeHalf, PixelOffsetModeHighQuality, PixelOffsetModeHighSpeed, PixelOffsetModeInvalid, PixelOffsetModeNone, _gdiplus_ENUM_PixelOffsetMode, gdiplus._gdiplus_ENUM_PixelOffsetMode, gdiplusenums/PixelOffsetMode, gdiplusenums/PixelOffsetModeDefault, gdiplusenums/PixelOffsetModeHalf, gdiplusenums/PixelOffsetModeHighQuality, gdiplusenums/PixelOffsetModeHighSpeed, gdiplusenums/PixelOffsetModeInvalid, gdiplusenums/PixelOffsetModeNone
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: gdiplusenums.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusenums.h
api_name:
 - PixelOffsetMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.0
---

# PixelOffsetMode enumeration


## -description


The <b>PixelOffsetMode</b> enumeration specifies the pixel offset mode of a 
			<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object. This enumeration is used by the <a href="https://msdn.microsoft.com/9d379aad-8e0d-4e3f-bbff-a8b26d0efa15">Graphics::GetPixelOffsetMode</a> and <a href="https://msdn.microsoft.com/2e93a8b1-e44d-4bd9-86bc-4291719afe9c">Graphics::SetPixelOffsetMode</a> methods of the 
			<b>Graphics</b> class.


## -enum-fields




### -field PixelOffsetModeInvalid

Used internally. 


### -field PixelOffsetModeDefault

Equivalent to PixelOffsetModeNone. 


### -field PixelOffsetModeHighSpeed

Equivalent to PixelOffsetModeNone. 


### -field PixelOffsetModeHighQuality

Equivalent to PixelOffsetModeHalf. 


### -field PixelOffsetModeNone

Indicates that pixel centers have integer coordinates. 


### -field PixelOffsetModeHalf

Indicates that pixel centers have coordinates that are half way between integer values. 


## -remarks



Consider the pixel in the upper-left corner of an image with address (0, 0). With <b><b>PixelOffsetModeNone</b></b>, the pixel covers the area between 
				–0.5 and 0.5 in both the x and y directions; that is, the pixel center is at (0, 0). With <b><b>PixelOffsetModeHalf</b></b>, the pixel covers the area between 0 and 1 in both the x and y directions; that is, the pixel center is at (0.5, 0.5).




## -see-also




<a href="https://msdn.microsoft.com/9d379aad-8e0d-4e3f-bbff-a8b26d0efa15">Graphics::GetPixelOffsetMode</a>



<a href="https://msdn.microsoft.com/2e93a8b1-e44d-4bd9-86bc-4291719afe9c">Graphics::SetPixelOffsetMode</a>
 

 

