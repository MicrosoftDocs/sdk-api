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

# Color::SetFromCOLORREF


## -description


The <b>Color::SetFromCOLORREF</b> method uses a Windows Graphics Device Interface (GDI)<b>COLORREF</b> value to set the <b>ARGB</b> value of this <a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a> object.


## -parameters




### -param rgb [in]

Type: <b>COLORREF</b>

GDI<b>COLORREF</b> value that specifies the red, green, and blue components of this <a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a> object's <b>ARGB</b> value. The default value of the alpha component for this <b>Color</b> object is 255. 


## -returns



This method does not return a value.




## -remarks



A 32-bit GDI<b>COLORREF</b> value contains three, 8-bit color components. The most significant 8 bits are zeros and are not used, the next 8 bits contain the blue component, the next 8 bits contain the green component, and the last 8 bits (the least significant) contain the red component. Note that the ordering (starting with the high-order bits) of the components in a <b>COLORREF</b> value is blue, green, red; whereas, the ordering of an <b>ARGB</b> value is alpha, red, green, blue. 


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a> object and sets a GDI<b>COLORREF</b> value. The code then sets the <b>Color</b> object to the value of the GDI<b>COLORREF</b> value, creates a pen, and draws a line.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_SetFromCOLORREF(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a color object.
   Color gdipColor(255, 0, 0, 255);

   // COLORREF is defined as an unsigned long in Wingdi.h
   unsigned long gdiColorRef = RGB(0, 0, 0);   // Set a GDI COLORREF value.

   // Set the color object to the COLORREF value.
   gdipColor.SetFromCOLORREF(gdiColorRef);

   // Create a Pen object based on the Color object.
   Pen pen((gdipColor), 10);

   // Draw a line.
   graphics.DrawLine(&amp;pen, 0, 0, 200, 100);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a>



<a href="https://msdn.microsoft.com/41befc00-c256-4f56-90c3-8fd5aa18bb49">Color::MakeARGB</a>



<a href="https://msdn.microsoft.com/1bf9093d-5316-4280-850e-b0738cf5d0cf">Color::ToCOLORREF</a>
 

 

