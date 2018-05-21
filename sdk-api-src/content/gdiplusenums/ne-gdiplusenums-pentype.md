---
UID: NE:gdiplusenums.PenType
title: PenType
author: windows-driver-content
description: The PenType enumeration indicates the type of pattern, texture, or gradient that a pen draws.
old-location: gdiplus\_gdiplus_ENUM_PenType.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\pentype.htm
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: PenType, PenType enumeration [GDI+], PenTypeHatchFill, PenTypeLinearGradient, PenTypePathGradient, PenTypeSolidColor, PenTypeTextureFill, PenTypeUnknown, _gdiplus_ENUM_PenType, gdiplus._gdiplus_ENUM_PenType, gdiplusenums/PenType, gdiplusenums/PenTypeHatchFill, gdiplusenums/PenTypeLinearGradient, gdiplusenums/PenTypePathGradient, gdiplusenums/PenTypeSolidColor, gdiplusenums/PenTypeTextureFill, gdiplusenums/PenTypeUnknown
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Gdiplusenums.h
api_name:
-	PenType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.0
---

# PenType enumeration


## -description


The <b>PenType</b> enumeration indicates the type of pattern, texture, or gradient that a pen draws. 


## -enum-fields




### -field PenTypeSolidColor

Indicates that the pen draws with a solid color. 


### -field PenTypeHatchFill

Indicates that the pen draws with a hatch pattern that is specified by a 
				<a href="https://msdn.microsoft.com/6e633cb2-8b0f-4b6a-95d8-f494d5f972eb">HatchBrush</a> object. 


### -field PenTypeTextureFill

Indicates that the pen draws with a texture that is specified by a 
				<a href="https://msdn.microsoft.com/4657ed8b-9cec-49ba-bf20-545bf3ee51f9">TextureBrush</a> object. 


### -field PenTypePathGradient

Indicates that the pen draws with a color gradient that is specified by a 
				<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a> object. 


### -field PenTypeLinearGradient

Indicates that the pen draws with a color gradient that is specified by a 
				<a href="https://msdn.microsoft.com/43901cd3-b059-4830-9063-e8287899e18a">LinearGradientBrush</a> object. 


### -field PenTypeUnknown

Indicates that the pen type is unknown. 


## -remarks



A pen's type is determined when the pen is constructed. For example, if you pass a 
				<a href="https://msdn.microsoft.com/6e633cb2-8b0f-4b6a-95d8-f494d5f972eb">HatchBrush</a> object to a 
				<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> constructor, then the pen that is constructed has a pen type of <b><b>PenTypeHatchFill</b></b>. If you pass a 
				<a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a> object or a 
				<a href="https://msdn.microsoft.com/8d5c8780-f03c-40b2-b237-e40121e3d6f6">SolidBrush</a> object to a 
				<b>Pen</b> constructor, then the pen that is constructed has a pen type of <b><b>PenTypeSolidColor</b></b>. 



