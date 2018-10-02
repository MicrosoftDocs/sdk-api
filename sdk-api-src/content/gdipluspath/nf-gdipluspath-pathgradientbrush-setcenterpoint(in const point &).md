---
UID: NF:gdipluspath.PathGradientBrush.SetCenterPoint(IN const Point &)
title: PathGradientBrush::SetCenterPoint(IN const Point &)
author: windows-sdk-content
description: The PathGradientBrush::SetCenterPoint method sets the center point of this path gradient brush. By default, the center point is at the centroid of the brush's boundary path, but you can set the center point to any location inside or outside the path.
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_SetCenterPoint_Point_point_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\pathgradientbrushsetcenterpointmethods\setcenterpoint.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: PathGradientBrush class [GDI+],SetCenterPoint method, PathGradientBrush.SetCenterPoint, PathGradientBrush.SetCenterPoint(IN const Point &), PathGradientBrush.SetCenterPoint(const Point&), PathGradientBrush::SetCenterPoint, PathGradientBrush::SetCenterPoint(IN const Point &), SetCenterPoint, SetCenterPoint method [GDI+], SetCenterPoint method [GDI+],PathGradientBrush class, _gdiplus_CLASS_PathGradientBrush_SetCenterPoint_Point_point_, gdiplus._gdiplus_CLASS_PathGradientBrush_SetCenterPoint_Point_point_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdipluspath.h
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
 - PathGradientBrush.SetCenterPoint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# PathGradientBrush::SetCenterPoint(IN const Point &)


## -description


The <b>PathGradientBrush::SetCenterPoint</b> method sets the center point of this path gradient brush. By default, the center point is at the centroid of the brush's boundary path, but you can set the center point to any location inside or outside the path.


## -parameters




### -param point [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a></b>

Reference to a 
					<a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a> object that specifies the center point. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/7aa94b39-bd4c-4e66-b0dc-77f8953797b1">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534483(v=VS.85).aspx">PathGradientBrush</a>



<a href="https://msdn.microsoft.com/b5b79732-f89a-46fb-b7ac-2eb45f7d4f87">PathGradientBrush::GetCenterColor</a>



<a href="https://msdn.microsoft.com/6bd4993d-2401-4070-be0e-dbac684095d3">PathGradientBrush::GetCenterPoint Methods</a>



<a href="https://msdn.microsoft.com/33e9a8f0-7c07-475d-8332-cf2e08190b35">PathGradientBrush::SetCenterColor</a>
 

 

