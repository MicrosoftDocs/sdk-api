---
UID: NF:gdipluspath.PathGradientBrush.SetCenterPoint(IN const Point &)
title: PathGradientBrush::SetCenterPoint(IN const Point &) (gdipluspath.h)
author: windows-sdk-content
description: The PathGradientBrush::SetCenterPoint method sets the center point of this path gradient brush. By default, the center point is at the centroid of the brush's boundary path, but you can set the center point to any location inside or outside the path.
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_SetCenterPoint_Point_point_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\pathgradientbrushsetcenterpointmethods\setcenterpoint.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PathGradientBrush class [GDI+],SetCenterPoint method, PathGradientBrush.SetCenterPoint, PathGradientBrush.SetCenterPoint(IN const Point &), PathGradientBrush.SetCenterPoint(const Point&), PathGradientBrush::SetCenterPoint, PathGradientBrush::SetCenterPoint(IN const Point &), SetCenterPoint, SetCenterPoint method [GDI+], SetCenterPoint method [GDI+],PathGradientBrush class, _gdiplus_CLASS_PathGradientBrush_SetCenterPoint_Point_point_, gdiplus._gdiplus_CLASS_PathGradientBrush_SetCenterPoint_Point_point_
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

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a></b>

Reference to a 
					<a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a> object that specifies the center point. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536356(v=VS.85).aspx">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533856(v=VS.85).aspx">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534483(v=VS.85).aspx">PathGradientBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535064(v=VS.85).aspx">PathGradientBrush::GetCenterColor</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535076(v=VS.85).aspx">PathGradientBrush::GetCenterPoint Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535085(v=VS.85).aspx">PathGradientBrush::SetCenterColor</a>
 

 

