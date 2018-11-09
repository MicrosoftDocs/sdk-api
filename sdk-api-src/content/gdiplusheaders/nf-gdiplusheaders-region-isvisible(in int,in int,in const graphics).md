---
UID: NF:gdiplusheaders.Region.IsVisible(IN INT,IN INT,IN const Graphics)
title: Region::IsVisible(IN INT,IN INT,IN const Graphics)
author: windows-sdk-content
description: The Region::IsVisible method determines whether a point is inside this region.
old-location: gdiplus\_gdiplus_CLASS_Region_IsVisible_INT_x_INT_y_Graphics_g_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\regionisvisiblemethods\isvisible_51intx_inty_graphicsg.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IsVisible, IsVisible method [GDI+], IsVisible method [GDI+],Region class, Region class [GDI+],IsVisible method, Region.IsVisible, Region.IsVisible(IN INT,IN INT,IN const Graphics), Region.IsVisible(INT,INT,const Graphics*), Region::IsVisible, Region::IsVisible(IN INT,IN INT,IN const Graphics), _gdiplus_CLASS_Region_IsVisible_INT_x_INT_y_Graphics_g_, gdiplus._gdiplus_CLASS_Region_IsVisible_INT_x_INT_y_Graphics_g_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusheaders.h
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
 - Region.IsVisible
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Region::IsVisible(IN INT,IN INT,IN const Graphics)


## -description


The <b>Region::IsVisible</b> method determines whether a point is inside this region.


## -parameters




### -param x [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the point to test. 


### -param y [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the point to test. 


### -param g [in]

Type: <b>const <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>*</b>

Optional. Pointer to a <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object that contains the world and page transformations required to calculate the device coordinates of this region and the point. The default value is <b>NULL</b>. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the point is inside this region, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.




## -remarks



<div class="alert"><b>Note</b>  A region contains its border.</div>
<div> </div>

#### Examples



The following example creates a region from a path and then tests to determine whether a point is inside the region.


```cpp
VOID Example_IsVisibleXY(HDC hdc)
{
   Graphics graphics(hdc);

   Point points[] = {
      Point(110, 20),
      Point(120, 30),
      Point(100, 60),
      Point(120, 70),
      Point(150, 60),
      Point(140, 10)};

   GraphicsPath path;
   SolidBrush solidBrush(Color(255, 255, 0, 0));

   path.AddClosedCurve(points, 6);

   // Create a region from a path.
   Region pathRegion(&path);
   graphics.FillRegion(&solidBrush, &pathRegion);

   // Check to see whether the point (125, 40) is in the region.
   INT x = 125;
   INT y = 40;
   if(pathRegion.IsVisible(x, y, &graphics))
   {

      // The point is in the region.
   }

   // Fill a small circle centered at the point (125, 40).
   SolidBrush brush(Color(255, 0, 0, 0));
   graphics.FillEllipse(&brush, x - 4, y - 4, 8, 8);
}
```





## -see-also




<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>



<a href="https://msdn.microsoft.com/2972b879-7d2f-4cad-b17d-670125f43691">Region</a>
 

 

