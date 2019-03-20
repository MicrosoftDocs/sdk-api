---
UID: NF:gdiplusgraphics.Graphics.SetSmoothingMode
title: Graphics::SetSmoothingMode (gdiplusgraphics.h)
author: windows-sdk-content
description: The Graphics::SetSmoothingMode method sets the rendering quality of the Graphics object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_SetSmoothingMode_smoothingMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\setsmoothingmode.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Graphics class [GDI+],SetSmoothingMode method, Graphics.SetSmoothingMode, Graphics::SetSmoothingMode, SetSmoothingMode, SetSmoothingMode method [GDI+], SetSmoothingMode method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_SetSmoothingMode_smoothingMode_, gdiplus._gdiplus_CLASS_Graphics_SetSmoothingMode_smoothingMode_
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
 - Graphics.SetSmoothingMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::SetSmoothingMode


## -description


The <b>Graphics::SetSmoothingMode</b> method sets the rendering quality of the <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object.


## -parameters




### -param smoothingMode [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534173(v=VS.85).aspx">SmoothingMode</a></b>

Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534173(v=VS.85).aspx">SmoothingMode</a> enumeration that specifies whether smoothing (antialiasing) is applied to lines and curves. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks



To get the rendering quality for text, use the <a href="https://msdn.microsoft.com/en-us/library/ms535728(v=VS.85).aspx">Graphics::GetTextRenderingHint</a> method. The higher the level of quality of the smoothing mode, the slower the performance.


#### Examples



The following example sets the smoothing mode to two different values and fills an ellipse to demonstrate each mode.


```cpp
VOID Example_SetSetSmoothingMode(HDC hdc)
{
   Graphics graphics(hdc);

   // Set the smoothing mode to SmoothingModeHighSpeed, and fill an ellipse.
   graphics.SetSmoothingMode(SmoothingModeHighSpeed);
   graphics.FillEllipse(&SolidBrush(Color(255, 0, 0, 0)), 0, 0, 200, 100);

   // Set the smoothing mode to SmoothingModeHighQuality, and fill an ellipse.
   graphics.SetSmoothingMode(SmoothingModeHighQuality);
   graphics.FillEllipse(&SolidBrush(Color(255, 0, 0, 0)), 200, 0, 200, 100);
}
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536351(v=VS.85).aspx">Antialiasing with Lines and Curves</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535723(v=VS.85).aspx">Graphics::GetSmoothingMode</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533830(v=VS.85).aspx">Loading and Displaying Bitmaps</a>
 

 

