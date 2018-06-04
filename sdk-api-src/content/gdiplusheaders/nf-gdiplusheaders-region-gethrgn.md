---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# Region::GetHRGN


## -description


The <b>Region::GetHRGN</b> method creates a Windows Graphics Device Interface (GDI) region from this region.


## -parameters




### -param g [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object that contains the world and page transformations required to calculate the device coordinates of this region. 


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



<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">Rect</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn915769">Region</a>
 

 

