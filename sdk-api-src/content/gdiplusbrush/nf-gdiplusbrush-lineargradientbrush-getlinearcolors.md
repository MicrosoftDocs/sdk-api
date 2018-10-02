---
UID: NF:gdiplusbrush.LinearGradientBrush.GetLinearColors
title: LinearGradientBrush::GetLinearColors
author: windows-sdk-content
description: The LinearGradientBrush::GetLinearColors method gets the starting color and ending color of this linear gradient brush.
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_GetLinearColors_colors_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushmethods\getlinearcolors.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetLinearColors, GetLinearColors method [GDI+], GetLinearColors method [GDI+],LinearGradientBrush class, LinearGradientBrush class [GDI+],GetLinearColors method, LinearGradientBrush.GetLinearColors, LinearGradientBrush::GetLinearColors, _gdiplus_CLASS_LinearGradientBrush_GetLinearColors_colors_, gdiplus._gdiplus_CLASS_LinearGradientBrush_GetLinearColors_colors_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusbrush.h
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - LinearGradientBrush.GetLinearColors
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# LinearGradientBrush::GetLinearColors


## -description


The <b>LinearGradientBrush::GetLinearColors</b> method gets the starting color and ending color of this linear gradient brush.


## -parameters




### -param colors [out]

Type: <b>Color*</b>

Pointer to an array that receives the starting color and the ending color. The first color in the 
					<i>colors</i> array is the color at the starting boundary line of the gradient; the second color in the 
					<i>colors</i> array is the color at the ending boundary line. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536356(v=VS.85).aspx">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534427(v=VS.85).aspx">Color</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533914(v=VS.85).aspx">Creating a Linear Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533856(v=VS.85).aspx">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534473(v=VS.85).aspx">LinearGradientBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535347(v=VS.85).aspx">LinearGradientBrush::SetLinearColors</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534495(v=VS.85).aspx">Rect</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534508(v=VS.85).aspx">SolidBrush</a>
 

 

