---
UID: NF:gdiplusgraphics.Graphics.FillPolygon(IN const Brush,IN const Point,IN INT,IN FillMode)
title: Graphics::FillPolygon(IN const Brush,IN const Point,IN INT,IN FillMode)
author: windows-sdk-content
description: The Graphics::FillPolygon method uses a brush to fill the interior of a polygon.
old-location: gdiplus\_gdiplus_CLASS_Graphics_FillPolygon_Brush_brush_PointF_points_INT_count_FillMode_fillMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsfillpolygonmethods\fillpolygon_71brushbrush_pointfpoints_intcount_fillm.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
ms.keywords: FillPolygon, FillPolygon method [GDI+], FillPolygon method [GDI+],Graphics class, Graphics class [GDI+],FillPolygon method, Graphics.FillPolygon, Graphics.FillPolygon(IN const Brush,IN const Point,IN INT,IN FillMode), Graphics.FillPolygon(const Brush*,const PointF*,INT,FillMode), Graphics::FillPolygon, Graphics::FillPolygon(IN const Brush,IN const Point,IN INT,IN FillMode), _gdiplus_CLASS_Graphics_FillPolygon_Brush_brush_PointF_points_INT_count_FillMode_fillMode_, gdiplus._gdiplus_CLASS_Graphics_FillPolygon_Brush_brush_PointF_points_INT_count_FillMode_fillMode_
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
 - Graphics.FillPolygon
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::FillPolygon(IN const Brush,IN const Point,IN INT,IN FillMode)


## -description


The <b>Graphics::FillPolygon</b> method uses a brush to fill the interior of a polygon. 


## -parameters




### -param brush [in]

Type: <b>const <a href="https://msdn.microsoft.com/37cfc0f8-8e17-4944-85fc-cc80ebff13df">Brush</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/37cfc0f8-8e17-4944-85fc-cc80ebff13df">Brush</a> object that is used to paint the interior of the polygon. 


### -param points [in]

Type: <b>const <a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a>*</b>

Pointer to an array of points that make up the vertices of the polygon. The first two points in the array specify the first side of the polygon. Each additional point specifies a new side, the vertices of which include the point and the previous point. If the last point and the first point do not coincide, they specify the last side of the polygon. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of points in the <i>points</i> array. 


### -param fillMode [in]

Type: <b><a href="https://msdn.microsoft.com/fd54e07b-74a2-4bce-9fa3-e36afec4be92">FillMode</a></b>

Element of the <a href="https://msdn.microsoft.com/fd54e07b-74a2-4bce-9fa3-e36afec4be92">FillMode</a> enumeration that specifies how to fill a closed area that is within another closed area and that is created when the curve or path passes over itself. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a>



<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a>
 

 

