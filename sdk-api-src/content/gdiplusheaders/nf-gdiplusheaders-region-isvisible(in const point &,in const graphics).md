---
UID: NF:gdiplusheaders.Region.IsVisible(IN const Point &,IN const Graphics)
title: Region::IsVisible(IN const Point &,IN const Graphics)
author: windows-sdk-content
description: The Region::IsVisible method determines whether a point is inside this region.
old-location: gdiplus\_gdiplus_CLASS_Region_IsVisible_Point_point_Graphics_g_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\regionisvisiblemethods\isvisible_84pointamppoint_graphicsg.htm
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: IsVisible, IsVisible method [GDI+], IsVisible method [GDI+],Region class, Region class [GDI+],IsVisible method, Region.IsVisible, Region.IsVisible(IN const Point &,IN const Graphics), Region.IsVisible(const Point&,const Graphics*), Region::IsVisible, Region::IsVisible(IN const Point &,IN const Graphics), _gdiplus_CLASS_Region_IsVisible_Point_point_Graphics_g_, gdiplus._gdiplus_CLASS_Region_IsVisible_Point_point_Graphics_g_
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

# Region::IsVisible(IN const Point &,IN const Graphics)


## -description


The <b>Region::IsVisible</b> method determines whether a point is inside this region.


## -parameters




### -param point [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a></b>

Reference to a point to test. 


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



The following example creates a region from a path and then tests to determine whether a point is in the region.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_IsVisiblePoint(HDC hdc)
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
   Region pathRegion(&amp;path);
   graphics.FillRegion(&amp;solidBrush, &amp;pathRegion);

   // Check to see whether a point is in the region.
   Point testPoint(125, 30);

   if(pathRegion.IsVisible(testPoint, &amp;graphics))
   {
      // The test point is in the region.
   }

   // Fill a small circle centered at the test point.
   SolidBrush brush(Color(255, 0, 0, 0));
   graphics.FillEllipse(&amp;brush, testPoint.X - 4, testPoint.Y - 4, 8, 8);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534501(v=VS.85).aspx">Region</a>



<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a>
 

 

