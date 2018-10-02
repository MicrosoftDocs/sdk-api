---
UID: NF:gdiplusgraphics.Graphics.GetSmoothingMode
title: Graphics::GetSmoothingMode
author: windows-sdk-content
description: The Graphics::GetSmoothingMode method determines whether smoothing (antialiasing) is applied to the Graphics object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_GetSmoothingMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\getsmoothingmode.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetSmoothingMode, GetSmoothingMode method [GDI+], GetSmoothingMode method [GDI+],Graphics class, Graphics class [GDI+],GetSmoothingMode method, Graphics.GetSmoothingMode, Graphics::GetSmoothingMode, _gdiplus_CLASS_Graphics_GetSmoothingMode_, gdiplus._gdiplus_CLASS_Graphics_GetSmoothingMode_
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
 - Graphics.GetSmoothingMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::GetSmoothingMode


## -description


The <b>Graphics::GetSmoothingMode</b> method determines whether smoothing (antialiasing) is applied to the 
			<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/42b3fc67-2cdb-4e14-88a0-aac914e8336a">SmoothingMode</a></b>
</strong>

If smoothing (antialiasing) is applied to this 
						<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object, this method returns SmoothingModeAntiAlias. If smoothing (antialiasing) is not applied to this 
						<b>Graphics</b> object, this method returns SmoothingModeNone. SmoothingModeAntiAlias and SmoothingModeNone are elements of the 
						<a href="https://msdn.microsoft.com/42b3fc67-2cdb-4e14-88a0-aac914e8336a">SmoothingMode</a> enumeration.




## -remarks



To get the rendering quality level for text, use the 
				<a href="https://msdn.microsoft.com/6525ac0e-bfd7-4471-bedb-df970b208222">Graphics::GetTextRenderingHint</a> method.


#### Examples



The following example sets the smoothing mode to high speed and draws an ellipse. It then gets the smoothing mode, changes it to high quality, and draws a second ellipse to demonstrate the difference.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetSmoothingMode(HDC hdc)
{
   Graphics graphics(hdc);

   // Set the smoothing mode to SmoothingModeHighSpeed.
   graphics.SetSmoothingMode(SmoothingModeHighSpeed);

   // Draw an ellipse.
   graphics.DrawEllipse(&amp;Pen(Color(255, 0, 0, 0), 3), Rect(10, 0, 200, 100));

   // Get the smoothing mode.
   SmoothingMode mode = graphics.GetSmoothingMode();


   // Test mode to see whether smoothing has been set for the Graphics object.
   if (mode == SmoothingModeAntiAlias)
   {
   graphics.SetSmoothingMode(SmoothingModeHighQuality);
   }

   // Draw an ellipse to demonstrate the difference.
   graphics.DrawEllipse(&amp;Pen(Color::Red, 3), Rect(220, 0, 200, 100));
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7c4869c1-76ff-42d1-abf1-387121943b2a">Antialiasing with Lines and Curves</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/8c1a26d9-b640-4f38-8276-10c4464525f2">Loading and Displaying Bitmaps</a>
 

 

