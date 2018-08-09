---
UID: NF:gdiplusbrush.LinearGradientBrush.SetInterpolationColors
title: LinearGradientBrush::SetInterpolationColors
author: windows-sdk-content
description: The LinearGradientBrush::SetInterpolationColors method sets the colors to be interpolated for this linear gradient brush and their corresponding blend positions.
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_SetInterpolationColors_presetColors_blendPositions_count_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushmethods\setinterpolationcolors.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: LinearGradientBrush class [GDI+],SetInterpolationColors method, LinearGradientBrush.SetInterpolationColors, LinearGradientBrush::SetInterpolationColors, SetInterpolationColors, SetInterpolationColors method [GDI+], SetInterpolationColors method [GDI+],LinearGradientBrush class, _gdiplus_CLASS_LinearGradientBrush_SetInterpolationColors_presetColors_blendPositions_count_, gdiplus._gdiplus_CLASS_LinearGradientBrush_SetInterpolationColors_presetColors_blendPositions_count_
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: KnownGamingPrivileges
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - LinearGradientBrush.SetInterpolationColors
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# LinearGradientBrush::SetInterpolationColors


## -description


The <b>LinearGradientBrush::SetInterpolationColors</b> method sets the colors to be interpolated for this linear gradient brush and their corresponding blend positions.


## -parameters




### -param presetColors [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a>*</b>

Pointer to an array of <a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a> objects that specify the colors to be interpolated for this linear gradient brush. A color of a given index in the 
					<i>presetColors</i> array corresponds to the blend position of that same index in the 
					<i>blendPositions</i> array. 


### -param blendPositions [in]

Type: <b>const REAL*</b>

Pointer to an array of real numbers that specify the blend positions. Each number in the array specifies a percentage of the distance between the starting boundary and the ending boundary and is in the range from 0.0 through 1.0, where 0.0 indicates the starting boundary of the gradient and 1.0 indicates the ending boundary. There must be at least two positions specified: the first position, which is always 0.0f, and the last position, which is always 1.0f. Otherwise, the behavior is undefined. A blend position between 0.0 and 1.0 indicates the line, parallel to the boundary lines, that is a certain fraction of the distance from the starting boundary to the ending boundary. For example, a blend position of 0.7 indicates the line that is 70 percent of the distance from the starting boundary to the ending boundary. The color is constant on lines that are parallel to the boundary lines. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the 
					<i>presetColors</i> array. This is the same as the number of elements in the 
					<i>blendPositions</i> array. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536356(v=VS.85).aspx">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533914(v=VS.85).aspx">Creating a Linear Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533856(v=VS.85).aspx">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534473(v=VS.85).aspx">LinearGradientBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535332(v=VS.85).aspx">LinearGradientBrush::GetInterpolationColors</a>
 

 

