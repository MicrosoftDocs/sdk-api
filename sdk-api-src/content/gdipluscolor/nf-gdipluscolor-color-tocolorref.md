---
UID: NF:gdipluscolor.Color.ToCOLORREF
title: Color::ToCOLORREF
author: windows-sdk-content
description: The Color::ToCOLORREF method converts this Color object's ARGB value to a Windows Graphics Device Interface (GDI)COLORREF value.
old-location: gdiplus\_gdiplus_CLASS_Color_ToCOLORREF_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\colorclass\colormethods\tocolorref.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Color class [GDI+],ToCOLORREF method, Color.ToCOLORREF, Color::ToCOLORREF, ToCOLORREF, ToCOLORREF method [GDI+], ToCOLORREF method [GDI+],Color class, _gdiplus_CLASS_Color_ToCOLORREF_, gdiplus._gdiplus_CLASS_Color_ToCOLORREF_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdipluscolor.h
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
 - Color.ToCOLORREF
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Color::ToCOLORREF


## -description


The <b>Color::ToCOLORREF</b> method converts this <a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a> object's <b>ARGB</b> value to a Windows Graphics Device Interface (GDI)<b>COLORREF</b> value.


## -parameters






## -returns



Type: <strong>Type: <b>COLORREF</b>
</strong>

This method returns a GDI<b>COLORREF</b> value that has the same red, green, and blue components as this color's <b>ARGB</b> value.




## -remarks



When the <b>ARGB</b> value is converted to a <b>COLORREF</b> value, the alpha component of the <b>ARGB</b> value is ignored.


#### Examples



The following example creates two <a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a> objects and converts the <b>ARGB</b> value of the first <b>Color</b> object into a GDI<b>COLORREF</b> value. The code then passes that <b>COLORREF</b> value to the <a href="https://msdn.microsoft.com/5fb15f81-8bed-4895-bec8-b687028cc5a2">Color::SetFromCOLORREF</a> method of the second <b>Color</b> object. Finally, the code uses the second <b>Color</b> object to fill a rectangle.

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




<a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a>



<a href="https://msdn.microsoft.com/5fb15f81-8bed-4895-bec8-b687028cc5a2">Color::SetFromCOLORREF</a>
 

 

