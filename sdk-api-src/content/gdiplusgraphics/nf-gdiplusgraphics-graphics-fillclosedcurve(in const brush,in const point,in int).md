---
UID: NF:gdiplusgraphics.Graphics.FillClosedCurve(IN const Brush,IN const Point,IN INT)
title: Graphics::FillClosedCurve(IN const Brush,IN const Point,IN INT)
author: windows-sdk-content
description: The Graphics::FillClosedCurve method creates a closed cardinal spline from an array of points and uses a brush to fill the interior of the spline.
old-location: gdiplus\_gdiplus_CLASS_Graphics_FillClosedCurve_Brush_brush_Point_points_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsfillclosedcurvemethods\fillclosedcurve.htm
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: FillClosedCurve, FillClosedCurve method [GDI+], FillClosedCurve method [GDI+],Graphics class, Graphics class [GDI+],FillClosedCurve method, Graphics.FillClosedCurve, Graphics.FillClosedCurve(IN const Brush,IN const Point,IN INT), Graphics.FillClosedCurve(const Brush*,const Point*,INT), Graphics::FillClosedCurve, Graphics::FillClosedCurve(IN const Brush,IN const Point,IN INT), _gdiplus_CLASS_Graphics_FillClosedCurve_Brush_brush_Point_points_INT_count_, gdiplus._gdiplus_CLASS_Graphics_FillClosedCurve_Brush_brush_Point_points_INT_count_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusgraphics.h
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
 - Graphics.FillClosedCurve
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::FillClosedCurve(IN const Brush,IN const Point,IN INT)


## -description


The <b>Graphics::FillClosedCurve</b> method creates a closed cardinal spline from an array of points and uses a brush to fill the interior of the spline. 


## -parameters




### -param brush [in]

Type: <b>const <a href="https://msdn.microsoft.com/37cfc0f8-8e17-4944-85fc-cc80ebff13df">Brush</a>*</b>

Pointer to a 
					<a href="https://msdn.microsoft.com/37cfc0f8-8e17-4944-85fc-cc80ebff13df">Brush</a> object that is used to paint the interior of the spline. 


### -param points [in]

Type: <b>const <a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a>*</b>

Pointer to an array of points that this method uses to create a closed cardinal spline. Each point in the array is a point on the spline. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of points in the 
					<i>points</i> array. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/4fc62f00-7006-4ade-bfcc-091a3a97d889">Cardinal Splines</a>



<a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a>



<a href="https://msdn.microsoft.com/0bb84f55-18d0-4a4c-bc5b-7803aa807954">Drawing Cardinal Splines</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/e0fb8ba1-1783-4b36-93d8-f1242425d8bd">Open and Closed Curves</a>



<a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a>



<a href="https://msdn.microsoft.com/8d5c8780-f03c-40b2-b237-e40121e3d6f6">SolidBrush</a>
 

 

