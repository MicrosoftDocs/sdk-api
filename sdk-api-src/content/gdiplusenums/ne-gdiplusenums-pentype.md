---
UID: NE:gdiplusenums.PenType
title: PenType
author: windows-sdk-content
description: The PenType enumeration indicates the type of pattern, texture, or gradient that a pen draws.
old-location: gdiplus\_gdiplus_ENUM_PenType.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\pentype.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: PenType, PenType enumeration [GDI+], PenTypeHatchFill, PenTypeLinearGradient, PenTypePathGradient, PenTypeSolidColor, PenTypeTextureFill, PenTypeUnknown, _gdiplus_ENUM_PenType, gdiplus._gdiplus_ENUM_PenType, gdiplusenums/PenType, gdiplusenums/PenTypeHatchFill, gdiplusenums/PenTypeLinearGradient, gdiplusenums/PenTypePathGradient, gdiplusenums/PenTypeSolidColor, gdiplusenums/PenTypeTextureFill, gdiplusenums/PenTypeUnknown
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
 - PenType
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
				<a href="https://msdn.microsoft.com/library/ms534459(v=VS.85).aspx">HatchBrush</a> object. 


### -field PenTypeTextureFill

Indicates that the pen draws with a texture that is specified by a 
				<a href="https://msdn.microsoft.com/library/ms534512(v=VS.85).aspx">TextureBrush</a> object. 


### -field PenTypePathGradient

Indicates that the pen draws with a color gradient that is specified by a 
				<a href="https://msdn.microsoft.com/library/ms534483(v=VS.85).aspx">PathGradientBrush</a> object. 


### -field PenTypeLinearGradient

Indicates that the pen draws with a color gradient that is specified by a 
				<a href="https://msdn.microsoft.com/library/ms534473(v=VS.85).aspx">LinearGradientBrush</a> object. 


### -field PenTypeUnknown

Indicates that the pen type is unknown. 


## -remarks



A pen's type is determined when the pen is constructed. For example, if you pass a 
				<a href="https://msdn.microsoft.com/library/ms534459(v=VS.85).aspx">HatchBrush</a> object to a 
				<a href="https://msdn.microsoft.com/library/ms534485(v=VS.85).aspx">Pen</a> constructor, then the pen that is constructed has a pen type of <b><b>PenTypeHatchFill</b></b>. If you pass a 
				<a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a> object or a 
				<a href="https://msdn.microsoft.com/library/ms534508(v=VS.85).aspx">SolidBrush</a> object to a 
				<b>Pen</b> constructor, then the pen that is constructed has a pen type of <b><b>PenTypeSolidColor</b></b>. 



