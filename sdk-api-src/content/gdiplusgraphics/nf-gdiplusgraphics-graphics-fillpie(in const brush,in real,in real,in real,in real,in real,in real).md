---
UID: NF:gdiplusgraphics.Graphics.FillPie(IN const Brush,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL)
title: Graphics::FillPie(IN const Brush,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL)
author: windows-sdk-content
description: The Graphics::FillPie method uses a brush to fill the interior of a pie.
old-location: gdiplus\_gdiplus_CLASS_Graphics_FillPie_Brush_brush_REAL_x_REAL_y_REAL_width_REAL_height_REAL_startAngle_REA.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsfillpiemethods\fillpie_76brushbrush_realx_realy_realwidth_realh.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FillPie, FillPie method [GDI+], FillPie method [GDI+],Graphics class, Graphics class [GDI+],FillPie method, Graphics.FillPie, Graphics.FillPie(IN const Brush,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL), Graphics.FillPie(const Brush*,REAL,REAL,REAL,REAL,REAL,REAL), Graphics::FillPie, Graphics::FillPie(IN const Brush,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL), _gdiplus_CLASS_Graphics_FillPie_Brush_brush_REAL_x_REAL_y_REAL_width_REAL_height_REAL_startAngle_REA, gdiplus._gdiplus_CLASS_Graphics_FillPie_Brush_brush_REAL_x_REAL_y_REAL_width_REAL_height_REAL_startAngle_REA
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
 - Graphics.FillPie
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::FillPie(IN const Brush,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL,IN REAL)


## -description


The <b>Graphics::FillPie</b> method uses a brush to fill the interior of a pie. 


## -parameters




### -param brush [in]

Type: <b>const <a href="https://msdn.microsoft.com/37cfc0f8-8e17-4944-85fc-cc80ebff13df">Brush</a>*</b>

Pointer to a 
					<a href="https://msdn.microsoft.com/37cfc0f8-8e17-4944-85fc-cc80ebff13df">Brush</a> object that is used to paint the interior of the pie. 


### -param x [in]

Type: <b>REAL</b>

Real number that specifies the x-coordinate of the upper-left corner of the rectangle that bounds the ellipse. A curved portion of the ellipse is the arc of the pie. 


### -param y [in]

Type: <b>REAL</b>

Real number that specifies the y-coordinate of the upper-left corner of the rectangle that bounds the ellipse. 


### -param width [in]

Type: <b>REAL</b>

Real number that specifies the width of the rectangle that bounds the ellipse. 


### -param height [in]

Type: <b>REAL</b>

Real number that specifies the height of the rectangle that bounds the ellipse. 


### -param startAngle [in]

Type: <b>REAL</b>

Real number that specifies the angle, in degrees, between the x-axis and the starting point of the pie's arc. 


### -param sweepAngle [in]

Type: <b>REAL</b>

Real number that specifies the angle, in degrees, between the starting and ending points of the pie's arc. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



A pie is a portion of the interior of an ellipse (it is bounded by an elliptical curve and two radial lines). The 
				<i>startAngle</i> and <i>sweepAngle</i> specify the portion of the ellipse to be used.


#### Examples



The following example defines a pie and then fills it.


```cpp
VOID Example_FillPie4(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a SolidBrush object.
   SolidBrush blackBrush(Color(255, 0, 0, 0));

   // Define the pie shape.
   REAL x = 0.0f;
   REAL y = 2.0f;
   REAL width = 200.8f;
   REAL height = 100.1f;
   REAL startAngle = 0.0f;
   REAL sweepAngle = 45.7f;

   // Fill the pie.
   graphics.FillPie(&blackBrush, x, y, width, height, startAngle, sweepAngle);
}
```





## -see-also




<a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a>
 

 

