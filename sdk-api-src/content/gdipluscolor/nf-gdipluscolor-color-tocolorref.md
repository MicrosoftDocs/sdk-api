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

# Color::ToCOLORREF


## -description


The <b>Color::ToCOLORREF</b> method converts this <a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a> object's <b>ARGB</b> value to a Windows Graphics Device Interface (GDI)<b>COLORREF</b> value.


## -parameters






## -returns



Type: <strong>Type: <b>COLORREF</b>
</strong>

This method returns a GDI<b>COLORREF</b> value that has the same red, green, and blue components as this color's <b>ARGB</b> value.




## -remarks



When the <b>ARGB</b> value is converted to a <b>COLORREF</b> value, the alpha component of the <b>ARGB</b> value is ignored.


#### Examples



The following example creates two <a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a> objects and converts the <b>ARGB</b> value of the first <b>Color</b> object into a GDI<b>COLORREF</b> value. The code then passes that <b>COLORREF</b> value to the <a href="https://msdn.microsoft.com/5fb15f81-8bed-4895-bec8-b687028cc5a2">Color::SetFromCOLORREF</a> method of the second <b>Color</b> object. Finally, the code uses the second <b>Color</b> object to fill a rectangle.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_ToCOLORREF(HDC hdc)
{
   Graphics graphics(hdc);

   // Create two Color objects.
   Color firstColor(255, 128, 128, 255);
   Color secondColor(255, 255, 255, 255);

   // Convert the ARGB value of the first color to a COLORREF value.
   COLORREF colorRef = firstColor.ToCOLORREF();

   // Use the COLORREF value to set the color of secondColor.
   secondColor.SetFromCOLORREF(colorRef);

   // Create a SolidBrush object based on secondColor, and fill a rectangle.
   SolidBrush colorRefBrush(secondColor);
   graphics.FillRectangle(&amp;colorRefBrush, Rect(0, 0, 100, 100));
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a>



<a href="https://msdn.microsoft.com/5fb15f81-8bed-4895-bec8-b687028cc5a2">Color::SetFromCOLORREF</a>
 

 

