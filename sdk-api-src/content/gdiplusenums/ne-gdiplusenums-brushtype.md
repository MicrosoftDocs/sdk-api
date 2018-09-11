---
UID: NE:gdiplusenums.BrushType
title: BrushType
author: windows-sdk-content
description: The BrushType enumeration indicates the type of brush. There are five types of brushes.
old-location: gdiplus\_gdiplus_ENUM_BrushType.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\brushtype.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: BrushType, BrushType enumeration [GDI+], BrushTypeHatchFill, BrushTypeLinearGradient, BrushTypePathGradient, BrushTypeSolidColor, BrushTypeTextureFill, _gdiplus_ENUM_BrushType, gdiplus._gdiplus_ENUM_BrushType, gdiplusenums/BrushType, gdiplusenums/BrushTypeHatchFill, gdiplusenums/BrushTypeLinearGradient, gdiplusenums/BrushTypePathGradient, gdiplusenums/BrushTypeSolidColor, gdiplusenums/BrushTypeTextureFill
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusenums.h
api_name:
 - BrushType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# BrushType enumeration


## -description


The <b>BrushType</b> enumeration indicates the type of brush. There are five types of brushes.


## -enum-fields




### -field BrushTypeSolidColor

Indicates a brush of type <a href="https://msdn.microsoft.com/en-us/library/ms534508(v=VS.85).aspx">SolidBrush</a>. A solid brush paints a single, constant color that can be opaque or transparent. 


### -field BrushTypeHatchFill

Indicates a brush of type <a href="https://msdn.microsoft.com/en-us/library/ms534459(v=VS.85).aspx">HatchBrush</a>. A hatch brush paints a background and paints, over that background, a pattern of lines, dots, dashes, squares, crosshatch, or some variation of these. The hatch brush consists of two colors: one for the background and one for the pattern over the background. The color of the background is called the 
				<i>background color</i>, and the color of the pattern is called the 
				<i>foreground color</i>. 


### -field BrushTypeTextureFill

Indicates a brush of type <a href="https://msdn.microsoft.com/en-us/library/ms534512(v=VS.85).aspx">TextureBrush</a>. A texture brush paints an image. The image or 
				<i>texture</i> is either a portion of a specified image or a scaled version of a specified image. The type of image (metafile or nonmetafile) determines whether the texture is a portion of the image or a scaled version of the image. 


### -field BrushTypePathGradient

Indicates a brush of type <a href="https://msdn.microsoft.com/en-us/library/ms534483(v=VS.85).aspx">PathGradientBrush</a>. A path gradient brush paints a color gradient in which the color changes from a center point outward to a boundary that is defined by a closed curve or path. The color gradient has one color at the center point and one or multiple colors at the boundary. 


### -field BrushTypeLinearGradient

Indicates a brush of type <a href="https://msdn.microsoft.com/en-us/library/ms534473(v=VS.85).aspx">LinearGradientBrush</a>. A linear gradient brush paints a color gradient in which the color changes evenly from the starting boundary line of the linear gradient brush to the ending boundary line of the linear gradient brush. The boundary lines of a linear gradient brush are two parallel straight lines. The color gradient is perpendicular to the boundary lines of the linear gradient brush, changing gradually across the stroke from the starting boundary line to the ending boundary line. The color gradient has one color at the starting boundary line and another color at the ending boundary line. 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536356(v=VS.85).aspx">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534459(v=VS.85).aspx">HatchBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534473(v=VS.85).aspx">LinearGradientBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534483(v=VS.85).aspx">PathGradientBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534508(v=VS.85).aspx">SolidBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534512(v=VS.85).aspx">TextureBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533811(v=VS.85).aspx">Using a Brush to Fill Shapes</a>
 

 

