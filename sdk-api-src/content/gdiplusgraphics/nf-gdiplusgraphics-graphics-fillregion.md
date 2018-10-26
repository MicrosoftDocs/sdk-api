---
UID: NF:gdiplusgraphics.Graphics.FillRegion
title: Graphics::FillRegion
author: windows-sdk-content
description: The Graphics::FillRegion method uses a brush to fill a specified region.
old-location: gdiplus\_gdiplus_CLASS_Graphics_FillRegion_brush_region_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\fillregion.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: FillRegion, FillRegion method [GDI+], FillRegion method [GDI+],Graphics class, Graphics class [GDI+],FillRegion method, Graphics.FillRegion, Graphics::FillRegion, _gdiplus_CLASS_Graphics_FillRegion_brush_region_, gdiplus._gdiplus_CLASS_Graphics_FillRegion_brush_region_
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
 - Graphics.FillRegion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::FillRegion


## -description


The <b>Graphics::FillRegion</b> method uses a brush to fill a specified region.


## -parameters




### -param brush [in]

Type: <b>const <a href="https://msdn.microsoft.com/37cfc0f8-8e17-4944-85fc-cc80ebff13df">Brush</a>*</b>

Pointer to a brush that is used to paint the region. 


### -param region [in]

Type: <b>const <a href="https://msdn.microsoft.com/2972b879-7d2f-4cad-b17d-670125f43691">Region</a>*</b>

Pointer to a region to be filled. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



Because a region describes a set of pixels, a pixel is considered either fully inside, or fully outside the region. Consequently, <b>Graphics::FillRegion</b> does not antialias the edges of the region.


#### Examples



The following example creates a region from a rectangle and then fills the region.


```cpp
VOID Example_FillRegion(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a SolidBrush object.
   SolidBrush blackBrush(Color(255, 0, 0, 0));

   // Create a Region object from a rectangle.
   Region ellipseRegion(Rect(0, 0, 200, 100));

   // Fill the region.
   graphics.FillRegion(&blackBrush, &ellipseRegion);
}
```





## -see-also




<a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>



<a href="https://msdn.microsoft.com/2972b879-7d2f-4cad-b17d-670125f43691">Region</a>



<a href="https://msdn.microsoft.com/eb78d7a0-6293-487f-88c5-88ba455b965f">Regions</a>



<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a>
 

 

