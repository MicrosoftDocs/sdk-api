---
UID: NF:gdipluscolor.Color.SetFromCOLORREF
title: Color::SetFromCOLORREF
author: windows-sdk-content
description: The Color::SetFromCOLORREF method uses a Windows Graphics Device Interface (GDI)COLORREF value to set the ARGB value of this Color object.
old-location: gdiplus\_gdiplus_CLASS_Color_SetFromCOLORREF_rgb_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\colorclass\colormethods\setfromcolorref.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: Color class [GDI+],SetFromCOLORREF method, Color.SetFromCOLORREF, Color::SetFromCOLORREF, SetFromCOLORREF, SetFromCOLORREF method [GDI+], SetFromCOLORREF method [GDI+],Color class, _gdiplus_CLASS_Color_SetFromCOLORREF_rgb_, gdiplus._gdiplus_CLASS_Color_SetFromCOLORREF_rgb_
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
 - Color.SetFromCOLORREF
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gdipluscolor.h
: 
- Color.SetFromCOLORREF
: 
req.product: GDI+ 1.0
---

# Color::SetFromCOLORREF


## -description


The <b>Color::SetFromCOLORREF</b> method uses a Windows Graphics Device Interface (GDI)<b>COLORREF</b> value to set the <b>ARGB</b> value of this <a href="https://msdn.microsoft.com/en-us/library/ms534427(v=VS.85).aspx">Color</a> object.


## -parameters




### -param rgb [in]

Type: <b>COLORREF</b>

GDI<b>COLORREF</b> value that specifies the red, green, and blue components of this <a href="https://msdn.microsoft.com/en-us/library/ms534427(v=VS.85).aspx">Color</a> object's <b>ARGB</b> value. The default value of the alpha component for this <b>Color</b> object is 255. 


## -returns



This method does not return a value.




## -remarks



A 32-bit GDI<b>COLORREF</b> value contains three, 8-bit color components. The most significant 8 bits are zeros and are not used, the next 8 bits contain the blue component, the next 8 bits contain the green component, and the last 8 bits (the least significant) contain the red component. Note that the ordering (starting with the high-order bits) of the components in a <b>COLORREF</b> value is blue, green, red; whereas, the ordering of an <b>ARGB</b> value is alpha, red, green, blue. 


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/en-us/library/ms534427(v=VS.85).aspx">Color</a> object and sets a GDI<b>COLORREF</b> value. The code then sets the <b>Color</b> object to the value of the GDI<b>COLORREF</b> value, creates a pen, and draws a line.

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




<a href="https://msdn.microsoft.com/en-us/library/ms534427(v=VS.85).aspx">Color</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536254(v=VS.85).aspx">Color::MakeARGB</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536257(v=VS.85).aspx">Color::ToCOLORREF</a>
 

 

