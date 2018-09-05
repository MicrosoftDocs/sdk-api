---
UID: NF:gdiplusheaders.Region.GetHRGN
title: Region::GetHRGN
author: windows-sdk-content
description: The Region::GetHRGN method creates a Windows Graphics Device Interface (GDI) region from this region.
old-location: gdiplus\_gdiplus_CLASS_Region_GetHRGN_g_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\gethrgn.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetHRGN, GetHRGN method [GDI+], GetHRGN method [GDI+],Region class, Region class [GDI+],GetHRGN method, Region.GetHRGN, Region::GetHRGN, _gdiplus_CLASS_Region_GetHRGN_g_, gdiplus._gdiplus_CLASS_Region_GetHRGN_g_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdiplusheaders.h
req.include-header: Gdiplus.h
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Region.GetHRGN
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Region::GetHRGN


## -description


The <b>Region::GetHRGN</b> method creates a Windows Graphics Device Interface (GDI) region from this region.


## -parameters




### -param g [in]

Type: <b>const <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object that contains the world and page transformations required to calculate the device coordinates of this region. 


## -returns



Type: <strong>Type: <b>HRGN</b>
</strong>

This method returns a Windows handle to a GDI region that is created from this region.




## -remarks



It is the caller's responsibility to call the GDI function 
				<a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> to free the GDI region when it is no longer needed.


#### Examples



The following example creates a GDI+ region from a path and then uses the GDI+ region to create a GDI region. The code then uses a GDI function to display the GDI region.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetHRGN(HDC hdc)
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
   path.AddClosedCurve(points, 6);

    // Create a region from a path.
    Region pathRegion(&amp;path);

   // Get a handle to a GDI region.
   HRGN hRegion;
   hRegion = pathRegion.GetHRGN(&amp;graphics);

   // Use GDI to display the region.
   HBRUSH hBrush = CreateSolidBrush(RGB(255, 0, 0));
   FillRgn(hdc, hRegion, hBrush);

   DeleteObject(hBrush);
   DeleteObject(hRegion);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>



<a href="https://msdn.microsoft.com/2972b879-7d2f-4cad-b17d-670125f43691">Region</a>
 

 

