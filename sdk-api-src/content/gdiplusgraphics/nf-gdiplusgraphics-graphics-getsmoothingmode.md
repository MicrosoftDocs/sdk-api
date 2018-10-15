---
UID: NF:gdiplusgraphics.Graphics.GetSmoothingMode
title: Graphics::GetSmoothingMode
author: windows-sdk-content
description: The Graphics::GetSmoothingMode method determines whether smoothing (antialiasing) is applied to the Graphics object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_GetSmoothingMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\getsmoothingmode.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
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
			<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534173(v=VS.85).aspx">SmoothingMode</a></b>
</strong>

If smoothing (antialiasing) is applied to this 
						<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object, this method returns SmoothingModeAntiAlias. If smoothing (antialiasing) is not applied to this 
						<b>Graphics</b> object, this method returns SmoothingModeNone. SmoothingModeAntiAlias and SmoothingModeNone are elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534173(v=VS.85).aspx">SmoothingMode</a> enumeration.




## -remarks



To get the rendering quality level for text, use the 
				<a href="https://msdn.microsoft.com/en-us/library/ms535728(v=VS.85).aspx">Graphics::GetTextRenderingHint</a> method.


#### Examples



The following example sets the smoothing mode to high speed and draws an ellipse. It then gets the smoothing mode, changes it to high quality, and draws a second ellipse to demonstrate the difference.


```cpp
VOID Example_GetSmoothingMode(HDC hdc)
{
   Graphics graphics(hdc);

   // Set the smoothing mode to SmoothingModeHighSpeed.
   graphics.SetSmoothingMode(SmoothingModeHighSpeed);

   // Draw an ellipse.
   graphics.DrawEllipse(&Pen(Color(255, 0, 0, 0), 3), Rect(10, 0, 200, 100));

   // Get the smoothing mode.
   SmoothingMode mode = graphics.GetSmoothingMode();


   // Test mode to see whether smoothing has been set for the Graphics object.
   if (mode == SmoothingModeAntiAlias)
   {
   graphics.SetSmoothingMode(SmoothingModeHighQuality);
   }

   // Draw an ellipse to demonstrate the difference.
   graphics.DrawEllipse(&Pen(Color::Red, 3), Rect(220, 0, 200, 100));
}
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536351(v=VS.85).aspx">Antialiasing with Lines and Curves</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533830(v=VS.85).aspx">Loading and Displaying Bitmaps</a>
 

 

