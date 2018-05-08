---
UID: NF:gdiplusgraphics.Graphics.SetSmoothingMode
title: Graphics::SetSmoothingMode
author: windows-driver-content
description: The Graphics::SetSmoothingMode method sets the rendering quality of the Graphics object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_SetSmoothingMode_smoothingMode_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\setsmoothingmode.htm
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: Graphics class [GDI+],SetSmoothingMode method, Graphics.SetSmoothingMode, Graphics::SetSmoothingMode, SetSmoothingMode, SetSmoothingMode method [GDI+], SetSmoothingMode method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_SetSmoothingMode_smoothingMode_, gdiplus._gdiplus_CLASS_Graphics_SetSmoothingMode_smoothingMode_
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	Graphics.SetSmoothingMode
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Graphics::SetSmoothingMode


## -description


The <b>Graphics::SetSmoothingMode</b> method sets the rendering quality of the <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object.


## -parameters




### -param smoothingMode [in]

Type: <b><a href="https://msdn.microsoft.com/42b3fc67-2cdb-4e14-88a0-aac914e8336a">SmoothingMode</a></b>

Element of the <a href="https://msdn.microsoft.com/42b3fc67-2cdb-4e14-88a0-aac914e8336a">SmoothingMode</a> enumeration that specifies whether smoothing (antialiasing) is applied to lines and curves. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



To get the rendering quality for text, use the <a href="https://msdn.microsoft.com/6525ac0e-bfd7-4471-bedb-df970b208222">Graphics::GetTextRenderingHint</a> method. The higher the level of quality of the smoothing mode, the slower the performance.


#### Examples



The following example sets the smoothing mode to two different values and fills an ellipse to demonstrate each mode.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_SetSetSmoothingMode(HDC hdc)
{
   Graphics graphics(hdc);

   // Set the smoothing mode to SmoothingModeHighSpeed, and fill an ellipse.
   graphics.SetSmoothingMode(SmoothingModeHighSpeed);
   graphics.FillEllipse(&amp;SolidBrush(Color(255, 0, 0, 0)), 0, 0, 200, 100);

   // Set the smoothing mode to SmoothingModeHighQuality, and fill an ellipse.
   graphics.SetSmoothingMode(SmoothingModeHighQuality);
   graphics.FillEllipse(&amp;SolidBrush(Color(255, 0, 0, 0)), 200, 0, 200, 100);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7c4869c1-76ff-42d1-abf1-387121943b2a">Antialiasing with Lines and Curves</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>



<a href="https://msdn.microsoft.com/85aacaa3-3a08-4879-8f49-7d082269cbe4">Graphics::GetSmoothingMode</a>



<a href="https://msdn.microsoft.com/8c1a26d9-b640-4f38-8276-10c4464525f2">Loading and Displaying Bitmaps</a>
 

 

