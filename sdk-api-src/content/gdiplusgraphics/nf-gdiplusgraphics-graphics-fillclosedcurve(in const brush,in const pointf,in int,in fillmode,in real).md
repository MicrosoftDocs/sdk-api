---
UID: NF:gdiplusgraphics.Graphics.FillClosedCurve(IN const Brush,IN const PointF,IN INT,IN FillMode,IN REAL)
title: Graphics::FillClosedCurve(IN const Brush,IN const PointF,IN INT,IN FillMode,IN REAL)
author: windows-sdk-content
description: The Graphics::FillClosedCurve method creates a closed cardinal spline from an array of points and uses a brush to fill, according to a specified mode, the interior of the spline.
old-location: gdiplus\_gdiplus_CLASS_Graphics_FillClosedCurve_Brush_brush_PointF_points_INT_count_FillMode_fillMode_REAL_t.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsfillclosedcurvemethods\fillclosedcurve_59brushbrush_pointfpoints_intcount_fillm.htm
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: FillClosedCurve, FillClosedCurve method [GDI+], FillClosedCurve method [GDI+],Graphics class, Graphics class [GDI+],FillClosedCurve method, Graphics.FillClosedCurve, Graphics.FillClosedCurve(IN const Brush,IN const PointF,IN INT,IN FillMode,IN REAL), Graphics.FillClosedCurve(const Brush*,const PointF*,INT,FillMode,REAL), Graphics::FillClosedCurve, Graphics::FillClosedCurve(IN const Brush,IN const PointF,IN INT,IN FillMode,IN REAL), _gdiplus_CLASS_Graphics_FillClosedCurve_Brush_brush_PointF_points_INT_count_FillMode_fillMode_REAL_t, gdiplus._gdiplus_CLASS_Graphics_FillClosedCurve_Brush_brush_PointF_points_INT_count_FillMode_fillMode_REAL_t
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

# Graphics::FillClosedCurve(IN const Brush,IN const PointF,IN INT,IN FillMode,IN REAL)


## -description


The <b>Graphics::FillClosedCurve</b> method creates a closed cardinal spline from an array of points and uses a brush to fill, according to a specified mode, the interior of the spline.


## -parameters




### -param brush [in]

Type: <b>const <a href="https://msdn.microsoft.com/37cfc0f8-8e17-4944-85fc-cc80ebff13df">Brush</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/37cfc0f8-8e17-4944-85fc-cc80ebff13df">Brush</a> object that is used to paint the interior of the spline. 


### -param points [in]

Type: <b>const <a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a>*</b>

Pointer to an array of points that this method uses to create a closed cardinal spline. Each point in the array is a point on the spline. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of points in the 
					<i>points</i> array. 


### -param fillMode [in]

Type: <b><a href="https://msdn.microsoft.com/fd54e07b-74a2-4bce-9fa3-e36afec4be92">FillMode</a></b>

Element of the <a href="https://msdn.microsoft.com/fd54e07b-74a2-4bce-9fa3-e36afec4be92">FillMode</a> enumeration that specifies how to fill a closed area that is created when the curve passes over itself. 


### -param tension [in]

Type: <b>REAL</b>

Optional. Nonnegative real number that specifies how tightly the spline bends as it passes through the points. A value of 0 specifies that the spline is a sequence of straight lines. As the value increases, the curve becomes fuller. The default value is 0.5f. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<b>Status</b> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/37cfc0f8-8e17-4944-85fc-cc80ebff13df">Brush</a>



<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/4fc62f00-7006-4ade-bfcc-091a3a97d889">Cardinal Splines</a>



<a href="https://msdn.microsoft.com/0bb84f55-18d0-4a4c-bc5b-7803aa807954">Drawing Cardinal Splines</a>



<a href="https://msdn.microsoft.com/fd54e07b-74a2-4bce-9fa3-e36afec4be92">FillMode</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/e0fb8ba1-1783-4b36-93d8-f1242425d8bd">Open and Closed Curves</a>



<a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a>
 

 

