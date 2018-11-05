---
UID: NF:gdiplusgraphics.Graphics.SetCompositingMode
title: Graphics::SetCompositingMode
author: windows-sdk-content
description: The Graphics::SetCompositingMode method sets the compositing mode of this Graphics object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_SetCompositingMode_compositingMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\setcompositingmode.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: Graphics class [GDI+],SetCompositingMode method, Graphics.SetCompositingMode, Graphics::SetCompositingMode, SetCompositingMode, SetCompositingMode method [GDI+], SetCompositingMode method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_SetCompositingMode_compositingMode_, gdiplus._gdiplus_CLASS_Graphics_SetCompositingMode_compositingMode_
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
 - Graphics.SetCompositingMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::SetCompositingMode


## -description


The <b>Graphics::SetCompositingMode</b> method sets the compositing mode of this <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object.


## -parameters




### -param compositingMode [in]

Type: <b><a href="https://msdn.microsoft.com/5bc2691d-8d7d-4322-bdae-a3b8ceb2d963">CompositingMode</a></b>

Element of the <a href="https://msdn.microsoft.com/5bc2691d-8d7d-4322-bdae-a3b8ceb2d963">CompositingMode</a> enumeration that specifies the compositing mode. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



Suppose you create a <a href="https://msdn.microsoft.com/8d5c8780-f03c-40b2-b237-e40121e3d6f6">SolidBrush</a> object based on a color that has an alpha component of 192, which is about 75 percent of 255. If your <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object has its compositing mode set to CompositingModeSourceOver, then areas filled with the solid brush are a blend that is 75 percent brush color and 25 percent background color. If your <b>Graphics</b> object has its compositing mode set to CompositingModeSourceCopy, then the background color is not blended with the brush color. However, the color rendered by the brush has an intensity that is 75 percent of what it would be if the alpha component were 255.

You cannot use CompositingModeSourceCopy along with TextRenderingHintClearTypeGridFit.


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object and sets its compositing mode to CompositingModeSourceOver. The code creates a <a href="https://msdn.microsoft.com/8d5c8780-f03c-40b2-b237-e40121e3d6f6">SolidBrush</a> object based on a color that has an alpha component of 128. The code passes the address of that brush to the <a href="https://msdn.microsoft.com/bee33174-f60f-415e-a1af-75aa3ad87342">Graphics::FillRectangle</a> method of the <b>Graphics</b> object to fill a rectangle with a color that is a half-and-half blend of the brush color and the background color. Then the code sets the compositing mode of the <b>Graphics</b> object to CompositingModeSourceCopy and fills a second rectangle with the same brush. In that second rectangle, the brush color is not blended with the background color.


```cpp
VOID Example_SetCompositingMode(HDC hdc)
{
   Graphics graphics(hdc);
   
   // Create a SolidBrush object with an alpha-blended color.
   SolidBrush alphaBrush(Color(180, 255, 0, 0));

   // Set the compositing mode to CompositingModeSourceOver,
   // and fill a rectangle.
   graphics.SetCompositingMode(CompositingModeSourceOver);
   graphics.FillRectangle(&alphaBrush, 0, 0, 100, 100);

   // Set the compositing mode to CompositingModeSourceCopy,
   // and fill a rectangle.
   graphics.SetCompositingMode(CompositingModeSourceCopy);
   graphics.FillRectangle(&alphaBrush, 100, 0, 100, 100);
}
```





## -see-also




<a href="https://msdn.microsoft.com/f8c22d1a-b96b-4d16-928e-20adbae4c4a7">Alpha Blending Lines and Fills</a>



<a href="https://msdn.microsoft.com/5bc2691d-8d7d-4322-bdae-a3b8ceb2d963">CompositingMode</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/dbc105a5-7541-491c-a8f0-fadecd1670cb">Graphics::GetCompositingMode</a>



<a href="https://msdn.microsoft.com/7d37da31-6ab0-4054-8a98-64cfbf9225ec">Graphics::GetCompositingQuality</a>



<a href="https://msdn.microsoft.com/e3544a81-d039-4bd6-89ea-d3883c95f7a9">Graphics::SetCompositingQuality</a>



<a href="https://msdn.microsoft.com/6ea9da15-a894-4b88-8615-bdfec19f4c1c">Graphics::SetTextRenderingHint</a>



<a href="https://msdn.microsoft.com/6e633cb2-8b0f-4b6a-95d8-f494d5f972eb">HatchBrush</a>



<a href="https://msdn.microsoft.com/0257a23c-560e-472e-863a-6ab5881dc156">New Features</a>



<a href="https://msdn.microsoft.com/8d5c8780-f03c-40b2-b237-e40121e3d6f6">SolidBrush</a>



<a href="https://msdn.microsoft.com/7f0c88f2-106f-4045-a6eb-cd84cab150c4">TextRenderingHint</a>
 

 

