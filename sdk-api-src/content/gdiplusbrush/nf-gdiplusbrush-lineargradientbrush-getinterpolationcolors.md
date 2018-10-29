---
UID: NF:gdiplusbrush.LinearGradientBrush.GetInterpolationColors
title: LinearGradientBrush::GetInterpolationColors
author: windows-sdk-content
description: The LinearGradientBrush::GetInterpolationColors method gets the colors currently set to be interpolated for this linear gradient brush and their corresponding blend positions.
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_GetInterpolationColors_presetColors_blendPositions_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushmethods\getinterpolationcolors.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetInterpolationColors, GetInterpolationColors method [GDI+], GetInterpolationColors method [GDI+],LinearGradientBrush class, LinearGradientBrush class [GDI+],GetInterpolationColors method, LinearGradientBrush.GetInterpolationColors, LinearGradientBrush::GetInterpolationColors, _gdiplus_CLASS_LinearGradientBrush_GetInterpolationColors_presetColors_blendPositions_count_, gdiplus._gdiplus_CLASS_LinearGradientBrush_GetInterpolationColors_presetColors_blendPositions_count_
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
 - LinearGradientBrush.GetInterpolationColors
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# LinearGradientBrush::GetInterpolationColors


## -description


The <b>LinearGradientBrush::GetInterpolationColors</b> method gets the colors currently set to be interpolated for this linear gradient brush and their corresponding blend positions.


## -parameters




### -param presetColors [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534427(v=VS.85).aspx">Color</a>*</b>

Pointer to an array that receives the colors. A color of a given index in the 
					<i>presetColors</i> array corresponds to the blend position of that same index in the 
					<i>blendPositions</i> array. 


### -param blendPositions [out]

Type: <b>REAL*</b>

Pointer to an array that receives the blend positions. Each number in the array indicates a percentage of the distance between the starting boundary and the ending boundary and is in the range from 0.0 through 1.0, where 0.0 indicates the starting boundary of the gradient and 1.0 indicates the ending boundary. A blend position between 0.0 and 1.0 indicates a line, parallel to the boundary lines, that is a certain fraction of the distance from the starting boundary to the ending boundary. For example, a blend position of 0.7 indicates the line that is 70 percent of the distance from the starting boundary to the ending boundary. The color is constant on lines that are parallel to the boundary lines. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the 
					<i>presetColors </i> array. This is the same as the number of elements in the 
					<i>blendPositions</i> array. Before calling the <b>LinearGradientBrush::GetInterpolationColors</b> method of a 
					<a href="https://msdn.microsoft.com/en-us/library/ms534473(v=VS.85).aspx">LinearGradientBrush</a> object, call the <a href="https://msdn.microsoft.com/en-us/library/ms535331(v=VS.85).aspx">LinearGradientBrush::GetInterpolationColorCount</a> method of that same 
					<b>LinearGradientBrush</b> object to determine the current number of colors. The number of blend positions retrieved is the same as the number of colors retrieved. 


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



<a href="https://msdn.microsoft.com/en-us/library/ms535331(v=VS.85).aspx">LinearGradientBrush::GetInterpolationColorCount</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535346(v=VS.85).aspx">LinearGradientBrush::SetInterpolationColors</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534483(v=VS.85).aspx">PathGradientBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534495(v=VS.85).aspx">Rect</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534508(v=VS.85).aspx">SolidBrush</a>
 

 

