---
UID: NF:gdiplusheaders.Region.GetBounds(OUT Rect,IN const Graphics)
title: Region::GetBounds(OUT Rect,IN const Graphics)
author: windows-sdk-content
description: The Region::GetBounds method gets a rectangle that encloses this region.
old-location: gdiplus\_gdiplus_CLASS_Region_GetBounds_Rect_rect_Graphics_g_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\regiongetboundsmethods\getbounds_6rectrect_graphicsg.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetBounds, GetBounds method [GDI+], GetBounds method [GDI+],Region class, Region class [GDI+],GetBounds method, Region.GetBounds, Region.GetBounds(OUT Rect,IN const Graphics), Region.GetBounds(Rect*,const Graphics*), Region::GetBounds, Region::GetBounds(OUT Rect,IN const Graphics), _gdiplus_CLASS_Region_GetBounds_Rect_rect_Graphics_g_, gdiplus._gdiplus_CLASS_Region_GetBounds_Rect_rect_Graphics_g_
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
 - Region.GetBounds
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gdiplusheaders.h
: 
- Region.GetBounds
: 
req.product: GDI+ 1.0
---

# Region::GetBounds(OUT Rect,IN const Graphics)


## -description


The <b>Region::GetBounds</b> method gets a rectangle that encloses this region.


## -parameters




### -param rect [out]

Type: <b><a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a> object that receives the enclosing rectangle. 


### -param g [in]

Type: <b>const <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>*</b>

Pointer to a 
					<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object that contains the world and page transformations required to calculate the device coordinates of this region and the rectangle. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



The current world and page transformations of the graphics object are used to calculate the region and the rectangle as they are drawn on the display device. The rectangle returned by <b>Region::GetBounds</b> is not always the smallest possible rectangle.


#### Examples



The following example creates a region from a path, gets the region's enclosing rectangle, and then displays both.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetBoundsRect(HDC hdc)
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
    Pen pen(Color(255, 0, 0, 0));
    Rect rect;

   path.AddClosedCurve(points, 6);

    // Create a region from a path.
    Region pathRegion(&amp;path);    
    
    // Get the region's enclosing rectangle.
    pathRegion.GetBounds(&amp;rect, &amp;graphics);

    // Show the region and the enclosing rectangle.
    graphics.FillRegion(&amp;solidBrush, &amp;pathRegion);
    graphics.DrawRectangle(&amp;pen, rect);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>



<a href="https://msdn.microsoft.com/2972b879-7d2f-4cad-b17d-670125f43691">Region</a>



<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a>
 

 

